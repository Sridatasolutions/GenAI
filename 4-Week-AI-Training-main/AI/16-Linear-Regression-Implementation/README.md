# Day 16 – Linear Regression Implementation

Today, I implemented **Simple Linear Regression** and **Multiple Linear Regression** using Scikit-learn. I also learned how to prepare datasets, train regression models, evaluate their performance, and make predictions using trained models.

## Topics Learned

* Simple Linear Regression
* Multiple Linear Regression
* Loading Datasets
* One-Hot Encoding
* Train-Test Split
* LinearRegression Model
* Model Evaluation
* Predictions
* Data Visualization

---

## Introduction to Linear Regression

Linear Regression is a supervised machine learning algorithm used to predict continuous numerical values.

There are two main types:

* **Simple Linear Regression** – Uses one independent variable.
* **Multiple Linear Regression** – Uses two or more independent variables.

---

# Simple Linear Regression

For Simple Linear Regression, I worked with the **Salary_dataset.csv** dataset.

The model predicts **Salary** based on **Years of Experience**.

---

## Visualizing the Dataset

A scatter plot was used to observe the relationship between years of experience and salary.

### Example

```python
sns.scatterplot(
    x="YearsExperience",
    y="Salary",
    data=df
)
```

---

## Splitting the Dataset

The dataset was divided into training and testing sets.

### Example

```python
x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.30, random_state=48
)
```

---

## Training the Model

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()

model.fit(x_train, y_train)
```

---

## Model Parameters

The trained model provides:

* **Slope (Coefficient)**

```python
model.coef_
```

* **Intercept**

```python
model.intercept_
```

---

## Evaluating the Model

The model performance was evaluated using the R² score.

### Example

```python
model.score(x_test, y_test)
```

---

## Predicting Salary

The trained model can predict salary for new values of experience.

### Example

```python
model.predict([[4.2]])
```

---

# Multiple Linear Regression

For Multiple Linear Regression, I worked with the **50_Startups.csv** dataset.

The dataset contains the following features:

* R&D Spend
* Administration
* Marketing Spend
* State
* Profit

Since the **State** column contains categorical values, it was converted into numerical form using **One-Hot Encoding**.

### Example

```python
from sklearn.preprocessing import OneHotEncoder

encoder = OneHotEncoder()

df["State"] = encoder.fit_transform(df[["State"]]).toarray()
```

---

## Visualizing the Dataset

A pair plot was used to understand relationships between different features.

### Example

```python
sns.pairplot(data=df)
```

---

## Splitting the Dataset

The dataset was divided into training and testing sets.

### Example

```python
x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.30, random_state=46
)
```

---

## Training the Model

```python
model = LinearRegression()

model.fit(x_train, y_train)
```

---

## Evaluating the Model

The model performance was evaluated using the R² score.

### Example

```python
model.score(x_test, y_test)
```

---

## Making Predictions

After training, the model was used to predict profit for new input values.

### Example

```python
model.predict([[93863.75, 127320.38, 249839.44, 1.0]])
```

---

## What I Learned Today

* Implemented both Simple and Multiple Linear Regression using Scikit-learn.
* Used One-Hot Encoding for categorical features.
* Split datasets into training and testing sets.
* Trained regression models using `LinearRegression`.
* Evaluated model performance using the R² score.
* Made predictions using trained models.
* Used scatter plots and pair plots to visualize data before training.
