# Core Python Notes

---

# Core Python

## 1. Basics & Control Flow

* Data types
* Variables
* Input & Output
* Operators
* Conditional statements
* Loops
* `break`, `continue`, `pass`

## 2. Data Structures

* Strings
* Lists
* Tuples
* Sets
* Dictionaries

## 3. Functions

* Functions
* Lambda functions
* Generators
* Decorators

## 4. OOPS

* Class
* Objects
* Inheritance
* Polymorphism
* Encapsulation
* Abstraction

## 5. Practical Python

* File handling
* Exception handling
* Logging
* Modules & Packages

## 6. Concurrency

* Multithreading
* Multiprocessing

---

# Data Types, Variables, Input & Output

---

# Data Types

## Primitive Data Types

* `int`
* `str`
* `float`
* `bool`

## Collection Data Types

* `list`
* `tuple`
* `dictionary`
* `set`

---

# Variables

A variable is:

```text
A name used to store data that can change during program execution.
```

Python does not require datatype declaration.

Example:

```python
x = 10
name = "Pavani"
```

---

# Global Variable

Use the `global` keyword to modify global variables inside functions.

```python
x = 10

def update_global():
    global x
    x = 20

update_global()
print(x)
```

Output:

```text
20
```

---

# Variable Naming Rules

1. Allowed:

   * letters (`a-z`, `A-Z`)
   * numbers (`0-9`)
   * underscore (`_`)

2. Variable cannot start with a number.

3. Variable names are case-sensitive.

4. Python keywords cannot be used.

---

# Naming Styles

## camelCase

```python
studentName
```

## PascalCase

```python
StudentName
```

## snake_case (Preferred in Python)

```python
student_name
```

---

# Input

## Static Input

### Multiple Values to Multiple Variables

```python
a, b, c = 1, "hero", "Ram Charan"
```

### Single Value to Multiple Variables

```python
a = b = c = 1
```

---

## Dynamic Input

```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))
height = float(input("Enter your height: "))
```

---

# Output

```python
print(f"Name: {name}\nAge: {age}\nHeight: {height}")
```

---

# Operators

---

# Arithmetic Operators

```python
+  -  *  /  //  %  **
```

Example:

```python
print(2 ** 3)
```

Output:

```text
8
```

---

# Bitwise Operators

```python
&  |  ^  ~  <<  >>
```

---

# Comparison Operators

```python
==  !=  >  <  >=  <=
```

---

# Logical Operators

```python
and  or  not
```

---

# Membership Operators

```python
in
not in
```

Example:

```python
print(2 in [1,2,3])
```

Output:

```text
True
```

---

# Quantifiers

## all()

```python
nums = [1,1,1]
print(all(n == 1 for n in nums))
```

## any()

```python
nums = [0,0,1]
print(any(n == 1 for n in nums))
```

---

# Conditional Statements

## Standard Format

```python
if condition1:
    print("Statement")
elif condition2:
    print("Statement")
else:
    print("Statement")
```

---

## Single-Line Format

```python
if condition:
    print("Statement")
```

---

## Short-Hand If Else

```python
result = "Positive" if number > 0 else "Non-positive"
```

---

# Iterative Statements

Python supports:

* `for`
* `while`

---

# Index-Based Iteration

```python
numbers = [1,2,3]

for i in range(len(numbers)):
    print(i, numbers[i])
```

---

# Element-Based Iteration

```python
for value in numbers:
    print(value)
```

---

# enumerate()

```python
for i, value in enumerate(numbers):
    print(i, value)
```

---

# while Loop

```python
i = 0

while i < len(numbers):
    print(i, numbers[i])
    i += 1
```

---

# break, continue, pass

```python
for i in range(5):

    if i == 1:
        break

    if i == 2:
        continue

    if i == 3:
        pass
```

## break

```text
Stops the entire loop immediately.
```

## continue

```text
Skips current iteration.
```

## pass

```text
Placeholder for future code.
```

---

# String Functions

---

# ASCII Functions

