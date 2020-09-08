---
title: 'texturizer : Exploring diverse text derived features for machine learning'
date: 2020-09-06
permalink: /posts/2020/09/exploring-diverse-text-derived-features-for-machine-learning/
tags:
  - data science
  - feature engineering
  - natural language processing
  - text mining
---

Text data is a potential source of valuable information for data scientists. We can extract it
from email records, web forms, social media, even the text descriptions from financial transactions.

There are a set of very standard approaches to dealing with raw text to prepare it for machine
learning and statistics. Bag of words and n-gram models, TfiDf, topic modelling and all of the
various flavours of neural network derived word embeddings provide us with a powerful set of 
feature engineering approaches that require no domain knowledge and are widely applicable.
 
![Texturizer : Text features for Machine Learning](/images/texturizer/Texturizer_image.png)

There are also a virtually unlimited number of alternative ways to transform text into features for 
machine learning. Many of these are only appropriate for particular kinds of problems because 
they involve domain specific feature engineering scripts, and potentially bespoke 
dictionaries (or embedding models). Discovering what will work can present a daunting 
task for a time limited project.

To accelerate my own experimentation I have put together a text feature engineering package 
that will take a tabular dataset and a list of text column names and generate new features. 
It will add the feature as additional columns appended to the data.
The user can control the types of features through the command line switches and thereby
control the exact set of features you want to explore. Similarly, the user can switch off features
that turn out to be ineffective. Current options are:

* -topics. Indicators for the presence of words from common topics (e.g. Politics or Family). Note that these indicator words are chosen as unambiguous indicators. In other words it is not a complete vocabulary, but a vocabulary that is specific to the given topic. This switch has an additional option ```-topics=count``` which will counts all word matches from common topics.
* -pos. Part of Speech proportions in the text.
* -literacy. Checks for common literacy markers.
* -traits. Checks for common stylistic elements or traits that suggest personality type.
* -rhetoric. Checks for rhetorical devices used for persuasion.
* -profanity. Profanity check flags.
* -sentiment. Sentiment word counts and score, and sentiment score from the TextBlob package.
* -emoticons. A wide variety of emoticon check flags and emoticon sentiment.
* -comparison. Cross-column comparisons using edit distance metrics, note this is only applicable if you are running the application across multiple columnsof text.


Many of the features in the package are derived from custom word lists and regular expressions
which users can edit and customize to their heart's content. This means that the package should be
easily customizable to make it work for your domain (or alternative language).  
  
[Get it here](https://github.com/john-hawkins/texturizer)

