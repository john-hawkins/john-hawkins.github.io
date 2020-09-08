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

Text data is a fascinating source of information for data scientists. It can betray subtle clues
as to the mood, motives and behaviours of people, in both conscious and unconscious expressions. 
We can extract text from a wide variety of sources: internal documents, email records, web forms, 
social media posts, and even the text descriptions from financial transactions.

There are a set of very standard approaches to dealing with raw text to prepare it for machine
learning and statistics. From bag-of-words and n-gram models, through TF-IDF, topic modelling 
and up to the various flavours of neural network derived word embeddings like Word2Vec, GloVe, 
fastText or BERT. This toolset provides us with a powerful set of options for
feature engineering that require no domain knowledge and are widely applicable.
 
![Texturizer : Text features for Machine Learning](/images/texturizer/Texturizer_image.png)

However, there are also a virtually unlimited number of alternative ways to transform text 
into features for machine learning. Many of these are only appropriate for particular kinds 
of problems because they involve domain specific feature engineering scripts, and potentially 
bespoke dictionaries (or embedding models). Discovering what will work can present a daunting 
task for a time limited project.

To accelerate my own experimentation I have put together a text feature engineering package 
that will take a tabular dataset and a list of text column names and generate new features. 
It will add the features as additional columns appended to the data.
The user can control the types of features through the command line switches and thereby
control the exact set of features they want to explore. Similarly, the user can switch off features
that turn out to be ineffective. 

The current set of options are:

* ```-topics``` Indicators for the presence of words from common topics (e.g. Politics or Family). Note that these indicator words are chosen as unambiguous indicators. In other words it is not a complete vocabulary, but a vocabulary that is specific to the given topic. This switch has an additional option ```-topics=count``` which will counts all word matches from common topics.
* ```-pos``` Part of Speech proportions in the text. Using a SpaCy language model to process and tag each word.
* ```-literacy``` Checks for common literacy markers such as capitalisation problems or typos.
* ```-traits``` Checks for common stylistic elements or traits that suggest personality type, such as pronoun usage.
* ```-rhetoric``` Checks for rhetorical devices used for persuasion, for example an appeal to authority.
* ```-profanity``` Profanity check flags, including masked profanities and racial slurs.
* ```-sentiment``` Sentiment word counts and score plus a sentiment score from the TextBlob package.
* ```-emoticons``` A wide variety of flags for different kinds of emoticons and emoticon sentiment.
* ```-comparison``` Cross-column comparisons using a variety of edit distance metrics, note this is only applicable if you are running the application across multiple columns of text.

Many of the features in the package are derived from custom word lists and regular expressions
which users can edit and customize to their heart's content. This means that the package should be
easily customizable to make it work for your domain (or alternative language).  

There is a bunch of work to do to make that customisation process easier. I also have a laundry list
of additional features to add, but I feel like it is now ready for others to try. Please let me know if
you get some value from it.
  
You can pip install it: 
```pip install texturizer```
  
Or [grab the source code here](https://github.com/john-hawkins/texturizer)

