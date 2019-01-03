---
title: Analyzing Transactional Emails
author: segah
date: '2018-10-04'
slug: analyzing-transactional-emails
categories:
  - general
tags:
  - snowplow
  - sendgrid
  - Mandrill
type: commentary
featured: ["https://discourse.snowplowanalytics.com/t/tracking-email-events-sends-opens-and-clicks-with-snowplow-tutorial/436"]
---

## Tracking email events (sends, opens and clicks) with Snowplow
This is not really an article you would expect on the topic. And yet, I think it is important to cover. There are quite a lot of solutions out there covering campaign email analytics. A lesser known category of solutions cover transactional emails--the types of emails that are triggered as a result of customer's action on the site. Snowplow guys demonstrate how something like that is implemented on the frontend--before any analytics is done.

> Tracking email sends, opens and clicks with Snowplow is very common. In this post we detail how to do the above.

> How you do this depends on how you’re sending emails.

> If you’ve written your own application to send emails, you’d use one of our trackers 51 to record the send event: if it was a Python app that sent the email you’d record it using our Python tracker, or a Java app you’d use a Java tracker.

[discourse.snowplow](https://discourse.snowplowanalytics.com/t/tracking-email-events-sends-opens-and-clicks-with-snowplow-tutorial/436)
