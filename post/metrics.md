---
title: Metrics
author: tristan
# authors: [tristan,segah]
date: '2018-10-03'
slug: metrics
draft: true
categories: [analytics]
tags: []
type: commentary
featured: ["https://andrewchen.co/power-user-curve/","https://discourse.snowplowanalytics.com/t/basic-sql-recipes-for-web-data/25"]
---
@tristan
## The Power User Curve: The Best Way to Understand Your Most Engaged Users
This a brilliant example of thoughtful metric design. Almost every consumer software product measures daily actives, monthly actives, and the ratio of the two (often called the “stickiness ratio”). But Andrew Chen shows one particular view of DAU data that is both unusual and revealing; he calls it a “smile chart”.

The smile chart (example above) is a simple histogram of # of total active days in a given month. What’s interesting about it here is that it points to important characteristics of your user base. I’ll let him explain in the article, as he does so quite well.

Metric design often feels mundane, but making small changes in the way you’re looking at your data can reveal very different insights about the underlying reality. Don’t just apply the same lens that everyone else is using.
[andrewchen.co](https://andrewchen.co/power-user-curve/)

@segah
## Basic SQL recipes for web data
In this post Yali does a nice job summarizing key SQL queries needed to calculate aggregates for various metrics. While the queries are targeting native snowplow schema, they can just as well be ported to other use cases/underlying event collection engines.

[discourse.snowplow](https://discourse.snowplowanalytics.com/t/basic-sql-recipes-for-web-data/25)
