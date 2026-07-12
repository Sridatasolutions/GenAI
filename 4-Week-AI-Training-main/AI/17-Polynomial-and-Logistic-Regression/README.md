# Day 17 – Polynomial Regression and Logistic Regression

Today, I learned about **Polynomial Regression** and **Logistic Regression**, two important machine learning algorithms. I implemented both models using Scikit-learn and learned how they are used for different types of machine learning problems.

## Topics Learned

* Introduction to Polynomial Regression
* Polynomial Features
* Training a Polynomial Regression Model
* Model Evaluation
* Introduction to Logistic Regression
* Binary Classification
* StandardScaler
* Model Training
* Model Prediction
* Accuracy Evaluation

---

# Polynomial Regression

## What is Polynomial Regression?

Polynomial Regression is an extension of Linear Regression that models the relationship between variables using polynomial terms. It is useful when the relationship between the input and output is not linear.

### Why Use Polynomial Regression?

* Captures non-linear relationships.
* Provides better fitting for curved data.
* Uses polynomial features to improve predictions.

---

## Polynomial Features

Scikit-learn provides the `PolynomialFeatures` class to generate polynomial combinations of input features.

### Example

```python
from sklearn.preprocessing import PolynomialFeatures

pf = PolynomialFeatures(degree=2)

x_poly = pf.fit_transform(x)
```

---

## Splitting the Dataset

The dataset is divided into training and testing sets before training the model.

### Example

```python
from sklearn.model_selection import train_test_split

x_train, x_test, y_train, y_test = train_test_split(
    x_poly,
    y,
    test_size=0.30,
    random_state=42
)
```

---

## Training the Model

Polynomial Regression is implemented by applying Linear Regression on the transformed polynomial features.

### Example

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()

model.fit(x_train, y_train)
```

---

## Evaluating the Model

The model performance can be evaluated using the R² score.

### Example

```python
model.score(x_test, y_test)
```

---

## Making Predictions

After training, the model can predict values for new input data.

### Example

```python
test = pf.transform([[25000]])

model.predict(test)
```

---

# Logistic Regression

## What is Logistic Regression?

Logistic Regression is a supervised machine learning algorithm used for **classification problems**. It predicts categorical outcomes, such as **Yes/No**, **True/False**, or **Disease/No Disease**.

---

## Binary Classification

In today's example, Logistic Regression was used to predict whether a patient has heart disease based on medical information.

---

## Feature Scaling

Before training the Logistic Regression model, numerical features were standardized using **StandardScaler**.

### Example

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)
```

---

## Training the Logistic Regression Model

### Example

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression(max_iter=1000)

model.fit(X_train, y_train)
```

---

## Making Predictions

The trained model predicts the class labels for new data.

### Example

```python
y_pred = model.predict(X_test)
```

A prediction can also be made for a new patient.

```python
new_patient = scaler.transform([[52,1,0,125,212,0,1,168,0,1.0,2,2,3]])

prediction = model.predict(new_patient)
```

---

## Evaluating the Model

The accuracy of the classification model is measured using the **Accuracy Score**.

### Example

```python
from sklearn.metrics import accuracy_score

accuracy = accuracy_score(y_test, y_pred)
```

---

## Difference Between Polynomial Regression and Logistic Regression

| Polynomial Regression            | Logistic Regression                       |
| -------------------------------- | ----------------------------------------- |
| Used for regression problems     | Used for classification problems          |
| Predicts continuous values       | Predicts categorical values               |
| Handles non-linear relationships | Predicts class labels using probabilities |

---

## What I Learned Today

* Learned the concept of Polynomial Regression and how it models non-linear relationships.
* Used `PolynomialFeatures` to create polynomial input features.
* Trained and evaluated a Polynomial Regression model.
* Learned that Logistic Regression is used for classification problems.
* Used `StandardScaler` before training the Logistic Regression model.
* Evaluated the classification model using the Accuracy Score.
* Made predictions for both testing data and new input values.
