# 1. Object-Oriented Programming (OOP)

## What is OOP?

Object-Oriented Programming (OOP) is a programming paradigm that organizes code into **objects**, which combine **data (attributes)** and **behavior (methods)**.

The four main principles are:

1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction

---

## Encapsulation

Encapsulation means **bundling data and methods together** and restricting direct access to internal data.

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance

account = BankAccount(1000)
account.deposit(500)

print(account.get_balance())
```

**Benefits**

* Data protection
* Better security
* Easier maintenance

---

## Inheritance

Inheritance allows one class to inherit properties and methods from another class.

```python
class Animal:
    def sound(self):
        print("Animal makes sound")

class Dog(Animal):
    def bark(self):
        print("Dog barks")

dog = Dog()
dog.sound()
dog.bark()
```

**Benefits**

* Code reuse
* Reduced duplication

---

## Polymorphism

Same method behaves differently for different objects.

```python
class Dog:
    def speak(self):
        return "Bark"

class Cat:
    def speak(self):
        return "Meow"

animals = [Dog(), Cat()]

for animal in animals:
    print(animal.speak())
```

Output

```
Bark
Meow
```

---

## Abstraction

Hide implementation details and expose only essential functionality.

```python
from abc import ABC, abstractmethod

class Vehicle(ABC):

    @abstractmethod
    def start(self):
        pass

class Car(Vehicle):

    def start(self):
        print("Car Started")

car = Car()
car.start()
```

---

## Interview Answer

> OOP is a programming paradigm based on objects. It improves modularity, reusability, scalability, and maintainability through encapsulation, inheritance, polymorphism, and abstraction.

---

# 2. Decorators

## What is a Decorator?

A decorator is a function that **adds functionality to another function without modifying its original code**.

```python
def decorator(func):

    def wrapper():
        print("Before function")
        func()
        print("After function")

    return wrapper

@decorator
def greet():
    print("Hello")

greet()
```

Output

```
Before function
Hello
After function
```

---

## Uses

* Logging
* Authentication
* Authorization
* Timing execution
* Caching

Example

```python
import time

def timer(func):

    def wrapper():
        start = time.time()
        func()
        print("Execution Time:", time.time() - start)

    return wrapper
```

---

## Interview Answer

> Decorators are higher-order functions that wrap another function to extend or modify its behavior without changing the original function's source code.

---

# 3. Generators

## What is a Generator?

A generator is a function that returns values one at a time using the `yield` keyword instead of returning all values at once.

```python
def numbers():

    for i in range(5):
        yield i

for n in numbers():
    print(n)
```

Output

```
0
1
2
3
4
```

---

## Why use generators?

Without generator

```python
numbers = [i for i in range(10000000)]
```

Consumes a large amount of memory.

Generator

```python
def generate():

    for i in range(10000000):
        yield i
```

Produces values only when needed.

---

## Advantages

* Memory efficient
* Faster for large datasets
* Supports lazy evaluation

---

## Interview Answer

> A generator is a special function that uses `yield` to produce values lazily, making it memory efficient for processing large datasets.

---

# 4. Multithreading vs Multiprocessing

| Feature       | Multithreading | Multiprocessing |
| ------------- | -------------- | --------------- |
| Unit          | Threads        | Processes       |
| Memory        | Shared         | Separate        |
| GIL           | Affected       | Not affected    |
| Speed         | Best for I/O   | Best for CPU    |
| Communication | Easy           | More expensive  |

---

## Multithreading Example

```python
import threading
import time

def task():
    time.sleep(2)
    print("Done")

t1 = threading.Thread(target=task)
t2 = threading.Thread(target=task)

t1.start()
t2.start()
```

---

## Multiprocessing Example

```python
from multiprocessing import Process

def task():
    print("Working")

p1 = Process(target=task)
p2 = Process(target=task)

