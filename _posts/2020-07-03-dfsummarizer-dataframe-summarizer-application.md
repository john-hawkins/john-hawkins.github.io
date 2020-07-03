---
title: 'dfsummarizer : A command line application for summarizing data frames'
date: 2020-07-03
permalink: /posts/2020/07/dfsummarizer-dataframe-summarizer-application/
tags:
  - data science
  - data analytics
  - data engineering
---

Summarizing data is one of those small tasks that data scientists and analysts need to do
routinely. However, we often need to write bespoke scripts for this and then go through
a tedious process to format it for sharing or publication.

Many of the standard data summarizing rotines in common analytics packages leave a lot to be
desire. The pandas dataframe summary function ignore missing values and only summarise numeric
data. Most data scientists require more comprehensive summaries of a dataset to be sure that 
they are taking a reasonable modelling approach. There is no substitute for deeper dives into
specific columns and features using plots and other visualisations, however, high level summarisation
is a great guide to where to spend your efforts.

For all of these reasons I have built a small and focused command line application that will
allow you to generate a summary table of your data and output it as either Latex or Markdown.

[Get it here](https://github.com/john-hawkins/dfsummarizer)

