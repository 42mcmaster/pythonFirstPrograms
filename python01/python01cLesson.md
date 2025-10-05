# Lesson 1c: Interactive Shell Basics

## Learning Objectives
- Understand variables and assignment
- Use the Python shell for experimentation
- Understand basic data types (strings, integers, floats)
- Access Python documentation using help()

## Variables: Storing Information

A **variable** is a name that refers to a value stored in the computer's memory.

### Creating Variables (Assignment)

```python
>>> age = 16
>>> name = "Alex"
>>> pi = 3.14159
```

The `=` is the **assignment operator**. It stores the value on the right into the variable on the left.

**Important:** This is NOT the same as mathematical equality!

```python
>>> x = 5      # x now contains 5
>>> x = x + 1  # x now contains 6 (take old value, add 1, store back)
>>> x
6
```

### Using Variables

Once you create a variable, you can use it in expressions:

```python
>>> radius = 5
>>> area = 3.14 * radius ** 2
>>> area
78.5
```

### Viewing Variable Values

Type just the variable name to see its value:

```python
>>> name
'Alex'
>>> age
16
```

Or use `print()`:

```python
>>> print(name)
Alex
>>> print("My name is", name)
My name is Alex
```

## Data Types

Python has several built-in data types:

### 1. Integers (int)
Whole numbers: `5`, `-3`, `1000`, `0`

```python
>>> count = 42
>>> type(count)
<class 'int'>
```

### 2. Floating-Point Numbers (float)
Decimal numbers: `3.14`, `-0.5`, `2.0`

```python
>>> price = 19.99
>>> type(price)
<class 'float'>
```

### 3. Strings (str)
Text enclosed in quotes: `"hello"`, `'Python'`, `"123"`

```python
>>> message = "Hello, World!"
>>> type(message)
<class 'str'>
```

**Note:** Single quotes `'...'` and double quotes `"..."` both work!

## String Operations

### Concatenation (Joining Strings)

```python
>>> first = "Hello"
>>> second = "World"
>>> message = first + " " + second
>>> message
'Hello World'
```

### Repetition

```python
>>> "Ha" * 3
'HaHaHa'
>>> "=" * 20
'===================='
```

## The help() Function

Python has built-in documentation!

```python
>>> help(print)
# Shows documentation for the print function

>>> help(str)
# Shows documentation for strings
```

Press `q` to exit the help viewer.

## Common Errors to Watch For

### NameError
Using a variable before creating it:

```python
>>> print(age)
NameError: name 'age' is not defined
```

**Fix:** Create the variable first!

### TypeError
Mixing incompatible types:

```python
>>> "5" + 3
TypeError: can only concatenate str (not "int") to str
```

### SyntaxError
Missing quotes, parentheses, etc.:

```python
>>> print(Hello)
NameError: name 'Hello' is not defined

>>> print("Hello)
SyntaxError: EOL while scanning string literal
```

## Best Practices for Variable Names

**Good variable names:**
- `age`, `student_name`, `total_score`
- Descriptive and meaningful
- Use lowercase with underscores for spaces

**Bad variable names:**
- `a`, `x`, `data` (too vague)
- `studentName` (wrong style for Python)
- `2nd_score` (can't start with a number)

**Rules:**
- Must start with a letter or underscore
- Can contain letters, numbers, and underscores
- Cannot be a Python keyword (`if`, `while`, `for`, etc.)
- Case-sensitive: `name` and `Name` are different!

## Shell Tips

- **Up arrow**: Recall previous commands
- **Tab**: Auto-complete (try typing `pr` and press Tab)
- **Ctrl+C**: Cancel current operation
- **Ctrl+D**: Quit IDLE