# Day 7 – Introduction to NumPy

Today, I learned about **NumPy**, one of the most popular Python libraries for numerical computing. NumPy provides a powerful N-dimensional array object and many built-in functions that make mathematical and scientific computations faster and more efficient.

## Topics Learned

- Why use NumPy?
- Advantages of NumPy
- Performance comparison: NumPy Arrays vs Python Lists
- Creating 1D, 2D, and 3D Arrays
- Vectorization
- Array Properties
- Data Types in NumPy
- Changing Data Types
- Reshaping Arrays
- Flattening Arrays
- Indexing
- Built-in Mathematical Functions

---

## Why Use NumPy?

NumPy is used for performing numerical computations efficiently. It provides high-performance arrays and a large collection of mathematical functions.

### Advantages of NumPy

- Faster execution than Python lists.
- Less memory consumption.
- Easy handling of multidimensional arrays.
- Supports vectorized operations.
- Provides many built-in mathematical functions.

---

## Performance Comparison

NumPy arrays perform operations much faster than Python lists because they are optimized and implemented in C.

---

## Creating NumPy Arrays

NumPy supports arrays of different dimensions.

### 1D Array

```python
import numpy as np

arr = np.array([1, 2, 3, 4])
```

### 2D Array

```python
arr = np.array([[1, 2], [3, 4]])
```

### 3D Array

```python
arr = np.array([
    [[1, 2], [3, 4]],
    [[5, 6], [7, 8]]
])
```

---

## Vectorization

Vectorization allows mathematical operations to be performed on an entire array without using loops.

### Example

```python
arr = np.array([1, 2, 3])

print(arr * 2)
```

---

## Array Properties

NumPy provides useful attributes to inspect arrays.

- `size` – Total number of elements.
- `shape` – Dimensions of the array.
- `ndim` – Number of dimensions.
- `dtype` – Data type of elements.

### Example

```python
arr = np.array([[1, 2], [3, 4]])

print(arr.size)
print(arr.shape)
print(arr.ndim)
print(arr.dtype)
```

---

## NumPy Data Types

Common NumPy data types include:

- `int32`
- `int64`
- `float32`
- `float64`
- `bool`
- `complex`
- `object`

---

## Changing Data Types

Data types can be changed using `dtype` while creating an array or by using the `astype()` method.

### Example

```python
arr = np.array([1, 2, 3])

new_arr = arr.astype(float)
```

---

## Reshaping Arrays

The `reshape()` method changes the dimensions of an array without changing its data.

### Example

```python
arr = np.array([1, 2, 3, 4])

new_arr = arr.reshape(2, 2)
```

---

## Flattening Arrays

The `flatten()` method converts a multidimensional array into a one-dimensional array.

### Example

```python
arr = np.array([[1, 2], [3, 4]])

flat = arr.flatten()
```

---

## Indexing

Indexing is used to access specific elements in an array.

### Example

```python
arr = np.array([10, 20, 30])

print(arr[1])
```

---

## Built-in Mathematical Functions

NumPy provides many mathematical functions for calculations.

Some commonly used functions are:

- `np.sum()`
- `np.mean()`
- `np.max()`
- `np.min()`
- `np.sqrt()`
- `np.sin()`
- `np.cos()`
- `np.log()`

### Example

```python
arr = np.array([1, 2, 3, 4])

print(np.sum(arr))
print(np.mean(arr))
```

---

## What I Learned Today

- NumPy provides efficient multidimensional arrays.
- It performs computations much faster than Python lists.
- Arrays can be created in one, two, or three dimensions.
- Vectorization eliminates the need for explicit loops in many operations.
- Array properties help understand the structure of data.
- Data types can be viewed and converted easily.
- Arrays can be reshaped and flattened as needed.
- NumPy includes many built-in mathematical functions for numerical computations.
