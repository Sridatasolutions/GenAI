# Day 14 – FunctionTransformer and Feature Selection

Today, I learned about **FunctionTransformer** and **Feature Selection**, two important concepts in data preprocessing and machine learning. FunctionTransformer allows us to apply custom transformations to data, while Feature Selection helps choose the most relevant features for building efficient machine learning models.

## Topics Learned

* FunctionTransformer
* Custom Data Transformations
* Feature Selection
* Importance of Feature Selection
* Examples of Feature Selection

---

## What is FunctionTransformer?

`FunctionTransformer` is a preprocessing tool provided by Scikit-learn that allows us to apply a custom Python function to data while keeping it compatible with machine learning pipelines.

### Why Use FunctionTransformer?

* Applies custom transformations easily.
* Integrates with Scikit-learn pipelines.
* Reduces repetitive preprocessing code.
* Improves code reusability.

### Example

```python
from sklearn.preprocessing import FunctionTransformer
import numpy as np

transformer = FunctionTransformer(np.log1p)

data = [[1], [5], [10]]

transformed_data = transformer.transform(data)
```

---

## Feature Selection

Feature Selection is the process of selecting the most relevant features (columns) from a dataset for training a machine learning model.

Removing unnecessary features helps improve model performance and reduces training time.

### Advantages of Feature Selection

* Reduces overfitting.
* Improves model accuracy.
* Decreases training time.
* Simplifies machine learning models.
* Removes irrelevant or redundant features.

---

## Example of Feature Selection

Suppose a dataset contains the following columns:

* Age
* Salary
* City
* Name
* Employee ID

If the goal is to predict salary, columns like **Name** and **Employee ID** may not contribute significantly to the prediction. Feature selection helps identify and remove such unnecessary features.

---

## Simple Example Using Scikit-learn

```python
from sklearn.feature_selection import SelectKBest
from sklearn.feature_selection import f_classif

selector = SelectKBest(score_func=f_classif, k=2)

X_new = selector.fit_transform(X, y)
```

---

## What I Learned Today

* FunctionTransformer allows custom preprocessing functions to be applied to datasets.
* It integrates seamlessly with Scikit-learn workflows.
* Feature Selection helps identify the most useful features for a machine learning model.
* Removing unnecessary features can improve accuracy and reduce computation time.
* Feature selection is an important preprocessing step before model training.

