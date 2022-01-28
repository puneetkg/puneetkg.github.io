---
title: "Data Analysis: 1.1 Reading data using pandas"
date: 2022-01-23
tags: [machine learning, data analysis, pandas]
header:
  overlay_image: "/images/2022-01-23-pandas.jpg"
  teaser: "/images/2022-01-23-pandas.jpg"
excerpt: "How to read data in python using Pandas"
mathjax: true
author: "Puneet Gupta"
category: project
---

# Data Analysis in Python
Reading data is the first step that is extremely important to understand. There are multiple way of reading data in python but we will explore 2 ways of reading dataset and converting it into a dataframe.

# What is a Dataframe?

a Dataframe is a tabular representation of data in rows and columns.

Eg: Consider an office where the employees' data like joining date, salary, employee id, mail id etc are saved in a table, this table is of the form Dataframe.

| emp ID | Name | joining Date | Salary | mail id |
| --- | --- | --- | --- | --- |
| 123 | Akshay | 2001-03-12 | 500000 | ak.shay@company.com |
| 124 | Puneet | 2000-03-22 | 700000 | pu.neet@company.com |
| 125 | Max | 2000-01-12 | 1000000 | ma.x@company.com |

Once you have this data, to analyse this data you need to be able to read the data correctly and then place it in a data-frame to be able to use it.

# How to read data in Python

## Method1: Using 'csv' library

```
import csv
​
with open('log.txt', 'r') as in_file:
    stripped = (line.strip() for line in in_file)
    lines = (line.split(",") for line in stripped if line)
    with open('log.csv', 'w') as out_file:
        writer = csv.writer(out_file)
        writer.writerow(('title', 'intro'))
        writer.writerows(lines)
```

## Method2: Using 'pandas' library

### Reading '.csv'

```
import pandas as pd

df = pd.read_csv('FILE_PATH.csv')
```

### Reading excel file

Using pandas to read excel
```
import pandas as pd
pd.read_excel

df = pd.read_excel(open('tmp.xlsx', 'rb), sheet_name='Sheet3')  
```

OR
Use a 'xlrd' library

```
import xlrd

# Give the location of the file
loc = ("path of file")

# To open Workbook
wb = xlrd.open_workbook(loc)
sheet = wb.sheet_by_index(0)

# For row 0 and column 0
print(sheet.cell_value(0, 0))
```

### When data is too huge or reduce memory usage

a. You can read only a limited dataset by providing value to the 'chunksize' parameter provided in 'read_csv' function.

```
import pandas as pd

df = pd.read_csv('FILE_PATH.csv', chunksize = 1)
df = pd.DataFrame(df)

chunk_list = []  # append each chunk df here

# Each chunk is in df format
for chunk in df_chunk:  
    # perform data filtering
    chunk_filter = chunk_preprocessing(chunk)

    # Once the data filtering is done, append the chunk to list
    chunk_list.append(chunk_filter)

# concat the list into data-frame
df_concat = pd.concat(chunk_list)
```
Once you have read all the chunks, merge them together to use the dataset. Note that **df_chunk** is not a data-frame but an object for further operation in the next step

OR

b. You can read first n lines from the dataframe and use them for an initial analysis , by passing value to the 'nrows' parameter

```
import pandas as pd

df = pd.read_csv('FILE_PATH.csv', nrows = 9999)
```

You will only need these majorly to read your data into a data-frame.

Hope this helps.

~P
