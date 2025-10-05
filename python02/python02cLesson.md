# Lesson 2c: Numbers and Data Types

## Learning Objectives
By the end of this lesson, you will be able to:
- Distinguish between integers and floating-point numbers
- Understand what a data type is
- Use the `type()` function to check data types
- Work with ASCII character codes
- Convert between characters and their numeric codes

## What is a Data Type?

A **data type** defines what kind of value something is and what operations can be performed on it. Think of it like categories of things in real life - you can add numbers together, but you can't add a number to a word!

Python has several built-in data types:

| Type | Python Name | Example Values | What It Represents |
|------|-------------|----------------|-------------------|
| Integers | `int` | `-1, 0, 1, 42` | Whole numbers |
| Floating-point | `float` | `3.14, -0.5, 6.0` | Decimal numbers |
| Strings | `str` | `"Hi", 'A', "66"` | Text |

## Integers (`int`)

Integers represent whole numbers - numbers without decimal points.

```python
age = 15
temperature = -5
score = 100
year = 2024
```

### Integer Range

In many programming languages, integers have strict size limits. Python 3 is special - integers can be as large as your computer's memory allows!

```python
tiny = 1
small = 100
big = 1000000
huge = 123456789012345678901234567890  # Still works!
```

### Integer Literals

Write integers without commas:

```python
# ✅ Correct
population = 7800000000

# ❌ Wrong - Python will think these are separate values
population = 7,800,000,000
```

However, Python 3.6+ allows underscores for readability:

```python
# This works! The underscores are ignored
population = 7_800_000_000
big_number = 1_000_000
```

## Floating-Point Numbers (`float`)

Floating-point numbers (or "floats") represent real numbers - numbers with decimal points.

```python
pi = 3.14159
temperature = 98.6
price = 19.99
gpa = 3.85
```

### Float Range and Precision

Unlike integers, floats have limits:

- **Range:** Approximately -10³⁰⁸ to 10³⁰⁸
- **Precision:** About 16 significant digits

```python
very_small = 0.0000000001
very_large = 1.23e100  # 1.23 × 10¹⁰⁰
```

### Scientific Notation

For very large or very small numbers, use **scientific notation**:

```python
# Regular notation vs Scientific notation
speed_of_light = 299792458        # meters per second
speed_of_light = 2.99792458e8     # Same value!

atom_size = 0.0000000001          # meters
atom_size = 1e-10                 # Same value!
```

Format: `AeB` means A × 10ᴮ

| Decimal | Scientific | Meaning |
|---------|-----------|---------|
| 3.78 | 3.78e0 | 3.78 × 10⁰ |
| 37.8 | 3.78e1 | 3.78 × 10¹ |
| 3780.0 | 3.78e3 | 3.78 × 10³ |
| 0.378 | 3.78e-1 | 3.78 × 10⁻¹ |
| 0.00378 | 3.78e-3 | 3.78 × 10⁻³ |

## Checking Data Types

Use the `type()` function to check what type a value is:

```python
print(type(42))        # <class 'int'>
print(type(3.14))      # <class 'float'>
print(type("Hello"))   # <class 'str'>
```

This is useful when debugging:

```python
age = input("Enter your age: ")
print(type(age))  # <class 'str'> - Careful! Input always returns a string!
```

## Integer vs Float: An Important Difference

Look carefully at these numbers:

```python
num1 = 5    # This is an int
num2 = 5.0  # This is a float
```

They might seem the same, but to Python they're different types!

```python
print(5 == 5.0)      # True - same value
print(type(5))       # <class 'int'>
print(type(5.0))     # <class 'float'>
```

**Key point:** A number is a float if it has a decimal point, even if the decimal part is zero!

## Character Sets and ASCII

Computers store all data as numbers. This includes text! Each character has a number code.

### ASCII (American Standard Code for Information Interchange)

**ASCII** is a system that assigns a number to each character:

