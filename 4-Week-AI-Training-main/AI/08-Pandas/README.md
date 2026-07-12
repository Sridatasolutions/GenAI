# Day 8 – Introduction to Pandas

Today, I learned about **Pandas**, one of the most widely used Python libraries for data analysis and manipulation. Pandas provides powerful and easy-to-use data structures that simplify working with structured data.

## Topics Learned

* Introduction to Pandas
* Advantages of Pandas
* Series
* DataFrame
* Index and Labels
* Loading Datasets
* Exploratory Data Analysis (EDA)
* Data Inspection Functions

---

## What is Pandas?

Pandas is an open-source Python library used for data manipulation, analysis, and cleaning. It provides efficient data structures and tools for handling structured datasets.

### Advantages of Pandas

* Easy to read and manipulate data.
* Supports large datasets efficiently.
* Built-in functions for data analysis.
* Handles missing values effectively.
* Supports importing data from multiple sources.
* Integrates well with NumPy and visualization libraries.

---

## Main Data Structures

### 1. Series

A **Series** is a one-dimensional labeled array capable of storing data of any type.

### Example

```python
import pandas as pd

numbers = pd.Series([10, 20, 30, 40])
print(numbers)
```

---

### 2. DataFrame

A **DataFrame** is a two-dimensional table consisting of rows and columns.

### Example

```python
import pandas as pd

data = {
    "Name": ["Alice", "Bob"],
    "Age": [21, 22]
}

df = pd.DataFrame(data)
print(df)
```

---

## Index and Labels

Every Series and DataFrame has an **index**, which uniquely identifies each row. Columns in a DataFrame are identified using **labels**.

### Example

```python
import pandas as pd

marks = pd.Series([85, 90, 95], index=["A", "B", "C"])

print(marks)
```

---

## Loading Datasets

Pandas can load data from various file formats and sources.

### CSV File

```python
df = pd.read_csv("students.csv")
```

### Excel File

```python
df = pd.read_excel("students.xlsx")
```

### JSON File

```python
df = pd.read_json("students.json")
```

### SQL Database

```python
df = pd.read_sql(query, connection)
```

### From the Web

```python
df = pd.read_csv("https://example.com/data.csv")
```

---

## Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) is the process of understanding and summarizing a dataset before performing further analysis or building machine learning models.

EDA helps in:

* Understanding the dataset structure.
* Identifying missing values.
* Detecting patterns and trends.
* Finding inconsistencies in the data.
* Generating summary statistics.

---

## Common Data Inspection Functions

### View the First Five Rows

```python
df.head()
```

### View the Last Five Rows

```python
df.tail()
```

### Display Dataset Information

```python
df.info()
```

### Generate Statistical Summary

```python
df.describe()
```

### Display Column Names

```python
df.columns
```

### Display Dataset Shape

```python
df.shape
```

---

## What I Learned Today

* Pandas is a powerful library for data analysis.
* It mainly uses **Series** and **DataFrame** for storing data.
* Datasets can be loaded from CSV, Excel, JSON, SQL databases, and web sources.
* EDA helps understand a dataset before analysis.
* Functions like `head()`, `tail()`, `info()`, `describe()`, `columns`, and `shape` are useful for inspecting data.

