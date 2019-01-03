---
title: Recommendation System
author: tristan
date: '2018-10-03'
slug: recommendation-system
categories:
  - data science
tags: []
type: commentary
featured: ["https://eng.uber.com/uber-eats-query-understanding/"]
---
## Food Discovery with Uber Eats: Building a Query Understanding Engine

> Choice is fundamental to the Uber Eats experience. At any given location, there could be thousands of restaurants and even more individual menu items for an eater to choose from. Many factors can influence their choice. For example, the time of day, their cuisine preference, and current mood can all play a role. At Uber Eats, we strive to help eaters find the exact food they want as effortlessly as possible.

Fairly detailed walkthrough of the Uber Eats recommendation system. The highlight of the post is the work the team has done on ontologies. Cuisine has a lot of concepts that map to one another, and in order to build an effective recommender the team has had to build a graph that understands these relationships.
[eng.uber.com](https://eng.uber.com/uber-eats-query-understanding/)