- `'A'` = 65
- `'B'` = 66
- `'a'` = 97
- `'b'` = 98
- `'0'` = 48
- `' '` (space) = 32

### Converting Characters and Numbers

Python provides two functions:

**`ord(char)`** - Get the ASCII code of a character:

```python
print(ord('A'))    # 65
print(ord('a'))    # 97
print(ord('0'))    # 48
print(ord(' '))    # 32
```

**`chr(number)`** - Get the character for an ASCII code:

```python
print(chr(65))     # 'A'
print(chr(97))     # 'a'
print(chr(48))     # '0'
print(chr(32))     # ' '
```

### Useful ASCII Facts

1. **Capital letters come before lowercase:**
   ```python
   print(ord('A'))  # 65
   print(ord('a'))  # 97
   ```

2. **Letters are in alphabetical order:**
   ```python
   print(ord('A'))  # 65
   print(ord('B'))  # 66
   print(ord('C'))  # 67
   ```

3. **Digits are in numerical order:**
   ```python
   print(ord('0'))  # 48
   print(ord('1'))  # 49
   print(ord('2'))  # 50
   ```

4. **The difference between uppercase and lowercase is always 32:**
   ```python
   print(ord('a') - ord('A'))  # 32
   print(ord('z') - ord('Z'))  # 32
   ```

## Practical Applications

### Example 1: Caesar Cipher (Simple Encryption)

```python
"""
Shift each letter forward by 1 in the alphabet
A -> B, B -> C, ... Z -> A
"""
letter = input("Enter a letter: ")
code = ord(letter)
new_code = code + 1
encrypted = chr(new_code)
print(f"{letter} encrypted is {encrypted}")
```

### Example 2: Checking Character Types

```python
char = input("Enter a character: ")
code = ord(char)

if 65 <= code <= 90:
    print("That's an uppercase letter!")
elif 97 <= code <= 122:
    print("That's a lowercase letter!")
elif 48 <= code <= 57:
    print("That's a digit!")
else:
    print("That's a special character!")
```

## When to Use Int vs Float

**Use `int` when:**
- Counting things (students, points, days)
- Representing whole units
- You need exact values (money in cents)

```python
num_students = 25
points_scored = 100
days_until_vacation = 14
```

**Use `float` when:**
- Dealing with measurements
- Doing division or scientific calculations
- Representing money in dollars (though be careful with precision!)

```python
temperature = 72.5
pi = 3.14159
price = 19.99
average_score = 87.3
```

## Common Mistakes

### Mistake 1: Using commas in numbers

```python
# ❌ Wrong
population = 7,800,000

# ✅ Correct
population = 7800000
# or
population = 7_800_000
```

### Mistake 2: Forgetting the decimal point

```python
# These are DIFFERENT!
half = 1/2      # float: 0.5
half = 1//2     # int: 0 (we'll learn about // next lesson)
```

### Mistake 3: Mixing up characters and strings

```python
# 'A' is not the same as "A"
print(ord('A'))     # Works! 65
print(ord("A"))     # Works! 65
print(ord("AB"))    # ERROR! ord() expects a single character
```

## Summary

- **Data types** define what kind of value something is
- **Integers** (`int`) are whole numbers with no limits in Python
- **Floats** (`float`) are decimal numbers with limited precision
- Use `type()` to check what type a value is
- Characters have numeric codes (ASCII values)
- Use `ord()` to convert character → number
- Use `chr()` to convert number → character
- Choose int or float based on what you're representing

## Key Terms

- **Data Type** - A category of values with specific operations
- **Integer** - Whole number (no decimal point)
- **Floating-Point Number** - Decimal number
- **Scientific Notation** - Compact way to write very large or small numbers
- **ASCII** - Standard system for encoding characters as numbers
- **Character Code** - The numeric value representing a character

## Next Lesson Preview

Next, we'll learn how to perform calculations using arithmetic operators like `+`, `-`, `*`, and `/`!