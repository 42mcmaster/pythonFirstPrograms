---
marp: true
theme: uncover
class: invert
paginate: true
---

# Lesson 3a: 
# Introduction to `For` Loops

---

## Learning Objectives
- Understand what **loops** (repetition statements) are  
- Distinguish between **definite** and **indefinite** iteration  
- Write **basic `for` loops** to repeat actions  
- Master the **accumulator pattern**
- Learn loop terminology:
  - iteration / pass  
  - loop header  
  - loop body  

---

## What are Loops?

- **Loops** let us repeat actions without rewriting code  
- Each time through the loop = **iteration** or **pass**  

---

## Types of Loops

1. **Definite Iteration**  
   - Repeat a set number of times  
   - Use a **`for` loop**  

2. **Indefinite Iteration**  
   - Repeat until a condition is met  
   - Use a **`while` loop**  

---

## The For Loop — Basic Syntax

```python
for counter in range(number):
    statement1
    statement2
```

* First line = **loop header**
* Indented code = **loop body**
* The loop body **must be indented**

---

Example 1: Simple Repetition

<br>

```python
for eachPass in range(4):
    print("It's alive!", end=" ")
```
<br>

**Output:**

```
It's alive! It's alive! It's alive! It's alive!
```

---

Example 2: Computing Exponents 
(repeated multiplication)

```python
number = 2
exponent = 3
product = 1

for x in range(exponent):
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
---
Example 2 Explanation

* Start with `product = 1` because multiplying by 1 doesn’t change the result
* Loop exponent times `(range(3) → 3 passes)`
* Each pass multiplies product by number

Step by step:
Pass 1 → product = 1 * 2 = 2
Pass 2 → product = 2 * 2 = 4
Pass 3 → product = 4 * 2 = 8

---

### Augmented Assignment Operators
In example 2 we see `product = product * number`
 

```python
a = 17
a += 3   # a = a + 3
a -= 3   # a = a - 3
a *= 3   # a = a * 3
a /= 3   # a = a / 3
a %= 3   # a = a % 3

s = "hi"
s += " there"  # "hi there"
```

---

### Accumulators: Real-World Pattern

**Accumulator** = a variable that **builds up** a result over time inside a loop

**Common uses:**  
totals, counts, averages, scores, balances

---

### The Accumulator Pattern

```python
accumulator = start_value
for item in collection:
    accumulator = accumulator + change_from_item
```

**Shorthand:**

```python
accumulator += change_from_item
```

---

### Example 3: Shopping Cart Total

```python
cart_items = [12.99, 5.50, 3.25, 20.00]
# T-shirt, mug, notebook, headphones
total = 0.0

for price in cart_items:  # price iterates through the list
    total += price  # or total = total + price

print("Final total:", total)  # 41.74
```

---

### Step-Through: Shopping Cart

```
Start total = 0.00  # intial total
+ 12.99  → 12.99    # new total
+ 5.50   → 18.49    # new total
+ 3.25   → 21.74    # new total
+ 20.00  → 41.74    # last item is 20.00 so new total is final

Final total = 41.74
```

---

### Example 4: Counting Passes (Attendance)

Count how many students are **present**

```python
attendance = ["P", "A", "P", "P", "A", "P"]
# P=Present, A=Absent
present_count = 0

for mark in attendance:
    if mark == "P":
        present_count += 1

print("Students present:", present_count)  # 4
```

---

### Example 5: Game Score

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

Same pattern, different domain!

---

### Example 6: Average Sensor Reading

```python
readings = [20.1, 19.8, 20.4, 20.0]
total = 0.0

for r in readings:
    total += r

average = total / len(readings)
print("Average temp:", average)  # 20.075
```

Accumulate → then compute a derived value

---

### Visual Walkthrough: Summing 0+1+2+3+4

```python
total = 0
for i in range(5):
    total = total + i  # or total += i
print(total)   # 10
```

---

## Step-by-Step Trace

| Iteration | `i` | Calculation   | `total` |
|-----------|-----|---------------|---------|
| Start     | –   | total = 0     | 0       |
| 1st pass  | 0   | total = 0 + 0 | 0       |
| 2nd pass  | 1   | total = 0 + 1 | 1       |
| 3rd pass  | 2   | total = 1 + 2 | 3       |
| 4th pass  | 3   | total = 3 + 3 | 6       |
| 5th pass  | 4   | total = 6 + 4 | 10      |

---

## Key Points

* For loops are best when you know the number of repeats
* Loop variable may or may not be used in the body
* All statements inside must align indentation
* `range(n)` → creates numbers `0 ... n-1`
* **Accumulator pattern** is fundamental for totals, counts, aggregates

---

## Common Mistake: Off-by-One

```python
# Trying to count 1 through 4
for count in range(1, 4):
    print(count)
```

**Output:**

```
1
2
3
```

This is a logic error, not a syntax error!

---

## Practice

* Run these examples in **IDLE or VS Code**  
* Experiment by changing the numbers  
* Add more items to the lists  
* Create your own accumulator patterns

---

## Summary

* **Loops** = repeat actions efficiently  
* **For loops** = definite iteration (known count)  
* **Accumulators** = build results over time  
* **Real-world uses**: totals, counts, scores, averages