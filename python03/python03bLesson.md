# Lesson 3b: Count-Controlled Loops, Range, and Formatted Output

## Learning Objectives
- Use loops to count through a range of numbers
- Specify explicit lower and upper bounds with range()
- Use a step value to skip numbers
- Create loops that count down
- Use the loop variable in calculations
- Format output into aligned tables and reports

## Understanding Range

The `range()` function creates a sequence of numbers. It can take 1, 2, or 3 arguments.

### One Argument: range(stop)
```python
range(4)  # Creates: 0, 1, 2, 3
```
- Starts at 0
- Stops BEFORE the number given
- Goes up by 1

### Two Arguments: range(start, stop)
```python
range(1, 5)  # Creates: 1, 2, 3, 4
```
- Starts at the first number
- Stops BEFORE the second number
- Goes up by 1

### Three Arguments: range(start, stop, step)
```python
range(1, 10, 2)  # Creates: 1, 3, 5, 7, 9
```
- Starts at the first number
- Stops BEFORE the second number
- Goes up (or down) by the step value

## Count-Controlled Loops

A **count-controlled loop** uses the loop variable as a counter.

### Example 1: Using the Counter

```python
product = 1
for count in range(1, 5):
    product = product * count
print(product)  # Output: 24 (which is 1 * 2 * 3 * 4)
```

### Example 2: Summation with Bounds

```python
lower = int(input("Enter the lower bound: "))
upper = int(input("Enter the upper bound: "))

theSum = 0
for number in range(lower, upper + 1):
    theSum = theSum + number

print("The sum is", theSum)
```

**Sample Run:**
```
Enter the lower bound: 1
Enter the upper bound: 10
The sum is 55
```

**Important:** We use `upper + 1` because range stops BEFORE the last number!

## Using Steps

### Counting by 2s
```python
for count in range(2, 11, 2):
    print(count, end=" ")
# Output: 2 4 6 8 10
```

### Counting by 3s
```python
for count in range(1, 10, 3):
    print(count, end=" ")
# Output: 1 4 7
```

### Visualizing Range
```python
# See what range creates
print(list(range(1, 6, 1)))    # [1, 2, 3, 4, 5]
print(list(range(1, 6, 2)))    # [1, 3, 5]
print(list(range(1, 6, 3)))    # [1, 4]
```

## Counting Down

Use a **negative step** to count backwards!

```python
for count in range(10, 0, -1):
    print(count, end=" ")
# Output: 10 9 8 7 6 5 4 3 2 1
```

### Example: Countdown Timer
```python
import time

print("Rocket launch countdown!")
for seconds in range(10, 0, -1):
    print(seconds)
    time.sleep(1)  # Wait 1 second
print("BLAST OFF!")
```

## Formatted Output and Tables

When creating reports and tables, we need to align text and numbers properly. Python provides the `%` formatting operator for this.

### Basic String Formatting

The `%` operator lets you insert values into strings:

```python
name = "Alice"
age = 15
print("My name is %s and I am %d years old" % (name, age))
# Output: My name is Alice and I am 15 years old
```

### Format Specifiers

Common format specifiers:
- `%s` - String
- `%d` - Integer (whole number)
- `%f` - Float (decimal number)

### Controlling Width and Alignment

Add a number between `%` and the letter to control width:

```python
# Right-aligned (default for numbers)
print("%10d" % 42)        # "        42" (8 spaces, then 42)
print("%10s" % "Hello")   # "     Hello" (5 spaces, then Hello)

# Left-aligned (use minus sign)
print("%-10s" % "Hello")  # "Hello     " (Hello, then 5 spaces)
print("%-10d" % 42)       # "42        " (42, then 8 spaces)
```

### Formatting Decimal Places

Use `.` to specify decimal places for floats:

```python
price = 19.5
print("Price: $%.2f" % price)   # "Price: $19.50"

value = 3.14159
print("Pi: %.2f" % value)       # "Pi: 3.14"
print("Pi: %.4f" % value)       # "Pi: 3.1416"
```

### Creating Tables

Combine width, alignment, and decimal formatting to create tables:

