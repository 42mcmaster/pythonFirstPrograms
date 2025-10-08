---
marp: true
theme: uncover
class: invert
paginate: true
title: Lesson 3b — Count-Controlled Loops, Range, and Formatted Output
---

# Lesson 3b  
## Count-Controlled Loops, Range, and Formatted Output

---

## 🎯 Learning Objectives

- Use loops to count through a range of numbers  
- Specify lower and upper bounds with `range()`  
- Use a step value to skip numbers  
- Create loops that count down  
- Use the loop variable in calculations  
- Format output into aligned tables and reports  

---

# 🔢 Understanding `range()`

The `range()` function creates a sequence of numbers.  
It can take **1, 2, or 3 arguments.**

---

### 1 Argument: `range(stop)`

```python
range(4)  # Creates: 0, 1, 2, 3
````

* Starts at 0
* Stops **before** the number given
* Increases by 1

---

### 2 Arguments: `range(start, stop)`

```python
range(1, 5)  # Creates: 1, 2, 3, 4
```

* Starts at the first number
* Stops **before** the second number
* Step defaults to +1

---

### 3 Arguments: `range(start, stop, step)`

```python
range(1, 10, 2)  # Creates: 1, 3, 5, 7, 9
```

* Starts at first number
* Stops **before** second number
* Increments (or decrements) by `step`

---

# 🧮 Count-Controlled Loops

A **count-controlled loop** uses the loop variable as a counter.

---

### Example 1: Using the Counter

```python
product = 1
for count in range(1, 5):
    product = product * count
print(product)  # Output: 24
```

---

### Example 2: Summation with Bounds

```python
lower = int(input("Enter lower bound: "))
upper = int(input("Enter upper bound: "))

theSum = 0
for number in range(lower, upper + 1):
    theSum += number

print("The sum is", theSum)
```

🧩 **Note:** Use `upper + 1` because `range()` stops *before* the end.

---

### Sample Run

```
Enter the lower bound: 1
Enter the upper bound: 10
The sum is 55
```

---

# 🪜 Using Steps

### Counting by 2s

```python
for count in range(2, 11, 2):
    print(count, end=" ")
# 2 4 6 8 10
```

---

### Counting by 3s

```python
for count in range(1, 10, 3):
    print(count, end=" ")
# 1 4 7
```

---

### Visualizing `range()`

```python
print(list(range(1, 6, 1)))  # [1, 2, 3, 4, 5]
print(list(range(1, 6, 2)))  # [1, 3, 5]
print(list(range(1, 6, 3)))  # [1, 4]
```

---

# ⏬ Counting Down

Use a **negative step** to count backward!

```python
for count in range(10, 0, -1):
    print(count, end=" ")
# 10 9 8 7 6 5 4 3 2 1
```

---

### Example: Countdown Timer

```python
import time

print("Rocket launch countdown!")
for seconds in range(10, 0, -1):
    print(seconds)
    time.sleep(1)
print("BLAST OFF!")
```
---
# 🔁 Common Patterns

### Sum of Even Numbers

```python
theSum = 0
for count in range(2, 11, 2):
    theSum += count
print(theSum)  # 30
```
---
### Explaining Previous Script
| Loop # | count | theSum before | Operation | theSum after |
| ------ | ----- | ------------- | --------- | ------------ |
| 1      | 2     | 0             | 0 + 2     | 2            |
| 2      | 4     | 2             | 2 + 4     | 6            |
| 3      | 6     | 6             | 6 + 6     | 12           |
| 4      | 8     | 12            | 12 + 8    | 20           |
| 5      | 10    | 20            | 20 + 10   | 30           |

---

### Product of a Range

```python
product = 1
for count in range(1, 6):
    product *= count
print(product)  # 120
```
---
### Explaining Previous Script

| Loop # | count | product before | Operation | product after |
| :----: | :---: | :------------: | :-------- | :-----------: |
|    1   |   1   |        1       | 1 × 1     |       1       |
|    2   |   2   |        1       | 1 × 2     |       2       |
|    3   |   3   |        2       | 2 × 3     |       6       |
|    4   |   4   |        6       | 6 × 4     |       24      |
|    5   |   5   |       24       | 24 × 5    |      120      |

---
### Counting by Tens

```python
for count in range(0, 101, 10):
    print(count, end=" ")
