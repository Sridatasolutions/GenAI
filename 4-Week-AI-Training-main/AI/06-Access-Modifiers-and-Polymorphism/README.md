# Day 6 – Access Modifiers, Data Hiding, and Polymorphism

Today, I learned about access modifiers, data hiding, and polymorphism in Python. These concepts are important in Object-Oriented Programming as they help protect data, control access to class members, and allow the same interface to perform different tasks.

## Topics Learned

* Access Modifiers
* Data Hiding
* Private Variables
* Encapsulation Example (Bank Account)
* Polymorphism

1+1 =2
"srini" + "vas" 
---

## Access Modifiers

Access modifiers define the accessibility of variables and methods within a class.

Python provides three types of access modifiers:

* **Public** – Can be accessed from anywhere.
* **Protected (`_`)** – Intended to be accessed within the class and its subclasses.
* **Private (`__`)** – Can only be accessed within the class.

### Example

```python
class Student:
    name = "John"          # Public
    _course = "Python"     # Protected
    __marks = 95           # Private
```

---

## Data Hiding

Data hiding is the process of restricting direct access to the internal data of an object. It is achieved using private variables and public methods to access or modify the data.

### Example

```python
class BankAccount:

    def __init__(self):
        self.__balance = 1000

    def credit(self, amount):
        self.__balance += amount

    def withdraw(self, amount):
        self.__balance -= amount

    def check_balance(self):
        print("Balance:", self.__balance)


account = BankAccount()

account.credit(500)
account.withdraw(200)
account.check_balance()
```

---

## Polymorphism

Polymorphism allows different classes to use methods with the same name while providing their own implementation.

### Example

```python
class Dog:
    def sound(self):
        print("Dog barks")

class Cat:
    def sound(self):
        print("Cat meows")

dog = Dog()
cat = Cat()

dog.sound()
cat.sound()
```

---

## What I Learned Today

* Access modifiers help control the visibility of class members.
* Public members are accessible from anywhere.
* Protected members are intended for use within the class and its subclasses.
* Private members provide data hiding by restricting direct access.
* Data hiding improves security and protects object data.
* Polymorphism allows the same method name to behave differently for different objects.
