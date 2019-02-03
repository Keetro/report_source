---
title: Methods for model selection
author: tristan
date: '2018-10-03'
slug: methods-for-model-selection
categories:
  - data science
tags: []
featured: ["http://www.fast.ai/2018/07/16/auto-ml2/","https://distill.pub/2018/feature-wise-transformations/"]
---

## An Opinionated Introduction to AutoML and Neural Architecture Search

This is a post I’ve been hoped someone would write. There was a lot of commotion about automating machine learning after the recent announcement of Google’s AutoML. The press storyline was that products like this would make machine learning expertise unnecessary, which seemed obviously misleading to anyone who had any sense of how machine learning actually works in practice.

This article demystifies the entire area of automated hyperparameter selection and neural architecture search. It goes deep into various approaches that researchers have taken on the problem since 2013, and the modern approaches of evolutionary or reinforcement-learning-based approaches. It also talks about why these problems are actually a fairly small part of the overall ML process, and why transfer learning is often a superior approach.

If you’ve been following AutoML with any interest, this is the best soup-to-nuts analysis piece that I’ve seen. It’s a useful technology, but don’t buy the marketing :)
[www.fast.ai](http://www.fast.ai/2018/07/16/auto-ml2/)

## Feature-Wise Transformations
New research from Yoshua Bengio and team. Their summary is excellent:
> Many real-world problems require integrating multiple sources of information. Sometimes these problems involve multiple, distinct modalities of information — vision, language, audio, etc. — as is required to understand a scene in a movie or answer a question about an image.
When approaching such problems, it often makes sense to process one source of information in the context of another; for instance, in the right example above, one can extract meaning from the image in the context of the question. In machine learning, we often refer to this context-based processing as conditioning: the computation carried out by a model is conditioned or modulated by information extracted from an auxiliary input.
Finding an effective way to condition on or fuse sources of information is an open research problem, and in this article, we concentrate on a specific family of approaches we call feature-wise transformations.
[distill.pub](https://distill.pub/2018/feature-wise-transformations/)