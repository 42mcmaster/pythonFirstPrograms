---
marp: true
theme: uncover
class: invert
paginate: true
---

# Lesson 3.1: Introduction to For Loops

---

## Learning Objectives
- Understand what **loops** (repetition statements) are  
- Distinguish between **definite** and **indefinite** iteration  
- Write **basic for loops** to repeat actions  
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
   - Use a **for loop**  

2. **Indefinite Iteration**  
   - Repeat until a condition is met  
   - Use a **while loop**  

---

## The For Loop — Basic Syntax

```python
for variable in range(number):
    statement1
    statement2
````

* First line = **loop header**
* Indented code = **loop body**
* The loop body **must be indented**

---

## Example 1: Simple Repetition

```python
for eachPass in range(4):
    print("It's alive!", end=" ")
```

**Output:**

```
It's alive! It's alive! It's alive! It's alive!
```

---

## Example 2: Computing Exponents

```python
number = 2
exponent = 3
product = 1

for eachPass in range(exponent):
    product = product * number
    print(product, end=" ")

print()
print(product)
```

**Output:**

```
2 4 8
8
```

---

## Augmented Assignment Operators

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

## Key Points

* For loops are best when you know the number of repeats
* Loop variable may not be used in the body
* All statements inside must align indentation
* `range(n)` → creates numbers `0 ... n-1`

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

⚠️ Logic error, not syntax error!

---

## Practice

✅ Run these examples in **IDLE or VS Code**
✅ Experiment by changing the numbers
✅ Watch how the loop output changes

---

```

Would you like me to also **add a dedicated practice slide** for your students where they compute **squares of numbers 1–5** (using both multiplication and the `**` exponent operator), so it flows right after the “Exponent” example?
```
