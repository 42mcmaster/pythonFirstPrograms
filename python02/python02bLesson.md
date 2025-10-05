# Lesson 2b: Strings and Variables

## Learning Objectives
By the end of this lesson, you will be able to:
- Create and use string literals with single and double quotes
- Use escape sequences in strings
- Concatenate strings using `+`
- Repeat strings using `*`
- Create and name variables following Python conventions
- Assign values to variables and use them in expressions

## What Are Strings?

A **string** is a sequence of characters (letters, numbers, symbols) used to represent text. Strings are one of the most common data types in programming because so much of computing involves working with text!

### Creating String Literals

In Python, you can create strings using either single quotes (`'`) or double quotes (`"`):

```python
name = 'Alice'
message = "Hello, World!"
```

Both work the same way! The choice is usually personal preference, but there's one important advantage to having both options:

```python
# Double quotes let you use single quotes (apostrophes) inside
sentence = "I'm learning Python!"

# Single quotes let you use double quotes inside
quote = 'She said, "Python is awesome!"'
```

### The Empty String

An empty string has no characters at all. Both of these create an empty string:

```python
empty1 = ''
empty2 = ""
```

This is useful when you need a placeholder or want to build up a string piece by piece.

## Multi-Line Strings

For longer text or documentation, use triple quotes (`"""` or `'''`):

```python
story = """This is a long story
that spans multiple lines.
Each line break is preserved
in the string!"""

print(story)
```

## Escape Sequences

Sometimes you need to include special characters in strings. **Escape sequences** start with a backslash (`\`) and represent special characters:

| Escape Sequence | What It Does |
|----------------|--------------|
| `\n` | New line (like pressing Enter) |
| `\t` | Tab (like pressing Tab) |
| `\\` | Actual backslash character |
| `\'` | Single quote |
| `\"` | Double quote |

### Examples:

```python
# Create a new line
print("First line\nSecond line")

# Create tabs for formatting
print("Name:\tAlice\nAge:\t15")

# Include quotes in strings
print("She said, \"Hello!\"")
print('It\'s a beautiful day!')
```

**Output:**
```
First line
Second line

Name:	Alice
Age:	15

She said, "Hello!"
It's a beautiful day!
```

## String Operations

### Concatenation (Joining Strings)

Use the `+` operator to join strings together:

```python
first = "Hello"
second = "World"
message = first + " " + second  # "Hello World"

greeting = "Hi, " + "Alice" + "!"  # "Hi, Alice!"
```

### Repetition

Use the `*` operator to repeat a string:

```python
laugh = "ha" * 3  # "hahaha"
line = "-" * 20   # "--------------------"
spaces = " " * 5  # "     " (5 spaces)
```

### Practical Example:

```python
# Create a simple text box
border = "*" * 30
message = "Welcome to Python!"

print(border)
print("*" + " " * 28 + "*")
print("*   " + message + "   *")
print("*" + " " * 28 + "*")
print(border)
```

## Variables

A **variable** is a name that refers to a value stored in the computer's memory. Think of it like a labeled box that holds information.

### Creating Variables

Use the assignment operator (`=`) to create a variable:

```python
age = 15
name = "Jordan"
gpa = 3.8
```

The variable name goes on the left, the value goes on the right.

### Variable Naming Rules

Python has strict rules for variable names:

1. **Must start with a letter or underscore** (`_`)
   - ✅ `name`, `_score`, `student1`
   - ❌ `1student`, `9total`

2. **Can contain letters, digits, and underscores**
   - ✅ `my_age`, `total_score`, `player_1`
   - ❌ `my-age`, `total score`, `player#1`

3. **Cannot use Python keywords**
   - ❌ `if`, `for`, `while`, `def`, `class`, `import`
   - ✅ `user_if`, `my_class`

4. **Are case-sensitive**
   - `Name`, `name`, and `NAME` are three different variables!

### Variable Naming Conventions

While not required, following these conventions makes your code easier to read:

1. **Use lowercase with underscores** for regular variables:
   ```python
   student_name = "Alex"
   final_score = 95
   ```

2. **Use UPPERCASE for constants** (values that never change):
   ```python
   TAX_RATE = 0.07
   MAX_STUDENTS = 30
   PI = 3.14159
   ```

3. **Use descriptive names:**
   ```python
   # ❌ Unclear
   x = 15
   y = "Smith"
   
   # ✅ Clear
   student_age = 15
   last_name = "Smith"
   ```

4. **Avoid single letters** (except in math or temporary uses):
   ```python
   # ❌ What does this mean?
   a = b + c
   
   # ✅ Much clearer!
   total_price = base_price + tax
   ```

## Using Variables

Once you create a variable, you can use it anywhere you'd use its value:

```python
name = "Taylor"
age = 16

# Use in print statements
print(name)
print(age)

# Use in calculations
next_year = age + 1

# Use in strings
message = "Hello, " + name + "!"
print(message)
```

### Variables Can Change

Variables can be reassigned to new values:

```python
score = 85
print(score)  # 85

score = 90
print(score)  # 90

score = score + 5  # Add 5 to current value
print(score)  # 95
```

## The Two Purposes of Variables

Variables serve two important purposes:

1. **Track data that changes over time**
   ```python
   score = 0
   score = score + 10  # Player scored!
   score = score + 25  # Player scored again!
   ```

2. **Give meaningful names to complex values (abstraction)**
   ```python
   # Instead of remembering 0.0875
   SALES_TAX_RATE = 0.0875
   
   # Now the code is self-documenting
   total = price * SALES_TAX_RATE
   ```

## Practical Example: Building a Mad Lib

```python
"""
Program: mad_lib.py
Author: Your Name
Creates a silly story using user input
"""

# Get words from the user
noun = input("Enter a noun: ")
verb = input("Enter a verb: ")
adjective = input("Enter an adjective: ")
place = input("Enter a place: ")

# Build the story
story = "Once upon a time, a " + adjective + " " + noun
story = story + " decided to " + verb + " at the " + place + "."

# Display the result
print("\n" + "=" * 40)
print("Your Silly Story:")
print("=" * 40)
print(story)
print("=" * 40)
```

## Summary

- Strings represent text data and are created with quotes
- Single quotes (`'`) and double quotes (`"`) both work
- Escape sequences like `\n` and `\t` create special characters
- Use `+` to concatenate (join) strings
- Use `*` to repeat strings
- Variables store values and have names that follow specific rules
- Good variable names make code easier to understand
- Variables can be reassigned to new values

## Key Terms

- **String** - A sequence of characters representing text
- **String Literal** - The way a string looks in code (in quotes)
- **Escape Sequence** - Special character combinations starting with `\`
- **Concatenation** - Joining strings together
- **Variable** - A named storage location for a value
- **Assignment** - Giving a value to a variable using `=`
- **Constant** - A variable whose value should not change (by convention, use UPPERCASE)

## Next Lesson Preview

Next, we'll learn about numeric data types (integers and floating-point numbers) and how to perform calculations with them!