## ord()

```python
print(ord('a'))
```

Output:

```text
97
```

## chr()

```python
print(chr(97))
```

Output:

```text
a
```

---

# String Manipulation

## strip()

```python
print("  hello  ".strip())
```

## replace()

```python
print("hello world".replace("world", "Python"))
```

## lower()

```python
print("HELLO".lower())
```

## upper()

```python
print("hello".upper())
```

## split()

```python
print("hello world".split())
```

---

# String Checks

## isalpha()

```python
print("abc".isalpha())
```

## isdigit()

```python
print("123".isdigit())
```

## isnumeric()

```python
print("123".isnumeric())
```

## isalnum()

```python
print("abc123".isalnum())
```

---

# Numerical Functions

---

# Absolute & Rounding

## abs()

```python
print(abs(-7))
```

## round()

```python
print(round(3.1415, 2))
```

---

# Power Functions

## math.sqrt()

```python
import math
print(math.sqrt(25))
```

## pow()

```python
print(pow(2,3))
```

## Modular Power

```python
print(pow(2,3,5))
```

---

# Aggregate Functions

## min()

```python
print(min([1,2,3]))
```

## max()

```python
print(max([1,2,3]))
```

## sum()

```python
print(sum([1,2,3]))
```

---

# Data Structures

---

| Data Structure | Ordered        | Mutable | Duplicates  |
| -------------- | -------------- | ------- | ----------- |
| String         | Yes            | No      | Yes         |
| List           | Yes            | Yes     | Yes         |
| Tuple          | Yes            | No      | Yes         |
| Set            | No             | Yes     | No          |
| Dictionary     | Inserted Order | Yes     | Keys Unique |

---

# List

## Initialization

```python
lst = []
lst = [0] * 5
```

---

# Insert Operations

## append()

```python
lst.append(10)
```

## insert()

```python
lst.insert(0, 5)
```

## extend()

```python
lst.extend([1,2,3])
```

---

# Delete Operations

## pop()

```python
lst.pop()
```

## clear()

```python
lst.clear()
```

---

# Sorting

## sort()

```python
lst.sort()
```

## sorted()

```python
new_list = sorted(lst)
```

---

# Reverse

```python
lst.reverse()
```

```python
lst[::-1]
```

---

# List Comprehension

```python
squares = [x**2 for x in range(5)]
```

---

# Set

## Initialization

```python
s = set()
```

---

# Insert

```python
s.add(10)
```

```python
s.update([1,2,3])
```

---

# Set Operations

## Union

```python
A | B
```

## Intersection

```python
A & B
```

## Difference

```python
A - B
```

## Symmetric Difference

```python
A ^ B
```

---

# Tuple

## Initialization

```python
t = ()
```

---

# Tuple Packing & Unpacking

```python
t = 1,2,3
```

```python
a,b,c = t
```

---

# Dictionary

## Initialization

```python
d = {}
```

---

# Insert & Update

```python
d["a"] = 1
```

```python
d.update({"b":2})
```

---

# Delete

## pop()

```python
d.pop("a")
```

## clear()

```python
d.clear()
```

---

# Accessing Dictionary

## keys()

```python
for key in d.keys():
    print(key)
```

## values()

```python
for value in d.values():
    print(value)
```

## items()

```python
for key, value in d.items():
    print(key, value)
```

---

# Searching in Dictionary

```python
print("a" in d)
```

```python
print(2 in d.values())
```

---

# Interview Questions

## Difference between list and tuple?

### List

* Mutable
* Uses `[]`

### Tuple

* Immutable
* Uses `()`

---

## Difference between sort() and sorted()?

### sort()

* modifies existing list
* returns `None`

### sorted()

* returns new sorted list
* original list unchanged

---

## Difference between set and dictionary?

### Set

* stores unique values

### Dictionary

* stores key-value pairs

---

## Why are sets faster for searching?

Because sets use:

```text
Hashing
```

which provides near:

```text
O(1)
```

average lookup time.
