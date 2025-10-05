# Lesson 2d: Arithmetic Expressions

## Learning Objectives
By the end of this lesson, you will be able to:
- Use all arithmetic operators in Python
- Understand operator precedence
- Write complex arithmetic expressions
- Distinguish between `/` (division) and `//` (integer division)
- Use the modulus operator `%` effectively

## Arithmetic Operators

Python supports all the standard arithmetic operations you know from math class, plus a few more:

| Operator | Meaning | Example | Result |
|----------|---------|---------|--------|
| `+` | Addition | `5 + 3` | `8` |
| `-` | Subtraction | `10 - 4` | `6` |
| `*` | Multiplication | `7 * 6` | `42` |
| `/` | Division | `15 / 4` | `3.75` |
| `//` | Integer Division (Quotient) | `15 // 4` | `3` |
| `%` | Modulus (Remainder) | `15 % 4` | `3` |
| `**` | Exponentiation (Power) | `2 ** 3` | `8` |
| `-` | Negation (Unary) | `-5` | `-5` |

## Basic Operations

### Addition and Subtraction

These work exactly as you'd expect:

```python
total = 10 + 5        # 15
difference = 10 - 5   # 5
temperature = 72.5 + 3.2  # 75.7
```

### Multiplication

Use `*` (asterisk) for multiplication:

```python
area = 5 * 3          # 15
price = 19.99 * 3     # 59.97
```

### Division - Two Types!

Python has TWO division operators:

**Regular Division (`/`)** - Always returns a float:

```python
print(10 / 3)    # 3.3333333333333335
print(10 / 2)    # 5.0  (still a float!)
print(9 / 3)     # 3.0  (still a float!)
```

**Integer Division (`//`)** - Returns only the whole number part:

```python
print(10 // 3)   # 3
print(10 // 2)   # 5
print(9 // 3)    # 3
print(7 // 2)    # 3  (not 3.5!)
```

Think of `//` as "how many times does the divisor fit completely?"

### Modulus (`%`) - The Remainder Operator

The modulus operator gives you the **remainder** after division:

```python
print(10 % 3)    # 1  (10 ÷ 3 = 3 remainder 1)
print(15 % 4)    # 3  (15 ÷ 4 = 3 remainder 3)
print(8 % 2)     # 0  (8 ÷ 2 = 4 remainder 0)
print(7 % 5)     # 2  (7 ÷ 5 = 1 remainder 2)
```

**Useful fact:** If `x % 2 == 0`, then x is even!

```python
number = 7
if number % 2 == 0:
    print("Even")
else:
    print("Odd")  # This will print!
```

### Division and Modulus Together

These operations are related:

```python
# For 17 divided by 5:
quotient = 17 // 5   # 3  (how many times 5 fits)
remainder = 17 % 5   # 2  (what's left over)

# Check: 3 * 5 + 2 = 17 ✓
```

### Exponentiation (`**`)

Use `**` to raise a number to a power:

```python
squared = 5 ** 2      # 25  (5²)
cubed = 2 ** 3        # 8   (2³)
power = 10 ** 6       # 1000000  (10⁶)
```

Also works with fractional exponents:

```python
square_root = 25 ** 0.5    # 5.0  (√25)
cube_root = 8 ** (1/3)     # 2.0  (∛8)
```

### Negation

Use `-` before a number to make it negative:

```python
positive = 10
negative = -positive   # -10
result = -5 + 3       # -2
```

## Operator Precedence (Order of Operations)

Just like in math, Python follows a specific order when evaluating expressions. Remember PEMDAS? Python follows similar rules!

**From HIGHEST to LOWEST precedence:**

1. **Parentheses** `()`
2. **Exponentiation** `**`
3. **Negation** `-x` (unary minus)
4. **Multiplication, Division, Modulus** `*`, `/`, `//`, `%` (left to right)
5. **Addition, Subtraction** `+`, `-` (left to right)

### Examples:

```python
# Without parentheses
result = 5 + 3 * 2
# Multiplication first: 5 + 6 = 11

# With parentheses
result = (5 + 3) * 2
# Addition first: 8 * 2 = 16

# More complex
result = 2 + 3 ** 2 * 4 - 1
# Step 1: 3 ** 2 = 9
# Step 2: 9 * 4 = 36
# Step 3: 2 + 36 = 38
# Step 4: 38 - 1 = 37
```

### Left-to-Right Evaluation

When operators have the same precedence, Python evaluates left to right:

```python
result = 10 - 5 - 2
# (10 - 5) - 2 = 5 - 2 = 3
# NOT 10 - (5 - 2) = 10 - 3 = 7

result = 20 / 4 / 2
# (20 / 4) / 2 = 5.0 / 2 = 2.5
```

