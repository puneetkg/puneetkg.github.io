---
title: "Data Analysis: 1.6 plotting data to understand it better"
date: 2022-01-28
tags: [Data preparation, data analysis, pandas, numpy, Exploratory Analysis, visualisation]
header:
  overlay_image: "/images/2022-01-23-pandas.jpg"
  teaser: "/images/2022-01-23-pandas.jpg"
excerpt: "Using libraries to plot data and understand data better"
mathjax: true
author: "Puneet Gupta"
category: project
---

# Using Visualisation to understand

Data visualisation is an important step in data analysis to better understand the data. This is helps visualise the relationships better. In this post we will walk through majority of the graphs that can be plotted using matplotlib

## Line Charts

Line charts are best to visualise features which change with time or series of data points. Eg, price changes, Speed, population etc

Code:
```
# Direct plot from a dataframe

df.head()
df.col.plot()

# matplotlib
import matplotlib.pyplot as plt

## Creating a graphs

### figure size
plt.figure(figize = (7,5))


### Title, x tile and y title

plt.title('test title', fontsize=20)

plt.xlabel('xl abel', fontsize=15)
plt.ylabel('ylabel', fontsize=15)

## ploting first 100 rows

df.loc[0:100,'GKHandling'].plot()
```


## Bar Charts
Bar charts can be used to visualise categorical

Code:
```
# Direct plot from a dataframe

df.head()
df.col.plot()


# matplotlib
import matplotlib.pyplot as plt

## Creating a graph

### figure size
plt.figure(figize = (7,5))


### Title, x tile and y title

plt.title('test title', fontsize=20)

plt.xlabel('xl abel', fontsize=15)
plt.ylabel('ylabel', fontsize=15)

## ploting first 100 rows

df.loc[0:100,'GKHandling'].plot.bar()
```

## Pie Charts

Code:
```
import matplotlib.pyplot as plt

df.head()

plt.pie(df.loc[0:10,'GKHandling'], labels = df.loc[0:10,'Name'])
```


## Scatter Plot

Code:
```
df.head()
df.columns

plt.scatter(df['GKHandling'], df.loc['Overall'])
```


## Histogram

Code:
```
plt.hist(df.col)
```

## Boxplot

Code:
```
plt.boxplot(df['col'])
```

Hope this helps

~P
