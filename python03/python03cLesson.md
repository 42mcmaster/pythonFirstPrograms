# Lesson 3c: String Traversal and Formatting Output

## Learning Objectives
- Understand that strings are sequences
- Traverse characters in a string using for loops
- Format output using field width and precision
- Create properly formatted tables and columns

## Strings as Sequences

In Python, strings are **sequences of characters**. Just like range creates a sequence of numbers, strings are sequences we can loop through!

### Traversing a String

```python
for character in "Hi there!":
    print(character, end=" ")

# Output: H i   t h e r e !
```

Notice:
- Each character is processed one at a time
- Even the space is a character!
- We don't need range() - we can loop directly through the string

### Example: Counting Vowels

```python
text = input("Enter some text: ")
vowel_count = 0

for char in text:
    if char in "aeiouAEIOU":
        vowel_count += 1

print(f"Number of vowels: {vowel_count}")
```

**Sample Run:**
```
Enter some text: Hello World
Number of vowels: 3
```

## Sequences and Range

Both `range()` and strings create sequences we can use with for loops:

```python
# Range creates a list of numbers
print(list(range(4)))        # [0, 1, 2, 3]
print(list(range(1, 5)))     # [1, 2, 3, 4]

# Strings are sequences of characters
for letter in "Python":
    print(letter)
# Output: P y t h o n (each on new line)
```

## Formatting Output

When displaying data, especially in tables, we need to control spacing and alignment.

### The Problem

```python
for exponent in range(7, 11):
    print(exponent, 10 ** exponent)

# Output (poorly aligned):
# 7 10000000
# 8 100000000
# 9 1000000000
# 10 10000000000
```

The columns don't line up!

### The Solution: Format Strings

Python's `%` operator formats strings with specific widths.

#### Basic Syntax
```
"format_string" % value
```

#### Formatting Integers

```python
# %d = integer
# %5d = integer in a field 5 characters wide

for exponent in range(7, 11):
    print("%-3d%12d" % (exponent, 10 ** exponent))

# Output (nicely aligned):
# 7   10000000
# 8   100000000
# 9   1000000000
# 10  10000000000
```

**Format codes:**
- `%-3d` : Integer, 3 characters wide, left-aligned (the minus sign)
- `%12d` : Integer, 12 characters wide, right-aligned (default)

### Formatting Floats

For decimal numbers, we can control:
- Total width
- Decimal places (precision)

```python
salary = 100.00

# Bad - too many decimal places
print("Your salary is $" + str(salary))
# Output: Your salary is $100.0

# Good - exactly 2 decimal places
print("Your salary is $%0.2f" % salary)
# Output: Your salary is $100.00
```

**Format code for floats:**
```
%<width>.<precision>f
```

- `width`: Total characters (optional)
- `precision`: Decimal places
- `f`: Float type

### Format String Examples

```python
# Integer formatting
print("%d" % 42)           # 42
print("%5d" % 42)          # "   42" (padded to 5 chars)
print("%-5d" % 42)         # "42   " (left-aligned)

# Float formatting
print("%f" % 3.14159)      # 3.141590 (default 6 decimals)
print("%.2f" % 3.14159)    # 3.14 (2 decimals)
print("%8.2f" % 3.14159)   # "    3.14" (8 chars total)

# String formatting
print("%s" % "Hello")      # Hello
print("%10s" % "Hello")    # "     Hello"
```

### Multiple Values

Format multiple values by putting them in parentheses:

```python
name = "Alice"
age = 16
gpa = 3.87

print("Student: %-10s Age: %2d GPA: %.2f" % (name, age, gpa))
# Output: Student: Alice      Age: 16 GPA: 3.87
```

## Creating Tables

Let's create a properly formatted table:

```python
# Header
print("%-10s %8s %8s" % ("Item", "Price", "Tax"))
print("-" * 28)

# Data rows
items = ["Apple", "Banana", "Orange"]
prices = [1.25, 0.75, 1.50]

for i in range(len(items)):
    tax = prices[i] * 0.07
    print("%-10s $%7.2f $%7.2f" % (items[i], prices[i], tax))

# Output:
# Item          Price      Tax
# ----------------------------
# Apple       $   1.25 $   0.09
# Banana      $   0.75 $   0.05
# Orange      $   1.50 $   0.11
```

## Modern Formatting (f-strings)

Python 3.6+ introduced a modern way: **f-strings**

```python
name = "Alice"
score = 95.7

# Old way
print("Student: %s Score: %.1f" % (name, score))

# New way (f-string)
print(f"Student: {name} Score: {score:.1f}")

# Both output: Student: Alice Score: 95.7
```

F-strings are easier to read and write! We'll use these more later.

## Summary Table: Format Codes

| Code | Type | Example | Result |
|------|------|---------|--------|
| `%d` | Integer | `%d` % 42 | 42 |
| `%5d` | Integer (5 wide) | `%5d` % 42 | "   42" |
| `%-5d` | Integer (left) | `%-5d` % 42 | "42   " |
| `%f` | Float | `%f` % 3.14 | 3.140000 |
| `%.2f` | Float (2 decimals) | `%.2f` % 3.14159 | 3.14 |
| `%8.2f` | Float (8 wide, 2 dec) | `%8.2f` % 3.14 | "    3.14" |
| `%s` | String | `%s` % "Hi" | Hi |

## Key Points

1. **Strings are sequences** - you can loop through characters
2. **Format strings control spacing** - use them for aligned output
3. **Left vs Right alignment** - use `-` for left
4. **Precision matters** - especially for money (always .2f)
5. **Multiple values** - put them in parentheses as a tuple

## Practice

Try this in IDLE or VS Code:

```python
# Experiment with formatting
value = 123.456

print("Default: %f" % value)
print("2 decimals: %.2f" % value)
print("10 wide, 1 decimal: %10.1f" % value)
print("Left-aligned: %-10.2f" % value)
```

Run this and observe how the spacing changes!