**Exception:** Exponentiation is RIGHT-to-left:

```python
result = 2 ** 3 ** 2
# 2 ** (3 ** 2) = 2 ** 9 = 512
# NOT (2 ** 3) ** 2 = 8 ** 2 = 64
```

## Using Parentheses

When in doubt, use parentheses to make your intentions clear!

```python
# Hard to read
total = price * quantity + tax

# Much clearer
total = (price * quantity) + tax

# Or maybe you meant:
total = price * (quantity + tax)
```

Even if the parentheses aren't needed for correctness, they can improve readability.

## Practical Examples

### Example 1: Temperature Conversion

```python
"""Convert Fahrenheit to Celsius"""
fahrenheit = 98.6
celsius = (fahrenheit - 32) * 5 / 9
print(f"{fahrenheit}°F = {celsius}°C")
# Output: 98.6°F = 37.0°C
```

### Example 2: Calculate Average

```python
"""Calculate average of three test scores"""
test1 = 85
test2 = 92
test3 = 88

average = (test1 + test2 + test3) / 3
print(f"Your average score is {average}")
# Output: Your average score is 88.33333333333333
```

### Example 3: Even or Odd

```python
"""Check if a number is even or odd"""
number = 47

if number % 2 == 0:
    print(f"{number} is even")
else:
    print(f"{number} is odd")
# Output: 47 is odd
```

### Example 4: Time Conversion

```python
"""Convert total seconds to hours, minutes, and seconds"""
total_seconds = 7384

hours = total_seconds // 3600
remaining = total_seconds % 3600
minutes = remaining // 60
seconds = remaining % 60

print(f"{total_seconds} seconds = {hours}h {minutes}m {seconds}s")
# Output: 7384 seconds = 2h 3m 4s
```

### Example 5: Circle Calculations

```python
"""Calculate circumference and area of a circle"""
pi = 3.14159
radius = 5

circumference = 2 * pi * radius
area = pi * radius ** 2

print(f"For a circle with radius {radius}:")
print(f"Circumference: {circumference}")
print(f"Area: {area}")
```

## Mixed-Mode Arithmetic

When you mix integers and floats, the result is always a float:

```python
print(3 + 4.0)      # 7.0 (float)
print(10 / 2)       # 5.0 (float)
print(5 * 2.5)      # 12.5 (float)
print(3 ** 2.0)     # 9.0 (float)
```

**Exception:** Integer division can return an int if both operands are ints:

```python
print(10 // 3)      # 3 (int)
print(10.0 // 3)    # 3.0 (float)
```

## Common Pitfalls

### 1. Integer Division When You Want Regular Division

```python
# ❌ Wrong - gives 0!
average = 5 / 10  # Wait, this is fine...
average = 5 // 10  # This gives 0!

# ✅ Correct
average = 5 / 10  # 0.5
```

### 2. Forgetting Parentheses

```python
# ❌ Wrong - multiplication happens first!
result = 10 + 5 * 2  # 20, not 30!

# ✅ Correct
result = (10 + 5) * 2  # 30
```

### 3. Confusing `/` and `//`

```python
# These are DIFFERENT!
print(7 / 2)   # 3.5
print(7 // 2)  # 3
```

### 4. Negative Modulus Results

```python
# The sign of modulus result matches the divisor
print(7 % 3)    # 2
print(-7 % 3)   # 2  (not -2!)
print(7 % -3)   # -2 (not 2!)
```

## Multi-Line Expressions

For long expressions, use `\` to continue on the next line:

```python
result = 3 + 4 * \
         2 ** 5
# Same as: 3 + 4 * 2 ** 5 = 131
```

Or use parentheses (preferred):

```python
result = (3 + 4 *
          2 ** 5)
```

## Summary

- Python has 8 arithmetic operators: `+`, `-`, `*`, `/`, `//`, `%`, `**`, and unary `-`
- `/` always returns a float; `//` returns the quotient (whole number part)
- `%` returns the remainder after division
- `**` raises numbers to powers
- Operator precedence: Parentheses → Exponents → Multiplication/Division → Addition/Subtraction
- Use parentheses to make complex expressions clearer
- Mixed-mode arithmetic (int + float) produces a float

## Key Terms

- **Operator** - A symbol that performs an operation on values
- **Expression** - A combination of values and operators that produces a result
- **Precedence** - The order in which operators are evaluated
- **Integer Division** - Division that returns only the whole number part
- **Modulus** - The remainder after division
- **Exponentiation** - Raising a number to a power

## Next Lesson Preview

Next, we'll learn about type conversions - how to convert between integers, floats, and strings, and how to get numeric input from users!