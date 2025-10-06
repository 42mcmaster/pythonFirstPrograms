# Lesson 3a: Introduction to For Loops

## Learning Objectives
- Understand what repetition statements (loops) are
- Learn the difference between definite and indefinite iteration
- Write basic for loops to repeat actions a fixed number of times
- Understand loop terminology (iteration, pass, loop header, loop body)
- Master the accumulator pattern for building results over time

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

### Example 2: Computing Exponents (Manual)

```python
number = 2
exponent = 3
product = 1

for _ in range(exponent):
    product = product * number
    print(product, end=" ")  # prints 2 4 8

print()  # line break so the next print is on a new line
print(product)  # final value after the loop
```

**Output:**
```
2 4 8
8
```

This computes 2³ = 8 by multiplying 2 by itself 3 times.

**Note:** Exponent = **repeated multiplication**. (Shortcut in Python: `2 ** 3`)

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

## Accumulators: Real-World Pattern

An **accumulator** is a variable that **builds up** a result over time inside a loop. 

**Common uses:** totals, counts, averages, scores, balances.

### The Pattern:

```python
accumulator = start_value
for item in collection:
    accumulator = accumulator + change_from_item
```

**Shorthand:**
```python
accumulator += change_from_item
```

### Example 3 (Real-World): Shopping Cart Total

```python
cart_items = [12.99, 5.50, 3.25, 20.00]  # T-shirt, mug, notebook, headphones
total = 0.0

for price in cart_items:
    total += price

print("Final total:", total)  # 41.74
```

**Step-through:**
```
Start total = 0.00
+ 12.99  → 12.99
+ 5.50   → 18.49
+ 3.25   → 21.74
+ 20.00  → 41.74
Final total = 41.74
```

### Example 4 (Real-World): Counting Passes (Attendance)

Count how many students are **present**.

```python
attendance = ["P", "A", "P", "P", "A", "P"]  # P=Present, A=Absent
present_count = 0

for mark in attendance:
    if mark == "P":
        present_count += 1

print("Students present:", present_count)  # 4
```

### Example 5 (Real-World): Game Score

```python
events = ["coin", "coin", "enemy", "coin", "goal"]
score = 0

for e in events:
    if e == "coin":
        score += 10
    elif e == "enemy":
        score += 50
    elif e == "goal":
        score += 100

print("Final score:", score)  # 170
```

Same accumulator pattern, different domain.

### Example 6 (Real-World): Average Sensor Reading

```python
readings = [20.1, 19.8, 20.4, 20.0]
total = 0.0

for r in readings:
    total += r

average = total / len(readings)
print("Average temp:", average)  # 20.075
```

Accumulate → then compute a derived value (average).

## Visual Walkthrough: Summing 0 + 1 + 2 + 3 + 4

```python
total = 0
for i in range(5):
    total = total + i
print(total)   # 10
```

| Iteration | `i` | Calculation | `total` |
|-----------|-----|-------------|---------|
| Start     | –   | total = 0   | 0       |
| 1st pass  | 0   | total = 0 + 0 | 0     |
| 2nd pass  | 1   | total = 0 + 1 | 1     |
| 3rd pass  | 2   | total = 1 + 2 | 3     |
| 4th pass  | 3   | total = 3 + 3 | 6     |
| 5th pass  | 4   | total = 6 + 4 | 10    |

## Key Points

- For loops are perfect when you know exactly how many times to repeat
- The loop variable (like `eachPass` or `i`) may or may not be used in the loop body
- All statements in the loop body must be indented the same amount
- `range(n)` creates a sequence from 0 to n-1
- The accumulator pattern is fundamental for building totals, counts, and other aggregate values

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

Try running these examples in IDLE or VS Code to see how they work. Experiment by:
- Changing the numbers in the examples
- Adding more items to the lists
- Creating your own accumulator patterns (counting, summing, multiplying)