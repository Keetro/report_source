---
title: Debugging bad event collection
author: segah
date: '2018-10-04'
slug: debugging-bad-event-collection
categories: [data engineering]
tags: [snowplow]
type: commentary
featured: ["https://discourse.snowplowanalytics.com/t/debugging-bad-rows-in-elasticsearch-and-kibana-tutorial/28"]
---

## Debugging bad rows in Elasticsearch and Kibana (Snowplow)
Even if you are not using these particular technologies, this is a useful article to review. I've come across many people who rely on event streaming technologies without understanding drop and error rates. Often the magnitudes are miniscule, so there is nothing to worry about. But if this stuff is important to you, then read on. 

> One of the features that makes Snowplow unique is that we actually report bad data: any data that hits the Snowplow pipeline and fails to be processed successfully. This is incredibly valuable, because it means you can:

> * spot data tracking issues that emerge, often during testing, and address them at the source
* have a high degree of confidence that trends in the data reflect trends in the business, not data issues
* recover events that failed to be processed

> Most Snowplow users load their bad rows into Elasticsearch. In this guide, we will walk through how to use Kibana and Elasticsearch to:

> * monitor the number of bad rows
* spot problems that emerge
* diagnose the route causes of the issues, so that they can be addressed upstream

> For more information on how to debug bad rows using Spark or Elasticsearch without Kibana, or how to recover events, visit these tutorials:

> * Debugging bad rows in Spark and Zeppelin
* Debugging bad rows in Elasticsearch using curl (without Kibana)
* Recovering events with a missing schema (documentation 5)

[discourse.snowplow](https://discourse.snowplowanalytics.com/t/debugging-bad-rows-in-elasticsearch-and-kibana-tutorial/28)

## Debugging bad rows in Spark and Zeppelin
Similarly to above, goes into how Snowplow can be used to track missing event data. Can be useful...
<img src="https://discourse-cdn-sjc1.com/business6/uploads/snowplowanalytics/optimized/1X/762a753773a5e965a82afb2e183027b06494cfb5_1_690x345.png"/>
[discourse.snowplow](https://discourse.snowplowanalytics.com/t/debugging-bad-rows-in-spark-and-zeppelin-tutorial/400)