# 0 10 20 30 ... 100
```

---
# Break Time - Questions?
---


# 🧾 Formatted Output

When creating tables or reports, we need proper **alignment**.
Python provides the **`%` formatting operator**.

---

### Basic Example

```python
name = "Alice"
age = 15
print("My name is %s and I am %d years old" % (name, age))
```

🖥️ Output:
`My name is Alice and I am 15 years old`

---

## Common Format Specifiers

| Code | Meaning                |
| ---- | ---------------------- |
| `%s` | String                 |
| `%d` | Integer (whole number) |
| `%f` | Float (decimal number) |

---

# 📏 Controlling Width & Alignment

### Right-Aligned (default)

```python
print("%10d" % 42)        # "        42"
print("%10s" % "Hello")   # "     Hello"
```

---

### Left-Aligned (with `-`)

```python
print("%-10s" % "Hello")  # "Hello     "
print("%-10d" % 42)       # "42        "
```

---

# 💲 Formatting Decimal Places

```python
price = 19.5
print("Price: $%.2f" % price)   # Price: $19.50

value = 3.14159
print("Pi: %.2f" % value)       # Pi: 3.14
print("Pi: %.4f" % value)       # Pi: 3.1416
```

---

# 🧮 Creating Tables

```python
print("%-15s %10s" % ("Item", "Price"))  # Header
print("-" * 25)

print("%-15s $%9.2f" % ("Notebook", 3.50))
print("%-15s $%9.2f" % ("Pen", 1.25))
print("%-15s $%9.2f" % ("Eraser", 0.75))
```
---
## Output

```
Item                 Price
-------------------------
Notebook        $     3.50
Pen             $     1.25
Eraser          $     0.75
```
---

# * - = Separator Lines

```python
print("=" * 40)
print("-" * 40)
print("*" * 40)
```

What the above looks like: 
```
=========================
-------------------------
*************************
```

---

# 🧾 Grade Report Example

```python
print("GRADE REPORT")
print("=" * 30)
print("%-15s %8s" % ("Subject", "Grade"))
print("-" * 30)

subjects = ["Math", "Science", "English"]
grades = [95, 88, 92]

for i in range(len(subjects)):
    print("%-15s %8d" % (subjects[i], grades[i]))

print("-" * 30)
average = sum(grades) / len(grades)
print("%-15s %8.1f" % ("Average:", average))
print("=" * 30)
```

---

### Output

```
GRADE REPORT
==============================
Subject            Grade
------------------------------
Math                  95
Science               88
English               92
------------------------------
Average:            91.7
==============================
```

---

# 🧩 Multiple Values Example

```python
name = "Bob"
test1 = 85
test2 = 92
average = (test1 + test2) / 2

print("%-10s   Test 1: %3d   Test 2: %3d   Avg: %.1f"
      % (name, test1, test2, average))
```

Output:
`Bob        Test 1:  85   Test 2:  92   Avg: 88.5`



---

# ✅ Table Formatting Checklist

1. Headers and separators
2. Consistent row formatting
3. Left-align text, right-align numbers
4. Control decimal places
5. Add totals or summaries

---

## ⚠️ Important Points

1. **Range upper bound is exclusive**
   `range(1, 5)` → 1, 2, 3, 4
   Use `range(1, 6)` to include 5
<br>
2. **Loop variable updates automatically**
   No need for `count += 1` — handled by `range()`

---

## ⚠️ Important Points Continued

3. **Steps can be positive or negative**
   (But not zero!)
<br>
4. **Match your format string values**
   `" %s %d" % ("Hi", 5)` ✅
   `" %s %d" % ("Hi")` ❌

---
# 🚫 Common Mistakes

### 1. Wrong Upper Bound

```python
for num in range(1, 10):  # Should be range(1, 11)
    theSum += num
```

---

### 2. Zero Step

```python
for i in range(1, 10, 0):  # ❌ ValueError
    print(i)
```

---

### 3. Backwards Range

```python
for i in range(10, 1):  # ❌ no output
    print(i)

# ✅ Correct:
for i in range(10, 1, -1):
    print(i)
```

---

### 4. Format String Mismatch

```python
print("Name: %s Age: %d" % ("Alice"))  # ❌ Missing value
print("Name: %s Age: %d" % ("Alice", 15))  # ✅
```

---

# 🧠 Practice Exercise

Try these in VS Code or IDLE:

```python
print("Range(5):", list(range(5)))
print("Range(2, 8):", list(range(2, 8)))
print("Range(0, 10, 2):", list(range(0, 10, 2)))
print("Range(10, 0, -1):", list(range(10, 0, -1)))

print("\nFormatting Practice:")
print("%-10s %5d" % ("Item", 123))
print("Price: $%.2f" % 19.5)
print("=" * 20)
```

---

# 🧩 Summary

* `range()` defines your counting sequence
* `for` loops automatically update their variable
* Use width (`%10s`) and precision (`%.2f`) for neat tables
* Practice formatting output for professional reports

---

# 💡 End of Lesson 3b

**Count-Controlled Loops, Range, and Formatted Output**
