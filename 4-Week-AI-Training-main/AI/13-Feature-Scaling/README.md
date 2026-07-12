# Day 13 – Feature Scaling

Today, I revised the different encoding techniques learned previously and studied **Feature Scaling**, an important preprocessing step in Machine Learning. Feature scaling ensures that numerical features are on a similar scale, which helps many machine learning algorithms perform more effectively.

## Topics Learned

* Revision of Encoding Techniques
* Introduction to Feature Scaling
* StandardScaler
* MinMaxScaler

---

## Revision of Encoding Techniques

Before learning feature scaling, I revised the three commonly used encoding techniques:

* **One-Hot Encoding** – Creates separate binary columns for each category.
* **Ordinal Encoding** – Converts ordered categorical values into numerical values.
* **Label Encoding** – Assigns a unique integer to each category.

---

## What is Feature Scaling?

Feature scaling is the process of transforming numerical features so that they have a similar range or distribution. It prevents features with larger values from dominating those with smaller values during model training.

### Why is Feature Scaling Important?

* Improves the performance of many machine learning algorithms.
* Speeds up model convergence.
* Prevents features with large values from dominating others.
* Produces more accurate and stable models.

---

## StandardScaler

StandardScaler standardizes data by transforming it so that it has:

* Mean = 0
* Standard Deviation = 1

### Formula

```text
z = (x - mean) / standard deviation
```

### Example

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

scaled_data = scaler.fit_transform(data[["Age", "Salary"]])
```

---

## MinMaxScaler

MinMaxScaler transforms data into a fixed range, usually between **0 and 1**.

### Formula

```text
x_scaled = (x - min) / (max - min)
```

### Example

```python
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()

scaled_data = scaler.fit_transform(data[["Age", "Salary"]])
```

---

## StandardScaler vs MinMaxScaler

| StandardScaler                         | MinMaxScaler                            |
| -------------------------------------- | --------------------------------------- |
| Mean becomes 0                         | Values are scaled between 0 and 1       |
| Standard deviation becomes 1           | Preserves the relative distribution     |
| Suitable for normally distributed data | Suitable when a fixed range is required |

---

## What I Learned Today

* Revised the three main encoding techniques used in Machine Learning.
* Learned the importance of feature scaling before model training.
* Understood how StandardScaler standardizes data.
* Learned how MinMaxScaler scales data to a fixed range.
* Understood the differences between StandardScaler and MinMaxScaler and when each can be used.
