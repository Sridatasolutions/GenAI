# Day 15 – Outlier Detection and Regression Overview

Today, I learned about **outliers**, methods to detect them, how datasets are split for machine learning, and received an introductory overview of **Simple Linear Regression** and **Multiple Linear Regression**.

## Topics Learned

* Introduction to Outliers
* Detecting Outliers using Quartiles (IQR Method)
* Detecting Outliers using Z-Score
* Splitting Dataset into Training and Testing Sets
* Introduction to Simple Linear Regression
* Introduction to Multiple Linear Regression

---

## What are Outliers?

Outliers are data points that differ significantly from the rest of the observations in a dataset. They can affect statistical analysis and reduce the performance of machine learning models.

### Why Detect Outliers?

* Improve data quality.
* Increase model accuracy.
* Reduce the effect of unusual observations.
* Improve the reliability of analysis.

---

## Detecting Outliers using Quartiles (IQR Method)

The **Interquartile Range (IQR)** method identifies outliers using the first quartile (Q1) and third quartile (Q3).

### Formula

```text
IQR = Q3 - Q1

Lower Bound = Q1 - 1.5 × IQR
Upper Bound = Q3 + 1.5 × IQR
```

Any value outside these bounds is considered an outlier.

---

## Detecting Outliers using Z-Score

The **Z-Score** measures how far a data point is from the mean in terms of standard deviations.

### Formula

```text
Z = (X - Mean) / Standard Deviation
```

A value with a Z-Score greater than **3** or less than **-3** is generally considered an outlier.

---

## Splitting the Dataset

Before training a machine learning model, the dataset is divided into:

* **Training Set** – Used to train the model.
* **Testing Set** – Used to evaluate the model's performance on unseen data.

A commonly used split is **80% training** and **20% testing**, although other ratios such as **70:30** are also used depending on the dataset.

---

## Simple Linear Regression

Simple Linear Regression is a supervised machine learning algorithm used to predict a continuous value using **one independent variable** and **one dependent variable**.

### Example

Predicting a student's marks based on the number of hours studied.

---

## Multiple Linear Regression

Multiple Linear Regression predicts a continuous value using **two or more independent variables**.

### Example

Predicting a house price using features such as:

* Area
* Number of Bedrooms
* Location
* Age of the House

---

## What I Learned Today

* Outliers are unusual data points that may negatively affect machine learning models.
* The IQR method detects outliers using quartiles.
* The Z-Score method identifies outliers based on standard deviations from the mean.
* Splitting a dataset into training and testing sets is an important step before model training.
* Simple Linear Regression uses one input feature to make predictions.
* Multiple Linear Regression uses multiple input features for prediction.
* Today's session provided an overview of regression concepts; implementation will be covered in future sessions.
