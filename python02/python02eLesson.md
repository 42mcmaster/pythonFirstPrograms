# Lesson 2e: Type Conversions and Input

## Learning Objectives
By the end of this lesson, you will be able to:
- Convert between different data types using type conversion functions
- Get user input with the `input()` function
- Convert user input to numbers for calculations
- Understand when and why type conversion is necessary
- Handle mixed-mode arithmetic properly

## The Problem: Input Returns Strings

When you ask users for input, Python ALWAYS gives you back a string, even if they type a number:

```python
age = input("Enter your age: ")
print(type(age))  # <class 'str'>

# This won't work as expected!
next_year = age + 1  # TypeError: can only concatenate str to str
```

The `input()` function returns a **string** (text), not a number. To do math, we need to convert it first!

## Type Conversion Functions

Python provides functions to convert between types:

| Function | What It Does | Example |
|----------|-------------|---------|
| `int()` | Converts to integer | `int("42")` → `42` |
| `float()` | Converts to float | `float("3.14")` → `3.14` |
| `str()` | Converts to string | `str(42)` → `"42"` |

## Converting Strings to Numbers

### int() Function

Converts a string to an integer:

```python
age_str = "15"
age_num = int(age_str)  # "15" → 15

print(type(age_str))    # <class 'str'>
print(type(age_num))    # <class 'int'>
```

**Important:** The string must contain a valid integer!

```python
# ✅ These work:
int("42")      # 42
int("-17")     # -17
int("  25  ")  # 25 (spaces are OK)

# ❌ These don't work:
int("3.14")    # ValueError: invalid literal
int("hello")   # ValueError: invalid literal  
int("12.5")    # ValueError: invalid literal
```

### float() Function

Converts a string to a float:

```python
price_str = "19.99"
price_num = float(price_str)  # "19.99" → 19.99

print(type(price_str))    # <class 'str'>
print(type(price_num))    # <class 'float'>
```

**Advantage:** `float()` can handle decimal points AND integers:

```python
float("3.14")   # 3.14
float("42")     # 42.0 (becomes a float!)
float("-5.5")   # -5.5
```

## Getting Numeric Input

To get numeric input from users, combine `input()` with a conversion function:

### Getting Integer Input

```python
age = int(input("Enter your age: "))
# Now age is an int, not a string!

print(f"Next year you'll be {age + 1}")
```

**What happens:**
1. `input()` gets a string from the user
2. `int()` converts that string to an integer
3. The integer is stored in the variable

### Getting Float Input

```python
price = float(input("Enter the price: "))
tax = price * 0.07
total = price + tax

print(f"Total with tax: ${total}")
```

### Multiple Inputs Example

```python
"""Calculate rectangle area"""
length = float(input("Enter length: "))
width = float(input("Enter width: "))

area = length * width
print(f"Area: {area}")
```

## Converting Numbers to Strings

Sometimes you need to go the other way - converting numbers to strings!

### str() Function

```python
age = 15
message = "I am " + str(age) + " years old"
print(message)  # "I am 15 years old"
```

**Why is this needed?**

```python
age = 15

# ❌ This doesn't work:
message = "I am " + age + " years old"
# TypeError: can only concatenate str to str

# ✅ This works:
message = "I am " + str(age) + " years old"

# ✅ This also works (better!):
message = f"I am {age} years old"
```

## Mixed-Mode Arithmetic Review

When numbers of different types are combined, Python converts automatically:

```python
# int + float → float
result = 5 + 2.5       # 7.5 (float)

# int * float → float
result = 3 * 4.0       # 12.0 (float)

# Division ALWAYS returns float
result = 10 / 2        # 5.0 (float, even though it could be 5)
```

**Rule:** When mixing int and float, the result is always a float!

## Converting Between Numbers

### Float to Int (Truncation)

Converting float to int **truncates** (chops off) the decimal part:

```python
print(int(3.9))     # 3 (not 4!)
print(int(3.1))     # 3
print(int(-3.9))    # -3 (not -4!)
```

**Not rounding!** Use `round()` if you want to round:

```python
print(round(3.9))   # 4
print(round(3.1))   # 3
print(round(3.5))   # 4
```

### Int to Float

This always works and adds `.0`:

```python
print(float(42))    # 42.0
print(float(-17))   # -17.0
```

## Common Conversion Patterns

### Pattern 1: Calculate with User Input

