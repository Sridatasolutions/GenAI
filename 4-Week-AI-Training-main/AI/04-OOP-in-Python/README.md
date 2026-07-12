# Day 4 – Object-Oriented Programming in Python

Today, I learned the fundamentals of Object-Oriented Programming (OOP) in Python. OOP helps in organizing code by creating classes and objects that represent real-world entities.

## Topics Learned

- Classes
- Objects
- Constructors
- Instance Variables
- Class Variables
- Instance Methods
- Class Methods
- Static Methods

---

## Class

A class is a blueprint for creating objects. It defines the attributes and behaviors that objects of the class will have.

### Example

```python
class Student:
    pass
```

---

## Object

An object is an instance of a class. Objects can access the attributes and methods defined in the class.

### Example

```python
student1 = Student()
```

---

## Constructor

A constructor is a special method (`__init__`) that is automatically called when an object is created. It is used to initialize object attributes.

### Example

```python
class Student:
    def __init__(self, name):
        self.name = name
```

---

## Instance Variable

Instance variables belong to a specific object. Each object can have its own values for these variables.

### Example

```python
class Student:
    def __init__(self, name):
        self.name = name
```

---

## Class Variable

Class variables are shared among all objects of a class.

### Example

```python
class Student:
    school = "ABC School"
```

---

## Instance Method

Instance methods operate on object-specific data and use the `self` parameter.

### Example

```python
class Student:
    def greet(self):
        print("Hello")
```

---

## Class Method

Class methods work with class-level data and use the `cls` parameter. They are defined using the `@classmethod` decorator.

### Example

```python
class Student:
    school = "ABC School"

    @classmethod
    def show_school(cls):
        print(cls.school)
```

---

## Static Method

Static methods do not depend on instance or class data. They are defined using the `@staticmethod` decorator.

### Example

```python
class Student:

    @staticmethod
    def welcome():
        print("Welcome")
```

---

## What I Learned Today

- A class acts as a blueprint for creating objects.
- Objects are instances of classes.
- Constructors initialize object data when an object is created.
- Instance variables store data specific to an object.
- Class variables are shared by all objects of a class.
- Instance methods work with object-specific data.
- Class methods work with class-level data.
- Static methods perform utility tasks and do not require object or class data.

