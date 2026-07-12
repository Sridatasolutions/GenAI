# Day 9 – Pandas Data Cleaning and Transformation

Today, I learned how to manipulate, clean, and transform data using Pandas. These techniques are essential for preparing datasets before performing data analysis or building machine learning models.

## Topics Learned

* Selecting Rows and Columns
* Filtering Data with Conditions
* Data Cleaning and Preprocessing
* Handling Missing Values
* Detecting and Removing Duplicates
* Type Conversion
* Sorting and Ranking
* Reshaping Data
* Aggregation and Grouping
* Merging DataFrames

---

## Selecting Rows and Columns

Pandas provides multiple ways to access specific rows and columns from a DataFrame.

### Example

```python
# Select a column
df["Name"]

# Select multiple columns
df[["Name", "Age"]]

# Select rows using iloc
df.iloc[0:5]
```

---

## Filtering Data with Conditions

Filtering allows us to retrieve only the rows that satisfy a specific condition.

### Example

```python
filtered = df.query("Age < 50")
```

---

## Data Cleaning and Preprocessing

Data cleaning is the process of identifying and correcting incomplete, inaccurate, or inconsistent data before analysis.

---

## Handling Missing Values

### Check for Missing Data

```python
df.isnull()
```

Returns `True` for missing values.

```python
df.isnull().sum()
```

Returns the number of missing values in each column.

---

### Drop Missing Data

```python
df.dropna()
```

Removes rows containing missing values.

```python
df.dropna(axis=1)
```

Removes columns containing missing values.

---

### Fill Missing Data

Replace missing values using different techniques.

```python
df.fillna(0)
```

Replace all missing values with `0`.

```python
df["Age"].fillna(df["Age"].mean())
```

Replace missing values with the column mean.

```python
df.ffill()
```

Forward Fill.

```python
df.bfill()
```

Backward Fill.

---

## Detecting and Removing Duplicates

Duplicate records can be identified and removed to improve data quality.

### Example

```python
df.duplicated()

df.drop_duplicates()
```

---

## Type Conversion

The `astype()` method is used to convert the data type of a column.

### Example

```python
df["Age"] = df["Age"].astype(int)
```

---

## Sorting and Ranking

Sorting organizes data in ascending or descending order.

### Example

```python
df.sort_values("Age")
```

---

## Reshaping Data

Reshaping changes the structure of a DataFrame for easier analysis.

### Example

```python
df.pivot(index="Department", columns="Year", values="Sales")
```

---

## Aggregation and Grouping

Grouping allows data to be summarized based on one or more columns.

### Example

```python
df.groupby("Department")["Salary"].mean()
```

---

## Merging DataFrames

Pandas provides the `merge()` function to combine multiple DataFrames, similar to SQL joins.

### Example

```python
merged = pd.merge(df1, df2, on="ID")
```

---

## What I Learned Today

* Selected rows and columns using different indexing techniques.
* Filtered datasets using conditions.
* Cleaned datasets by handling missing values.
* Detected and removed duplicate records.
* Converted data types using `astype()`.
* Sorted and organized data efficiently.
* Reshaped datasets for analysis.
* Used grouping and aggregation to summarize data.
* Merged multiple DataFrames similar to SQL joins.
