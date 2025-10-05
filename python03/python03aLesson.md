# Lesson 3a: Introduction to For Loops

## Learning Objectives
- Understand what repetition statements (loops) are
- Learn the difference between definite and indefinite iteration
- Write basic for loops to repeat actions a fixed number of times
- Understand loop terminology (iteration, pass, loop header, loop body)

## What are Loops?

**Loops** (also called repetition statements) allow you to repeat an action multiple times without writing the same code over and over.

Each time through a loop is called an **iteration** or **pass**.

## Types of Loops

There are two main types of loops:

1. **Definite Iteration**: Repeat an action a predetermined number of times
   - We use **for loops** for this
   
2. **Indefinite Iteration**: Repeat an action until a condition is met
   - We use **while loops** for this (we'll learn these later)

## The For Loop

### Basic Syntax

```python
for variable in range(number):
    statement1
    statement2
    # ... more statements
```

- The first line is the **loop header**
- The indented statements are the **loop body**
- The loop body MUST be indented

### Example 1: Simple Repetition

```python
for eachPass in range(4):
    print("It's alive!", end=" ")
```

**Output:**
```
It's alive! It's alive! It's alive! It's alive!
```

This loop runs 4 times, printing the message each time.

### Example 2: Computing Exponents

```python
number = 2
exponent = 3
product = 1

for eachPass in range(exponent):
    product = product * number
    print(product, end=" ")

print()  # New line
print(product)
```

**Output:**
```
2 4 8
8
```

This computes 2³ = 8 by multiplying 2 by itself 3 times.

## Augmented Assignment Operators

Python provides shortcuts for common operations:

```python
a = 17
a += 3   # Same as: a = a + 3
a -= 3   # Same as: a = a - 3
a *= 3   # Same as: a = a * 3
a /= 3   # Same as: a = a / 3
a %= 3   # Same as: a = a % 3

s = "hi"
s += " there"  # Same as: s = s + " there"
```

## Key Points

- For loops are perfect when you know exactly how many times to repeat
- The loop variable (like `eachPass`) is often not used in the loop body
- All statements in the loop body must be indented the same amount
- `range(n)` creates a sequence from 0 to n-1

## Common Mistakes

**Off-by-One Error**: Getting the number of iterations wrong

```python
# Trying to count 1 through 4, but this only goes 1 through 3
for count in range(1, 4):
    print(count)
# Output: 1 2 3
```

This is a **logic error**, not a syntax error, so Python won't catch it!

## Practice

Try running these examples in IDLE or VS Code to see how they work. Experiment by changing the numbers and seeing what happens.