---
title: "Data Analysis: 1.2 filtering a dataframe"
date: 2022-01-24
tags: [Data preparation, data analysis, pandas]
header:
  overlay_image: "/images/2022-01-23-pandas.jpg"
  teaser: "/images/2022-01-23-pandas.jpg"
excerpt: "How to analyse data in python using Pandas"
mathjax: true
author: "Puneet Gupta"
category: project
---

# How to filter dataset

In this post we will learn how to filter the dataframe and then use that filtered dataframe to understand data better or correct values or assign new values after analysis

## Using '**iloc**' (a pandas function)

```
df.head()

# Selecting specific column after filtering
filtered_df = df.iloc[df['column1'] > 5]

# Selecting specific solumn after filtering
filtered_df = df.iloc[df['col1'] == 0]['col2']
```

## Using '**np.where**' (a numpy verison)

```
# Single condition
df['col'] = np.where(df.col)

# Multiple conditions
df['col'] = np.where((df.col1) > 4 & (df.col2 =='Test'), 'if condition satisfied', 'if cnodition not satisfied')
```


Hope this helps.

~P
