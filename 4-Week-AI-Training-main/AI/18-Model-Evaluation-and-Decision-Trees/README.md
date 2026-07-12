# Day 18 – Model Evaluation and Decision Trees

Today, I learned how to evaluate Machine Learning models using different performance metrics. I also studied **Decision Trees** for both classification and regression problems, including **pre-pruning**, **post-pruning**, and tree visualization.

## Topics Learned

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* Confusion Matrix
* Accuracy
* Precision
* Recall
* Decision Tree Classifier
* Decision Tree Regressor
* Pre-Pruning
* Post-Pruning
* Tree Visualization

---

# Model Evaluation Metrics

Machine Learning models must be evaluated to determine how well they perform on unseen data.

---

## Mean Absolute Error (MAE)

MAE calculates the average absolute difference between actual and predicted values.

### Formula

```text
MAE = (1/n) Σ |Actual − Predicted|
```

A smaller MAE indicates better model performance.

---

## Mean Squared Error (MSE)

MSE calculates the average of the squared differences between actual and predicted values.

### Formula

```text
MSE = (1/n) Σ (Actual − Predicted)²
```

Larger errors receive greater penalties because the differences are squared.

---

## Root Mean Squared Error (RMSE)

RMSE is the square root of MSE and is expressed in the same unit as the target variable.

### Formula

```text
RMSE = √MSE
```

It is one of the most commonly used metrics for regression problems.

---

# Classification Metrics

## Confusion Matrix

A Confusion Matrix summarizes the predictions of a classification model by comparing predicted values with actual values.

It contains:

* True Positive (TP)
* True Negative (TN)
* False Positive (FP)
* False Negative (FN)

### Example

```python
from sklearn.metrics import confusion_matrix

cm = confusion_matrix(y_test, y_pred)
```

---

## Accuracy

Accuracy represents the percentage of correctly classified instances.

### Formula

```text
Accuracy = (TP + TN) / (TP + TN + FP + FN)
```

---

## Precision

Precision measures how many positive predictions are actually correct.

### Formula

```text
Precision = TP / (TP + FP)
```

---

## Recall

Recall measures how many actual positive cases are correctly identified.

### Formula

```text
Recall = TP / (TP + FN)
```

---

# Decision Tree

A Decision Tree is a supervised machine learning algorithm that makes predictions by splitting data into smaller subsets based on feature values.

Decision Trees can be used for both:

* Classification
* Regression

---

# Decision Tree Classifier

A Decision Tree Classifier predicts categorical outputs.

### Training the Model

```python
from sklearn.tree import DecisionTreeClassifier

dt = DecisionTreeClassifier()

dt.fit(x_train, y_train)
```

---

## Making Predictions

```python
dt.predict([[-1.781797, -1.490046]])
```

---

## Visualizing the Decision Tree

```python
from sklearn.tree import plot_tree

plot_tree(dt)
```

---

# Pre-Pruning

Pre-pruning limits the growth of a Decision Tree before it becomes too complex.

One commonly used parameter is `max_depth`.

### Example

```python
dt = DecisionTreeClassifier(max_depth=5)
```

Benefits include:

* Reduces overfitting.
* Produces a simpler model.
* Improves generalization.

---

# Post-Pruning

Post-pruning evaluates trees of different depths and selects the one with the best performance.

### Example

```python
for depth in range(1, 20):
    model = DecisionTreeClassifier(max_depth=depth)
```

---

# Decision Tree Regressor

Decision Tree Regressor predicts continuous numerical values.

### Example

```python
from sklearn.tree import DecisionTreeRegressor

dtr = DecisionTreeRegressor()

dtr.fit(x_train, y_train)
```

---

## Visualizing the Regression Tree

```python
plot_tree(dtr)
```

---

## What I Learned Today

* Learned the most commonly used regression evaluation metrics: MAE, MSE, and RMSE.
* Understood how a Confusion Matrix evaluates classification models.
* Learned the concepts of Accuracy, Precision, and Recall.
* Implemented a Decision Tree Classifier using Scikit-learn.
* Visualized the decision tree using `plot_tree()`.
* Learned the difference between pre-pruning and post-pruning.
* Implemented a Decision Tree Regressor for predicting continuous values.
    