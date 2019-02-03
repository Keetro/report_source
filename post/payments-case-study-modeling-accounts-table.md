---
title: "Case study: modeling accounts table "
author: segah
team: caura
type: article
date: '2018-09-21'
categories:
  - analytics
slug: payments-case-study-modeling-accounts-table
tags: [Payments,accounts,metrics]
---

Modern payment companies today have some of the most complex datasets. Not only do they store the usual account or user type data, but they also operate in the complexity of financial banking: bank ledgers, deposit/widthdrawl records, payment statuses, refunds, and everything else.

One of the key attributes relevant to any financial-transactional datasets is the presence of an accounts table. An accounts table is like a snapshot of what's going on with this account today–at the latest snapshot in time.

<!--more-->
Unfortunately, the underlying data warehouse rarely is kept in sync with the latest analytical needs. The logic of an additional column/attribute is a higher-level logic, requiring abstraction–moving it down to the data engineering level is a lot more work than writing SQL.

## Challenges

In this case the data team asked whether we could enrich their existing accounts information with additional properties. The logic could be best characterized into:
* Deposit / Withdrawl summaries by account
* Funding Source summaries by account
* Sending Limit summaries by account
* Social (network) summaries by account

The challenge here was to model the data using underlying raw event/transaction-based tables while also ensuring the new attributes were calculated using all the key logic used elsewhere throughout analytics–namely: ignored account ids, excluded payment types, and excluded irrelevant timeframes.

## Modeling process

Before proceeding, we needed to understand the underlying relationships between accounts and various tables. For example, for the deposits & withdrawals, the relationships are straightforward:
```
deposits_and_withdrawls dw
LEFT JOIN accounts ON dw.account_id = accounts.id
```

where we handle the transaction type always at the measure level:
```
SELECT
SUM(CASE WHEN dw.type = 'credit' THEN dw.amount ELSE -1*dw.amount END) AS deposits
# or
SUM(CASE WHEN dw.type = 'debit' THEN dw.amount ELSE -1*dw.amount END) AS withdrawl
...
FROM deposits_and_withdrawls dw
LEFT JOIN accounts ON dw.account_id = accounts.id
...
GROUP BY accounts.id
```
> >
Sidenote: the above would be different if we were to join the transactional table into the accounts. In that case, we might actually perform the logic at the join level:
SELECT accounts.id
, SUM(deposits.amount) AS deposits
, SUM(withdrawls.amount) AS withdrawl ...
FROM accounts LEFT JOIN deposits_and_withdrawls deposits
ON accounts.id = dw.account_id and dw.type = 'credit'
LEFT JOIN deposits_and_withdrawls widthdrawls ON accounts.id = dw.account_id and dw.type = 'debit' GROUP BY accounts.id

The result of this process leads us to additional attributes:
[1] "Account ID"
[2] "Initial Deposit Date"
[3] "Lifetime Deposits"
[4] "Registration to First Deposit (# of days)"

What is interesting is that these result from very simple measures:
```
MIN => Initial Date
COUNT => LIFETIME
DATEDIFF => Registration...
```
Once we have all this as an intermediary table, we can build even further more interesting measures:
1. % of Users with Deposits on First Day
2. % of Users with Withdrawls on the day of Registration
3. % of Users with FULL Withdrawls in X Days/Weeks/Months
4. Lifetime bank accounts connected
5. Days since sign-up
6. …

## Summary

The client came to us for high-level business goals and proxy metrics helping those goals. We've translated those metrics into the language of the data model and underlying data. In this case, the key underlying attributes were amount and type of the account. From these we were able to derive much more complex higher-level concepts.