```python
# Get input, convert, calculate
radius = float(input("Enter radius: "))
area = 3.14159 * radius ** 2
print(f"Area: {area}")
```

### Pattern 2: Display Numbers in Text

```python
score = 95
message = f"Your score is {score}"  # f-string (best way!)
# or
message = "Your score is " + str(score)  # manual conversion
```

### Pattern 3: Convert Then Validate

```python
age_str = input("Enter age: ")

try:
    age = int(age_str)
    if age > 0:
        print(f"You are {age} years old")
    else:
        print("Age must be positive")
except ValueError:
    print("That's not a valid number!")
```

## Type Conversion Table

| From | To | Function | Example | Result |
|------|-----|----------|---------|--------|
| str | int | `int()` | `int("42")` | `42` |
| str | float | `float()` | `float("3.14")` | `3.14` |
| int | str | `str()` | `str(42)` | `"42"` |
| float | str | `str()` | `str(3.14)` | `"3.14"` |
| float | int | `int()` | `int(3.9)` | `3` |
| int | float | `float()` | `float(42)` | `42.0` |

## Practical Example: Tax Calculator

```python
"""
Calculate sales tax and total cost
"""

# Get input
price = float(input("Enter price: $"))
tax_rate = float(input("Enter tax rate (as decimal, e.g., 0.07): "))

# Calculate
tax = price * tax_rate
total = price + tax

# Display results
print("\n" + "=" * 30)
print(f"Price:    ${price:.2f}")
print(f"Tax:      ${tax:.2f}")
print(f"Total:    ${total:.2f}")
print("=" * 30)
```

**Example run:**
```
Enter price: $19.99
Enter tax rate (as decimal, e.g., 0.07): 0.07

==============================
Price:    $19.99
Tax:      $1.40
Total:    $21.39
==============================
```

## Common Errors and Solutions

### Error 1: Forgetting to Convert Input

```python
# ❌ Wrong
age = input("Enter age: ")
next_year = age + 1  # TypeError!

# ✅ Correct
age = int(input("Enter age: "))
next_year = age + 1
```

### Error 2: Converting to Wrong Type

```python
# ❌ Wrong - trying to convert decimal to int
price = int(input("Enter price: "))  # Error if user types "19.99"

# ✅ Correct - use float for decimals
price = float(input("Enter price: "))
```

### Error 3: Concatenating Without Converting

```python
age = 15

# ❌ Wrong
print("Age: " + age)  # TypeError!

# ✅ Correct options:
print("Age: " + str(age))
print(f"Age: {age}")
print("Age:", age)
```

### Error 4: Using int() on Floats from Input

```python
# If user might enter decimals, use float()!

# ❌ Risky
height = int(input("Height in meters: "))  # Fails on "1.75"

# ✅ Better
height = float(input("Height in meters: "))
```

## The Round Function

The `round()` function is related to type conversion:

```python
# Round to nearest integer
print(round(3.7))     # 4
print(round(3.2))     # 3

# Round to specific decimal places
print(round(3.14159, 2))   # 3.14
print(round(3.14159, 3))   # 3.142

# Combine with type conversion
price = 19.996
print(int(round(price)))   # 20
```

## Python is Strongly Typed

Python is a **strongly typed** language - it won't automatically convert types that don't make sense:

```python
# ❌ This doesn't work:
result = "5" + 3  # TypeError!

# ✅ You must be explicit:
result = int("5") + 3   # 8
# or
result = "5" + str(3)   # "53"
```

This is actually a good thing - it prevents bugs!

## Summary

- `input()` always returns a string, even if the user types numbers
- Use `int()` to convert strings to integers
- Use `float()` to convert strings to floats  
- Use `str()` to convert numbers to strings
- `int()` truncates decimals; use `round()` to round first
- Python is strongly typed and won't auto-convert incompatible types
- F-strings (`f"..."`) make combining text and numbers easier
- Always convert input to the appropriate type before doing math

## Key Terms

- **Type Conversion** - Changing a value from one data type to another
- **Truncation** - Removing the decimal part (not rounding)
- **Strongly Typed** - A language that requires explicit type conversions
- **Cast** - Another term for type conversion
- **ValueError** - Error that occurs when conversion fails

## Next Lesson Preview

Next, we'll explore functions and modules - how to use Python's built-in functions and import additional functionality from libraries!