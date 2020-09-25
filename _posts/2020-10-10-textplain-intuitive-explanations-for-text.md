---
title: 'textplain : Intuitive explanations for text based machine learning models'
date: 2020-10-10
permalink: /posts/2020/10/textplain-intuitive-explanations-for-text/
tags:
  - data science
  - natural language processing
  - text mining
  - explainable machine learning
---

Text data is a powerful a useful source of signal in machine learning systems. 
There are a set of very standard approaches to dealing with raw text to prepare it for machine
learning and statistics. We routinely use: bag of words and n-gram models, TF-IDF, 
topic modelling or potentially word embeddings derived from one of the neural network language
models like Word2Vec, GloVe or fastText. All of these approaches have proven themselves as
effective text pre-processing techniques that require no domain knowledge and are widely applicable.

However, most of these approaches are relatively opaque which it comes to explaining what is driving
the performance or outputs of the models. Text data is less amenable to SHAP values for local feature
explanations, and there is no intuitive way to do permutation based feature importance correctly.
 
In the package we will explore methods of understanding the sub-structures of text that drive
predictive performance.
  
[In Development Here](https://github.com/john-hawkins/textplain)

