# Day 11 – Seaborn and Machine Learning Pipeline Overview

Today, I learned about **Seaborn**, a Python library used for statistical data visualization, and received an overview of the **Machine Learning Pipeline**, which outlines the main stages involved in building and deploying a machine learning model.

## Topics Learned

* Introduction to Seaborn
* Installing and Importing Seaborn
* Line Plot
* Bar Plot
* Scatter Plot
* Box Plot
* Heatmap
* Overview of the Machine Learning Pipeline

---

## What is Seaborn?

Seaborn is a Python data visualization library built on top of Matplotlib. It provides a high-level interface for creating attractive and informative statistical graphics.

### Advantages of Seaborn

* Easy to create visually appealing plots.
* Built on top of Matplotlib.
* Integrates well with Pandas DataFrames.
* Useful for statistical data visualization.
* Provides built-in themes and color palettes.

---

## Installing Seaborn

```python
pip install seaborn
```

---

## Importing Seaborn

```python
import seaborn as sns
import matplotlib.pyplot as plt
```

---

## Line Plot

A line plot is used to visualize trends or changes over a continuous interval.

### Example

```python
sns.lineplot(x=[1, 2, 3], y=[2, 4, 6])
```

---

## Bar Plot

A bar plot compares values across different categories.

### Example

```python
sns.barplot(x=["A", "B", "C"], y=[10, 15, 8])
```

---

## Scatter Plot

A scatter plot shows the relationship between two numerical variables.

### Example

```python
sns.scatterplot(x=[1, 2, 3], y=[4, 6, 5])
```

---

## Box Plot

A box plot displays the distribution of data and helps identify outliers.

### Example

```python
sns.boxplot(y=[2, 4, 5, 6, 8, 12])
```

---

## Heatmap

A heatmap represents data values using different colors and is commonly used to visualize correlation matrices.

### Example

```python
import numpy as np

data = np.array([[1, 2], [3, 4]])

sns.heatmap(data, annot=True)
```

---

# Machine Learning Pipeline (Overview)

Today, I also received an introduction to the typical stages involved in building a Machine Learning project.

The pipeline generally consists of the following steps:

1. **Dataset Collection** – Gather the required data.
2. **Data Cleaning** – Handle missing values, duplicates, and inconsistencies.
3. **Data Transformation** – Prepare the data for analysis.
4. **Encoding** – Convert categorical data into numerical form.
5. **Feature Scaling** – Scale numerical features to a common range.
6. **Feature Selection** – Choose the most relevant features.
7. **Train-Test Split** – Divide the dataset into training and testing sets.
8. **Model Training** – Train a machine learning model.
9. **Model Testing** – Evaluate the model's performance.
10. **Model Deployment** – Deploy the trained model for real-world use.

> **Note:** This was only an introductory overview. Each step will be studied in greater detail in the upcoming training sessions.

---

## What I Learned Today

* Seaborn is a powerful library for creating statistical visualizations.
* It provides simple functions to create line plots, bar plots, scatter plots, box plots, and heatmaps.
* Seaborn works seamlessly with Pandas and Matplotlib.
* I also learned the overall workflow of a Machine Learning project, from collecting data to deploying a trained model.

