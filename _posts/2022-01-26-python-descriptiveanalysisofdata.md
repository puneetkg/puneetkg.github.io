---
title: "Data Analysis: 1.4 Descriptive Analytics"
date: 2022-01-26
tags: [Data preparation, data analysis, pandas, descriptive analysis]
header:
  overlay_image: "/images/2022-01-23-pandas.jpg"
  teaser: "/images/2022-01-23-pandas.jpg"
excerpt: "How understand data by descriptive statistics"
mathjax: true
author: "Puneet Gupta"
category: project
---

# Understanding the Dataset

It is extremely important for any analyst to understand the data provided to him, this makes it easier to think of scenarios and better capture the insights hidden in the data. In order to do that

Descriptive statistics of the dataset gives you an instant summary of the dataset. Try it out

```
df.describe()
```
It gives you the values like
- total count
- maximum value
- minimum value
- mean
- standard deviation
- 25th percentile
- 75% percentile

This function by default ignores all the categorical columns

But you can force the function to pull the categorical column as well by passing a parameter in the function
```
df.describe(include='all')
```

Hope this helps.

~P
