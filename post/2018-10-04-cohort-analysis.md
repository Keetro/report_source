---
title: Cohort Analysis
author: segah
date: '2018-10-04'
slug: cohort-analysis
categories:
  - analytics
  - vendors
tags: [snowplow,sisense]
type: commentary
featured: ["https://discourse.snowplowanalytics.com/t/performing-cohort-analyses-with-snowplow/1154","https://discourse.looker.com/t/analytic-block-creating-custom-cohort-analysis/256"]
related: ["https://support.sisense.com/hc/en-us/articles/230650908-Creating-Cohort-Analysis-With-Sisense"]
---

@segah
## Performing cohort analyses with Snowplow
A SQL-heavy write-up on how to implement a cohort analysis. Describes data coming from snowplow's collection engine, but could just as well be generalized for a broader set of datasets and sources of data.
The snowplow guys start well with answering *"what is a cohort analysis"*:

> A cohort analysis is a longitudal study that compares two or more groups of customers / users (cohorts) over a period of time. The term cohort analysis therefore encompasses a wide variety of analyses:

> **We can vary our cohort definitions, depending on what we want to test.** (For example, if we wanted to see if customers acquired from particular marketing channels were more valuable over their lifetimes, we’d define our cohorts based on the customer acquisition channel. On the other hand, if we wanted to see if we’ve got better at converting freemium users to paid users over time, we’d compare cohorts of users who started with the service a long time ago, with those that started more recently: defining our cohorts by month joined.)

> **We can vary the metric we are comparing between are cohorts.** (For example, comparing the average lifetime value of customers in each cohort, or retention levels by cohort)

[discourse.snowplow](https://discourse.snowplowanalytics.com/t/performing-cohort-analyses-with-snowplow/1154)

@segah
## Creating Custom Cohort Analysis (Looker)
I've always seen the power of Looker in the ability to explore row-level data whereas this particular analytical write-up is focused on surfacing aggregates. That said, it is a useful framework to reference--whether you use Looker or not.

[discourse.looker](https://discourse.looker.com/t/analytic-block-creating-custom-cohort-analysis/256)