---
marp: true
theme: default
paginate: true
---

# Python Refresher 01
## Variables, Data Types, and Input/Output

**Medina County Career Center**
Instructor: Mr. McMaster

---

## Learning Objectives

By the end of this lesson, you will be able to:
- Create and use variables in Python
- Identify different data types (strings, integers, floats)
- Use `print()` to display output
- Use `input()` to get user input
- Convert between data types

---

## What is a Variable?

A **variable** is a container that stores data.

Think of it like a labeled box:
- The label is the variable **name**
- What's inside is the **value**

```python
age = 16
name = "Ryan"
price = 19.99
```

---

## Variable Naming Rules

✅ **DO:**
- Start with a letter or underscore
- Use letters, numbers, underscores
- Use descriptive names

```python
student_name = "Alex"
total_score = 95
_private = True
```

---

## Variable Naming Rules

❌ **DON'T:**
- Start with a number
- Use spaces
- Use special characters (@, #, !, etc.)
- Use Python keywords (if, else, for, etc.)

```python
2cool = "bad"        # Error!
my name = "bad"      # Error!
class = "bad"        # Error!
```

---

## Data Types: Strings

**Strings** are text data enclosed in quotes.

```python
# Single or double quotes both work
name = "Alice"
school = 'Medina Career Center'

# Can contain letters, numbers, symbols
message = "Hello! I am 16 years old."
```

---

## Data Types: Integers

**Integers** are whole numbers (no decimal points).

```python
age = 17
year = 2024
temperature = -5
score = 0
```

Can be positive, negative, or zero.

---

## Data Types: Floats

**Floats** are numbers with decimal points.

```python
price = 19.99
temperature = 98.6
gpa = 3.75
pi = 3.14159
```

Used for precise measurements and calculations.

---

## Checking Data Types

Use the `type()` function:

```python
age = 17
print(type(age))        # <class 'int'>

price = 19.99
print(type(price))      # <class 'float'>

name = "Sam"
print(type(name))       # <class 'str'>
```

---

## The print() Function

`print()` displays output to the screen.

```python
print("Hello, World!")
print(42)
print(3.14)
```

**Output:**
```
Hello, World!
42
3.14
```

---

## Printing Variables

You can print variables directly:

```python
name = "Taylor"
age = 16

print(name)
print(age)
```

**Output:**
```
Taylor
16
```

---

## Printing Multiple Items

Separate items with commas:

```python
name = "Jordan"
age = 17

print("Name:", name)
print("Age:", age)
```

**Output:**
```
Name: Jordan
Age: 17
```

---

## The input() Function

`input()` gets text from the user.

```python
name = input("What is your name? ")
print("Hello,", name)
```

**Important:** `input()` always returns a **string**!

---

## Getting User Input

```python
# This creates a prompt for the user
favorite_color = input("What is your favorite color? ")

# Display what they entered
print("Your favorite color is", favorite_color)
```

---

## Type Conversion

**Problem:** `input()` returns strings, but we often need numbers.

```python
age = input("How old are you? ")
# age is a STRING like "17", not a number!

print(age + 1)  # ERROR!
```

---

## Converting Strings to Integers

Use `int()` to convert:

```python
age = input("How old are you? ")
age = int(age)  # Convert string to integer

print("Next year you will be", age + 1)
```

---

## Converting Strings to Floats

Use `float()` to convert:

```python
price = input("Enter the price: ")
price = float(price)  # Convert string to float

tax = price * 0.07
print("Tax:", tax)
```

---

## Shortcut: Convert Immediately

```python
# Instead of two lines:
age = input("How old are you? ")
age = int(age)

# Do it in one line:
age = int(input("How old are you? "))
```

---

## Converting Numbers to Strings

Use `str()` to convert:

```python
score = 95
message = "Your score is " + str(score)
print(message)

# OR just use commas in print():
print("Your score is", score)
```

---

## Common Type Conversions

| Function | Purpose | Example |
|----------|---------|---------|
| `int()` | Convert to integer | `int("42")` → `42` |
| `float()` | Convert to float | `float("3.14")` → `3.14` |
| `str()` | Convert to string | `str(42)` → `"42"` |

---

## Practice Example

```python
# Get user's name
name = input("What is your name? ")

# Get user's age as an integer
age = int(input("How old are you? "))

# Calculate birth year (approximately)
birth_year = 2024 - age

# Display results
print("Hello,", name)
print("You were born around", birth_year)
```

---

## Common Mistakes

**Mistake 1:** Forgetting to convert input
```python
age = input("Age: ")
print(age + 1)  # ERROR! Can't add string and number
```

**Fix:**
```python
age = int(input("Age: "))
print(age + 1)  # Works!
```

---

## Common Mistakes

**Mistake 2:** Using quotes on variable names
```python
name = "Sam"
print("name")  # Prints: name
```

**Fix:**
```python
name = "Sam"
print(name)    # Prints: Sam
```

---

## Common Mistakes

**Mistake 3:** Mismatched data types
```python
age = 17
message = "You are " + age  # ERROR!
```

**Fix:**
```python
age = 17
message = "You are " + str(age)
# OR
print("You are", age)
```

---

## Lesson Summary

✓ Variables store data
✓ Three main data types: strings, integers, floats
✓ `print()` displays output
✓ `input()` gets user input (always returns a string)
✓ Convert data types with `int()`, `float()`, `str()`

---

## Task Time!

Open **python_refresher_01_task.py**

Complete the practice problems to reinforce what you learned today.

**Remember:**
- Test your code frequently
- Read error messages carefully
- Ask for help if you're stuck!
