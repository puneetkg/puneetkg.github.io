---
title: "1. Data Analysis: 1.2 renaming columns in the dataframe"
date: 2022-01-25
tags: [Data preparation, data analysis, pandas]
header:
  overlay_image: "/images/2022-01-23-pandas.jpg"
  teaser: "/images/2022-01-23-pandas.jpg"
excerpt: "How to rename columns of a dataframe"
mathjax: true
author: "Puneet Gupta"
category: project
---

# How to rename columns

Renaming columns in a dataframe becomes important when you have to columns named with same names, or you have concatenated two dataframes together with similar columns.

## Using '**.columns**'
This is the simplest but a little tedious if you have a lot of columns, if you want to change the value of one column then print out the values of all the columns and change the value of that one column and pass the list

```
# renaming all columns
df.columns = ['col1', 'col2', 'col3']
```

## Using '**.rename()**' function
This is the function provided by pandas library to change the name of the columns

```
df.rename(columns = {'variable': 'Year', 'value': 'Income'}, inplace = True)
print(df)
```

### Using a '**dict**'
A dictionary can be passed in the the rename function with key value pair of current column name and new column name
```
df.rename(columns={0 : 'title', 1 : 'author'},inplace=True)
```

### renaming the last column in a dataframe
This is a special usecase that i encountered and seemed an important usecase, this usually happens when you convert a pandas series into a dataframe and try to concat it with the base dataframe, if the series name is not given, it shows the column name as 0, which becomes difficult to tweak.
```
df.columns = [*df.columns[:-1], 'Test']
print(df)
```
`* is used to find the first value starting from -1 and change the column name only for that column


Hope this helps.

~P
