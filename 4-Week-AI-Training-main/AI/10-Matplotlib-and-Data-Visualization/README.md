# Day 10 – Matplotlib and Data Visualization

Today, I learned about **Data Visualization** and **Matplotlib**, one of the most popular Python libraries used to visualize data. Data visualization plays a vital role in Artificial Intelligence and Machine Learning by helping us understand datasets, identify trends, detect outliers, and communicate insights effectively.

## Topics Learned

* Importance of Data Visualization in AI & ML
* What is Data Visualization?
* Introduction to Matplotlib
* Installing and Importing Matplotlib
* Creating Line Plots
* Displaying Plots
* Adding Axis Labels
* Plotting Multiple Lines
* Using Legends
* Bar Chart
* Pie Chart
* Histogram
* Scatter Plot
* Box Plot

---

## Why is Data Visualization Important in AI & ML?

Data visualization helps in understanding data before building machine learning models. It allows us to:

* Identify patterns and trends.
* Detect outliers and anomalies.
* Understand data distribution.
* Compare different variables.
* Present results in a clear and meaningful way.

---

## What is Data Visualization?

Data visualization is the graphical representation of data using charts, graphs, and plots. It makes complex datasets easier to understand and analyze.

---

## What is Matplotlib?

Matplotlib is a Python library used for creating static, animated, and interactive visualizations. It provides a variety of charts and graphs for effective data analysis.

---

## Installing and Importing Matplotlib

### Install

```python
pip install matplotlib
```

### Import

```python
import matplotlib.pyplot as plt
```

---

## Line Plot

The `plot()` function is used to create line graphs.

### Example

```python
plt.plot([1, 2, 3], [2, 4, 6])
```

---

## Displaying a Plot

The `show()` function displays the graph.

### Example

```python
plt.show()
```

---

## Adding X and Y Labels

Axis labels make graphs more informative.

### Example

```python
plt.xlabel("X-Axis")
plt.ylabel("Y-Axis")
```

---

## Multiple Lines in One Plot

Multiple datasets can be displayed on the same graph.

### Example

```python
plt.plot([1, 2, 3], [2, 4, 6])
plt.plot([1, 2, 3], [1, 3, 5])
```

---

## Adding a Legend

Legends help identify different lines in a graph.

### Example

```python
plt.legend(["Line 1", "Line 2"])
```

---

## Bar Chart

Bar charts are used to compare values across categories.

### Example

```python
plt.bar(["A", "B", "C"], [10, 20, 15])
```

---

## Pie Chart

Pie charts show how each category contributes to the whole.

### Example

```python
plt.pie([40, 35, 25], labels=["A", "B", "C"])
```

---

## Histogram

Histograms display the distribution of numerical data.

### Example

```python
plt.hist([1, 2, 2, 3, 3, 3, 4])
```

---

## Scatter Plot

Scatter plots show the relationship between two variables.

### Example

```python
plt.scatter([1, 2, 3], [2, 5, 4])
```

---

## Box Plot

Box plots are useful for visualizing data distribution and detecting outliers.

### Example

```python
plt.boxplot([2, 4, 5, 6, 8, 10])
```

---

## What I Learned Today

* Data visualization is an essential step in AI and Machine Learning.
* Matplotlib provides powerful tools for creating different types of visualizations.
* Line plots, bar charts, pie charts, histograms, scatter plots, and box plots help represent data in different ways.
* Axis labels and legends improve the readability of graphs.
* Visualizing data makes it easier to identify patterns, trends, and outliers before performing analysis or training machine learning models.
