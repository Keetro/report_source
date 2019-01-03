---
title: Attribution Models
author: segah
date: '2018-10-04'
slug: attribution-models
categories: [analytics]
tags: [snowplow,salesforce]
type: commentary
featured: ["https://github.com/llooker/SFDC_campaign_attribution","https://discourse.snowplowanalytics.com/t/first-and-last-touch-attribution-models-in-sql-tutorial/27"]
---
## Campaign Attribution for Salesforce
Anyone who has ever worked with sales data knows, attribution is tricky. Prospect might run several trials, engage with an SDR, visit a company-sponsored event, attend a webinar, and perform various other activities before finally signing a contract. How do you perform attribution in that case? Based on just who closed the lead or something else? Looker's sales/marketing teams are some of the leaders in how data-driven sales are done. This is from their team:
[github/looker](https://github.com/llooker/SFDC_campaign_attribution)

## First and last touch attribution models in SQL
Unlike in the Looker framework above, the Snowplow guys are looking at the problem from the perspective of: how do we perform attribution if we don't even know which event actually led to purchase (supposedly, in the Looker framework we assume that the last event led to the purchase). They demonstrated a few different techniques of matching purchases (revenue events) to marketing events. Great all around write-up.

[discourse.looker](https://discourse.snowplowanalytics.com/t/first-and-last-touch-attribution-models-in-sql-tutorial/27)