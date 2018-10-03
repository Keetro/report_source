---
title: Data Infastructure
author: tristan
date: '2018-10-03'
slug: data-infastructure
categories: []
tags: []
featured: ["https://multithreaded.stitchfix.com/blog/2018/09/05/datahighway","https://towardsdatascience.com/data-science-for-startups-model-services-2facf2dde81d?gi=800d1347cc9c"]
---
## Stitch Fix: Putting the Power of Kafka into the Hands of Data Scientists

It’s been a while since I read an amazing “here’s how we built our killer data infrastructure” post, but this one more than scratched the itch. It details a year-long project involving design, technology selection, and implementation.

The original goals:
1. Fully self-service for data scientists (remember, this is the company that believes engineers shouldn’t write ETL)
2. Enable real-time analysis
3. High-fidelity change capture

Even if you’re not imagining going through a project like this tomorrow, this post is the distillation of three people’s thinking over the course of an entire year, and contains tons of wisdom. My absolute favorite part was at the end where the author discusses their strong preference for investing in open source:

> Never have I worked on a project this challenging that involved writing so little code. We spent about two-thirds of the project timeline on research, design, debate and prototyping. Over months we whittled away at every component until it was as small and maintainable as possible. We tried to salvage as much as we could from our legacy infrastructure. More than once we submitted patches upstream to Kafka Connect to avoid extra complexity on our end.

An amazing model for much of modern software development.
(multithreaded.stitchfix.com)

## Zynga: Data Science for Startups - Model Services
I love this post! Here’s the intro:
> In order for data scientists to be effective at a startup, they need to be able to build services that other teams can use, or that products can use directly. For example, instead of just defining a model for predicting user churn, a data scientist should be able to set up an endpoint that provides a real-time prediction for the likelihood of a player to churn. 

Ok, yes, I definitely agree with that. But where does the post go from there? Oh, Idunno, how about an entire walkthrough of how to use AWS Lambda to create such a service?

There are so many “How to do X thing in Python” tutorials out there, but it’s rare to see a detailed tutorial on the practical stuff that will differentiate you as a data scientist. Thanks to Ben Weber of Zynga for a great post.
[towardsdatascience.com](https://towardsdatascience.com/data-science-for-startups-model-services-2facf2dde81d?gi=800d1347cc9c)