```python
# Table header
print("%-15s %10s" % ("Item", "Price"))  
# `Item` L-aligned 15 total spaces, `Price` R-aligned
print("-" * 25)                           
# Prints 25 dashes as a divider

# Table rows
print("%-15s $%9.2f" % ("Notebook", 3.50)) 
print("%-15s $%9.2f" % ("Pen", 1.25)) 
print("%-15s $%9.2f" % ("Eraser", 0.75))
```

**Output:**
```
Item                 Price
-------------------------
Notebook        $     3.50
Pen             $     1.25
Eraser          $     0.75
```

### Complete Table Example

```python
# Print a formatted grade table
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

**Output:**
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

### Formatting with Multiple Values

When using multiple values, wrap them in parentheses:

```python
# Multiple values in one format string
name = "Bob"
test1 = 85
test2 = 92
average = (test1 + test2) / 2

print("%-10s   Test 1: %3d   Test 2: %3d   Avg: %.1f" % (name, test1, test2, average))
# Output: Bob          Test 1:  85   Test 2:  92   Avg: 88.5
```

### Creating Separator Lines

Use string multiplication to create dividers:

```python
print("=" * 40)   # 40 equal signs
print("-" * 40)   # 40 dashes
print("*" * 40)   # 40 asterisks
```

### Table Formatting Checklist

1. **Headers**: Print column titles
2. **Separator**: Use dashes or equals to separate header from data
3. **Data rows**: Use consistent formatting for each row
4. **Alignment**: 
   - Left-align text (use `%-` width)
   - Right-align numbers (use `%` width)
5. **Decimal places**: Use `.2f` for money, `.1f` or `.0f` for other numbers
6. **Footer**: Add totals or summaries with separators

## Common Patterns

### Pattern 1: Sum of Even Numbers
```python
theSum = 0
for count in range(2, 11, 2):
    theSum += count
print(theSum)  # Output: 30 (2+4+6+8+10)
```

### Pattern 2: Product of a Range
```python
product = 1
for count in range(1, 6):
    product *= count
print(product)  # Output: 120 (1*2*3*4*5)
```

### Pattern 3: Counting by Tens
```python
for count in range(0, 101, 10):
    print(count, end=" ")
# Output: 0 10 20 30 40 50 60 70 80 90 100
```

## Important Points

1. **Range is exclusive on the upper bound**
   - `range(1, 5)` gives you 1, 2, 3, 4 (NOT 5)
   - To include 5, use `range(1, 6)`

2. **The `for loop` variable updates automatically**
   - You don't need to write `count = count + 1`
   - The range function handles this
   - **Tip for later**: the `while loop` does need a counter, or it will run forever

3. **Steps can be any integer**
   - Positive: count up
   - Negative: count down
   - The step cannot be zero!

4. **Format strings require the right number of values**
   - `"%s %d" % ("Hi", 5)` ✓ Correct
   - `"%s %d" % ("Hi")` ✗ Wrong - needs 2 values

## Common Mistakes

### Mistake 1: Wrong Upper Bound
```python
# Want to sum 1 through 10, but this only sums 1 through 9
for num in range(1, 10):  # Should be range(1, 11)
    theSum += num
```

### Mistake 2: Zero Step
```python
# This causes an error!
for i in range(1, 10, 0):  # ValueError: range() arg 3 must not be zero
    print(i)
```

### Mistake 3: Backwards Range
```python
# This produces no output!
for i in range(10, 1):  # Need a negative step!
    print(i)

# Correct version:
for i in range(10, 1, -1):
    print(i)
```

### Mistake 4: Format String Mismatch
```python
# Wrong number of values
print("Name: %s Age: %d" % ("Alice"))  # Error! Need 2 values

# Correct:
print("Name: %s Age: %d" % ("Alice", 15))

# Wrong type
print("Number: %d" % 3.14)  # Works but truncates to 3
print("Number: %f" % 3.14)  # Correct for decimal
```

## Practice Exercise

Try this in IDLE or VS Code:

```python
# Experiment with different range values
print("Range(5):", list(range(5)))
print("Range(2, 8):", list(range(2, 8)))
print("Range(0, 10, 2):", list(range(0, 10, 2)))
print("Range(10, 0, -1):", list(range(10, 0, -1)))

# Practice formatting
print("\nFormatting Practice:")
print("%-10s %5d" % ("Item", 123))
print("Price: $%.2f" % 19.5)
print("=" * 20)
```

Run this and make sure you understand why each output is what it is!