p1.start()
p2.start()
```

---

## Interview Answer

> Multithreading is ideal for I/O-bound tasks because threads share memory and can overlap waiting times. Multiprocessing is better for CPU-bound tasks because each process has its own Python interpreter and GIL, enabling true parallel execution.

---

# 5. GIL (Global Interpreter Lock)

The GIL is a lock in CPython that allows only one thread to execute Python bytecode at a time.

### Affected

* CPU-intensive tasks

### Not affected much

* I/O operations

---

## Why?

It simplifies memory management and ensures thread safety in CPython.

---

## Interview Answer

> The GIL allows only one thread to execute Python bytecode at a time. It limits multithreading performance for CPU-bound tasks but has little impact on I/O-bound tasks.

---

# 6. Exception Handling

Exceptions prevent a program from crashing unexpectedly.

```python
try:
    num = int(input("Enter number:"))
    print(10 / num)

except ZeroDivisionError:
    print("Cannot divide by zero")

except ValueError:
    print("Invalid number")

finally:
    print("Always executed")
```

---

## Custom Exception

```python
class AgeError(Exception):
    pass

age = 15

if age < 18:
    raise AgeError("Age must be at least 18")
```

---

## Interview Answer

> Exception handling uses `try`, `except`, `else`, and `finally` blocks to gracefully handle runtime errors and keep applications robust.

---

# 7. Context Managers

A context manager automatically manages resources such as files, database connections, or locks.

Instead of

```python
file = open("data.txt")

# work

file.close()
```

Use

```python
with open("data.txt") as file:
    print(file.read())
```

The file is automatically closed.

---

## Custom Context Manager

```python
class Demo:

    def __enter__(self):
        print("Start")
        return self

    def __exit__(self, exc_type, exc, tb):
        print("End")

with Demo():
    print("Working")
```

---

## Benefits

* Automatic cleanup
* Prevents resource leaks
* Cleaner code

---

## Interview Answer

> A context manager manages resources automatically using the `with` statement by implementing `__enter__()` and `__exit__()` methods.

---

# 8. List and Dictionary Comprehensions

## List Comprehension

Creates lists in a concise way.

Traditional

```python
numbers = []

for i in range(5):
    numbers.append(i * i)

print(numbers)
```

Comprehension

```python
numbers = [i * i for i in range(5)]

print(numbers)
```

Output

```
[0, 1, 4, 9, 16]
```

With condition

```python
evens = [i for i in range(10) if i % 2 == 0]

print(evens)
```

Output

```
[0, 2, 4, 6, 8]
```

---

## Dictionary Comprehension

Traditional

```python
square = {}

for i in range(5):
    square[i] = i * i

print(square)
```

Comprehension

```python
square = {i: i * i for i in range(5)}

print(square)
```

Output

```
{0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

With condition

```python
square = {i: i * i for i in range(10) if i % 2 == 0}

print(square)
```

Output

```
{0: 0, 2: 4, 4: 16, 6: 36, 8: 64}
```

---

# Quick Interview Summary

| Topic                          | One-line Interview Answer                                                                    |
| ------------------------------ | -------------------------------------------------------------------------------------------- |
| OOP                            | Organizes code into objects using encapsulation, inheritance, polymorphism, and abstraction. |
| Decorators                     | Functions that extend another function's behavior without modifying its code.                |
| Generators                     | Functions that use `yield` to produce values lazily, improving memory efficiency.            |
| Multithreading                 | Uses multiple threads; best for I/O-bound tasks.                                             |
| Multiprocessing                | Uses multiple processes; best for CPU-bound tasks and true parallelism.                      |
| GIL                            | A CPython mechanism that allows only one thread to execute Python bytecode at a time.        |
| Exception Handling             | Handles runtime errors gracefully using `try`, `except`, `else`, and `finally`.              |
| Context Managers               | Manage resources automatically using the `with` statement.                                   |
| List/Dictionary Comprehensions | Concise syntax for creating lists and dictionaries from iterables.                           |

These explanations are at the level typically expected in **Python interviews for 3–7 years of experience**, especially for backend, data engineering, AI/ML, and MLOps roles.
