# Day 3 – Loops and Functions

Today, I learned about loops and functions in Python. Loops help in executing a block of code repeatedly, while functions allow us to organize and reuse code efficiently.

## Topics Learned

* `for` Loop
* `while` Loop
* Functions in Python
* Functions without Parameters
* Functions with Parameters
* Functions with Default Parameters

---

## Loops

Loops are used to execute a set of statements multiple times without writing the same code repeatedly.

### `for` Loop

The `for` loop is used to iterate over a sequence or range of values.

**Example:**

```python
for i in range(1, 6):
    print(i)
```

### `while` Loop

The `while` loop executes as long as a specified condition remains true.

**Example:**

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

---

## Functions

Functions are reusable blocks of code designed to perform a specific task.

### Function without Parameters

These functions do not accept any input values.

**Example:**

```python
def greet():
    print("Hello!")

greet()
```

### Function with Parameters

These functions accept values when they are called.

**Example:**

```python
def greet(name):
    print("Hello,", name)

greet("John")
```

### Function with Default Parameters

Default parameters provide predefined values if no argument is passed.

**Example:**

```python
def greet(name="Guest"):
    print("Hello,", name)

greet()
greet("John")
```

---

## What I Learned Today

* Loops help automate repetitive tasks.
* `for` loops are useful when the number of iterations is known.
* `while` loops execute based on conditions.
* Functions improve code reusability and organization.
* Parameters make functions more flexible.
* Default parameters provide optional values and convenience.


