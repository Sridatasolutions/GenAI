
## NumPy (Numerical Python)

NumPy is the foundational library for numerical computing in Python.

It provides:

N-dimensional arrays (ndarray) for storing large amounts of numerical data efficiently.
Fast mathematical operations on arrays and matrices.
Linear algebra functions such as matrix multiplication and eigenvalues.
Statistical functions such as mean, median, variance, and standard deviation.
Random number generation for machine learning experiments.
 – Pandas Data Cleaning and Transformation

 how to manipulate, clean, and transform data using Pandas. These techniques are essential for preparing datasets before performing data analysis or building machine learning models.

 | AI Task                | NumPy Usage                                 |
| ---------------------- | ------------------------------------------- |
| Image Processing       | Images are stored as pixel matrices         |
| Deep Learning          | Neural network weights are matrices         |
| NLP                    | Words become numerical vectors (embeddings) |
| Recommendation Systems | User-item interaction matrices              |
| Computer Vision        | Tensor calculations                         |

Alternatives to NumPy

| Library                    | Best For                      | Advantages                                      |
| ----------------------------------------------------------------------- | ----------------------------- | ----------------------------------------------- |
| [JAX]                      | AI research and deep learning | Automatic differentiation
CUpy                         | GPU computing                 | NumPy-compatible API running on NVIDIA GPUs     |
| [PyTorch Tensors]          | Deep learning                 | GPU support and automatic gradients             |
| [TensorFlow Tensors]       | Production AI systems         | Distributed training and TPU support            |
| [Apache Arrow]             | Analytics and columnar memory | Extremely fast data exchange between systems    |
| [Polars Expressions]       | Data processing               | Fast Rust-based computation engine              |

Which is replacing NumPy in AI?

For modern AI workloads:
# PyTorch tensors dominate deep learning research.
# JAX is growing rapidly in advanced AI research.
# CuPy is popular when GPU acceleration is required.

                                                         # Pandas #

## Topics Learned

 Pandas

pandas is a library designed for data analysis and data manipulation.

Its main data structures are:

Series → One-dimensional data.
DataFrame → Table-like data similar to an Excel sheet or SQL table.


Why Pandas is important for AI

AI models require clean, organized, high-quality data.

Pandas helps with:

| Capability               | NumPy     | Pandas |
| ------------------------ | --------- | ------ |
| Numerical Computation    | ✅         | ❌      |
| Matrix Operations        | ✅         | ❌      |
| Data Cleaning            | ❌         | ✅      |
| Reading CSV/Excel        | ❌         | ✅      |
| Feature Engineering      | Limited   | ✅      |
| Model Input Preparation  | ✅         | ✅      |
| Performance Optimization | Very High | High   |



| Library                    | Best For                     | Advantages                                     |
| -------------------------------------------------------------------------------------------- | ---------------------------- | ---------------------------------------------- |
| [Polars]                   | Large datasets               | Rust-based, multithreaded, extremely fast      |
| [Dask DataFrame]           | Distributed computing        | Processes data larger than memory              |
| [PySpark DataFrame]  | Big data engineering         | Works on clusters with terabytes of data       |
| [Modin]                     | Scaling existing Pandas code | Minimal code changes required                  |
| [Vaex]                      | Billion-row datasets         | Memory-efficient processing                    |
| [DuckDB]                    | Analytical queries           | SQL directly on files without loading all data |

Why AI models need arrays instead of tables?

Machine learning models understand only numbers (vectors, matrices, tensors).



Why convert Spark DataFrames to Pandas?
Reason 1: Many traditional ML libraries expect local memory data

scikit-learn was originally designed for single-machine training, so it works with:

Pandas DataFrames
NumPy arrays

not with Spark DataFrames directly.

Delta Table
    ↓
Spark DataFrame
    ↓
Feature Engineering
    ↓
Small Training Dataset
    ↓
Pandas DataFrame (optional)
    ↓
NumPy Array or Tensor
    ↓
Machine Learning 



Visualization libraries expect Pandas

Examples:

Matplotlib
Seaborn
SHAP Explainability
EDA tools

These tools work naturally with Pandas.


Enterprise AI
Delta Table
 ↓
Spark DataFrame
 ↓
Spark ML or Feature Store
 ↓
PyTorch/TensorFlow


Distributed Deep Learning
Delta Table
 ↓
Spark DataFrame
 ↓
Petastorm or Arrow
 ↓
PyTorch Tensor
 ↓
GPU Training

Again, no Pandas required.


| Technology       | Purpose                    |
| ---------------- | -------------------------- |
| Delta Table      | Store massive datasets     |
| Spark DataFrame  | Distributed processing     |
| Pandas DataFrame | In-memory analytics        |
| NumPy Array      | Mathematical computations  |
| Tensor           | Deep learning computations |



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
