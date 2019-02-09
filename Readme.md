# Content Sources

There are two types of content that this site **currently** allows:
* Articles
* Commentary

All content is accomponied by rich meta data about :
1) piece:
  * Function Branch (e.g. Data Engineering, Data Science)
  * Relevant target audience info
2) original author
  * Avatars: Personal, Company
  * Description: Personal, Company
  * Link(s) to the original content
3) curator
  * same as original author
  * + promotional: Links

All posts are linked to the author, which can be crearted under [people](https://github.com/Keetro/people)

Here is a simple example of a meta table for an **Article**:
```
---
title: The Downfall of the Data Engineer
author: maxime
date: '2017-08-28'
slug: the-downfall-of-the-data-engineer
categories: [data science,data engineering,analytics]
tags: [airflow,maxime,lyft]
draft: true
type: article
---
```

And an example of a **Commentary**:
```
---
title: Data Discovery
author: tristan
date: '2018-10-03'
slug: data-discovery
categories: [Analytics]
tags: [google,uber,databook]
type: commentary
featured: ["https://www.blog.google/products/search/making-it-easier-discover-datasets/","https://eng.uber.com/databook/","https://medium.com/@leapingllamas/data-dictionary-a-how-to-and-best-practices-a09a685dcd61"]
---
```
