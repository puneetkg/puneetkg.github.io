---
title: "Data Analysis: 1.5 Exploratory Data Analysis"
date: 2022-01-27
tags: [Data preparation, data analysis, pandas, numpy, Exploratory Analysis, EDA]
header:
  overlay_image: "/images/2022-01-23-pandas.jpg"
  teaser: "/images/2022-01-23-pandas.jpg"
excerpt: "Using EDA to understand the impact of features on the target variable"
mathjax: true
author: "Puneet Gupta"
category: project
---

# Understanding the Dataset

If you are an analyst or a data scientist. The first step is to deep dive and understand the provided data. This understanding goes a long way to build hypothesis, insights, models and eventually recommendations. Since this is such an important task, folks have built libraries that directly help you with the complete EDA instead of writing manual codes to perform these steps. We will explore both in this post.

Legends:
Target variable: The metric that you need to model or analyse. Eg, sales, conversion, Revenue per Cost, Spend per Customer etc.
Independent variable: These are all the other features/columns present in the dataset which are assumed to be important to impact the target variable.
Continuous variable: These are variables which can attain any numerical value. Eg, selling price,
Categorical variable: These variables are categorical in nature single feature can only attain limited values which are repeated over users. Eg, Color, Gender, City Tier, Zone etc

## EDA by writing codes

**Numerical Analysis** <br />
This analysis is to understand the impact of continuous variables on the target feature.

Code:
```
df.groupby('ind')['target_col'].size()

# Plotting these values to understand better
df.groupby('ind')['target_col'].count().plot().bars()
```

**Categorical Analysis** <br />
The analysis helps understand the impact of different values within a feature
Code:
```
# getting values
df.groupby('categorical_col')['target_col'].size()

# Plotting these values to understand better
df.groupby('categorical_col')['target_col'].count().plot().bar()
```
Multiple iterations are required to understand the data better, these can be combined with [data filter]() discussed earlier in order to gain insights from selected data.

**Correlation between features** <br />
Code:
```
# Printing the correlation of features
df.head()
corrMatrix = df.corr()
print (corrMatrix)


# Plotting these correlations to understand visually using seaborn library
import seaborn as sns
sns.heatmap(corr)
```


## EDA using automated libraries

There are libraries like graphviz, sweetviz that allow you to do everything and more mentioned above

Code:
```
df.head()

# Install the package on your system
pip install sweetviz

# Importing sweetviz
import sweetviz as sv

# Analyzing the dataset
advert_report = sv.analyze(df)

# Display the report
advert_report.show_html('Advertising.html')
```
This generates an HTML file that can be seen on any browser

Hope this helps.

~P
