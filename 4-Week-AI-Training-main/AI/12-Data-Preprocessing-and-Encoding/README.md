# Day 12 – Data Preprocessing and Encoding

Today, I learned about **data preprocessing**, one of the most important steps in Machine Learning. I practiced handling missing values, converting data types, and encoding categorical data into numerical values using Scikit-learn.

## Topics Learned

* Data Preprocessing
* Handling Missing Values
* SimpleImputer
* Type Conversion
* One-Hot Encoding
* Ordinal Encoding
* Label Encoding

---

## What is Data Preprocessing?

Data preprocessing is the process of preparing raw data before it is used for analysis or training a machine learning model. It improves the quality of data and helps produce better model performance.

Common preprocessing tasks include:

* Handling missing values
* Converting data types
* Encoding categorical data
* Feature scaling
* Removing duplicates

---

## Loading the Dataset

A dataset can be loaded using Pandas.

### Example

```python
import pandas as pd

dataset = pd.read_csv("loan_sanction_train.csv")
data = dataset.copy()
```

---

## Exploring the Dataset

Before preprocessing, it is important to understand the dataset.

### Check Missing Values

```python
data.isnull().sum()
```

### Display Column Names

```python
data.columns
```

### View Dataset Information

```python
data.info()
```

---

## Type Conversion

The `astype()` function is used to convert the data type of a column.

### Example

```python
data["ApplicantIncome"] = data["ApplicantIncome"].astype("float64")
```

---

## Handling Missing Values using SimpleImputer

`SimpleImputer` replaces missing values using different strategies such as mean, median, or most frequent value.

### Example

```python
from sklearn.impute import SimpleImputer

si = SimpleImputer(strategy="mean")

arr = si.fit_transform(
    data[[
        "ApplicantIncome",
        "CoapplicantIncome",
        "LoanAmount",
        "Loan_Amount_Term",
        "Credit_History"
    ]]
)
```

---

# Encoding

Machine learning models cannot work directly with categorical values. Encoding converts categorical data into numerical form.

---

## One-Hot Encoding

One-Hot Encoding creates a separate binary column for each category.

### Example

```python
from sklearn.preprocessing import OneHotEncoder

encoder = OneHotEncoder(sparse_output=False)

encoded = encoder.fit_transform(data[["Gender"]])
```

---

## Ordinal Encoding

Ordinal Encoding assigns numerical values to categories that have a natural order.

### Example

```python
from sklearn.preprocessing import OrdinalEncoder

encoder = OrdinalEncoder()

education = [["School"], ["Graduate"], ["Post Graduate"]]

encoded = encoder.fit_transform(education)
```

---

## Label Encoding

Label Encoding converts each unique category into an integer.

### Example

```python
from sklearn.preprocessing import LabelEncoder

encoder = LabelEncoder()

colors = ["Red", "Blue", "Green", "Blue"]

encoded = encoder.fit_transform(colors)
```

---

## What I Learned Today

* Data preprocessing is an essential step before training machine learning models.
* Missing values can be handled using `SimpleImputer`.
* Data types can be changed using `astype()`.
* One-Hot Encoding is useful for nominal categorical data.
* Ordinal Encoding is used when categories have a meaningful order.
* Label Encoding converts categories into integer labels.
* Proper preprocessing helps improve the performance of machine learning models.


