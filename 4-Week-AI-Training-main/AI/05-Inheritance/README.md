# Day 5 – Inheritance in Python

Today, I learned about **Inheritance**, one of the fundamental concepts of Object-Oriented Programming (OOP). Inheritance allows a class to acquire the properties and methods of another class, promoting code reusability and making programs easier to maintain.

## Topics Learned

* Introduction to Inheritance
* Single Inheritance
* Multiple Inheritance
* Multilevel Inheritance
* Hierarchical Inheritance
* Hybrid Inheritance

---

## What is Inheritance?

Inheritance is a mechanism in Python where one class (called the **child class**) inherits the attributes and methods of another class (called the **parent class**).

### Advantages of Inheritance

* Promotes code reusability.
* Reduces code duplication.
* Makes code easier to maintain.
* Supports the concept of hierarchical relationships.

---

## 1. Single Inheritance

In Single Inheritance, one child class inherits from one parent class.

### Example

```python
class Animal:
    def sound(self):
        print("Animals make sounds")

class Dog(Animal):
    def bark(self):
        print("Dog barks")

dog = Dog()
dog.sound()
dog.bark()
```

---

## 2. Multiple Inheritance

In Multiple Inheritance, one child class inherits from more than one parent class.

### Example

```python
class Father:
    def skill1(self):
        print("Playing Cricket")

class Mother:
    def skill2(self):
        print("Cooking")

class Child(Father, Mother):
    pass

child = Child()
child.skill1()
child.skill2()
```

---

## 3. Multilevel Inheritance

In Multilevel Inheritance, a class inherits from another derived class.

### Example

```python
class Grandparent:
    def house(self):
        print("Grandparent's House")

class Parent(Grandparent):
    def car(self):
        print("Parent's Car")

class Child(Parent):
    def bike(self):
        print("Child's Bike")

child = Child()
child.house()
child.car()
child.bike()
```

---

## 4. Hierarchical Inheritance

In Hierarchical Inheritance, multiple child classes inherit from a single parent class.

### Example

```python
class Animal:
    def eat(self):
        print("Eating")

class Dog(Animal):
    def bark(self):
        print("Barking")

class Cat(Animal):
    def meow(self):
        print("Meowing")

dog = Dog()
dog.eat()
dog.bark()

cat = Cat()
cat.eat()
cat.meow()
```

---

## 5. Hybrid Inheritance

Hybrid Inheritance is a combination of two or more types of inheritance.

### Example

```python
class A:
    def displayA(self):
        print("Class A")

class B(A):
    def displayB(self):
        print("Class B")

class C(A):
    def displayC(self):
        print("Class C")

class D(B, C):
    def displayD(self):
        print("Class D")

obj = D()
obj.displayA()
obj.displayB()
obj.displayC()
obj.displayD()
```

---

## What I Learned Today

* Inheritance allows one class to reuse the properties and methods of another class.
* It helps reduce code duplication and improves code organization.
* Python supports five major types of inheritance:

  * Single Inheritance
  * Multiple Inheritance
  * Multilevel Inheritance
  * Hierarchical Inheritance
  * Hybrid Inheritance
