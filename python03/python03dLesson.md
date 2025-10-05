# Lesson 3d: Boolean Expressions and If Statements

## Learning Objectives
- Understand Boolean data types (True and False)
- Use comparison operators to create Boolean expressions
- Write if statements for one-way selection
- Write if-else statements for two-way selection
- Understand when selection statements are needed

## Boolean Data Type

Python has a special data type called **Boolean** (named after mathematician George Boole).

A Boolean value can only be:
- `True` 
- `False`

**Important:** These are capitalized in Python!

```python
>>> type(True)
<class 'bool'>
>>> type(False)
<class 'bool'>
```

## Comparison Operators

Comparison operators compare two values and return `True` or `False`.

| Operator | Meaning | Example | Result |
|----------|---------|---------|--------|
| `==` | Equals | `4 == 4` | `True` |
| `!=` | Not equals | `4 != 4` | `False` |
| `<` | Less than | `3 < 5` | `True` |
| `>` | Greater than | `5 > 3` | `True` |
| `<=` | Less than or equal | `3 <= 3` | `True` |
| `>=` | Greater than or equal | `5 >= 3` | `True` |

### Testing Comparisons

```python
>>> 4 == 4
True
>>> 4 != 4
False
>>> 10 > 5
True
>>> 10 < 5
False
>>> age = 16
>>> age >= 16
True
```

### Common Mistakes

```python
# WRONG - Using = instead of ==
if x = 5:  # SyntaxError!
    print("x is 5")

# CORRECT
if x == 5:
    print("x is 5")
```

**Remember:** 
- `=` is for assignment (storing a value)
- `==` is for comparison (checking equality)

## Selection Statements

**Selection statements** let your program make choices based on conditions.

Think of it like:
- "IF it's raining, bring an umbrella"
- "IF you're 16 or older, you can drive"

## One-Way Selection: The If Statement

Use an `if` statement when you want to do something only when a condition is true.

### Syntax

```python
if condition:
    statement1
    statement2
    # more statements...
```

### Example 1: Input Validation

```python
number = int(input("Enter a positive number: "))

if number <= 0:
    print("Error: That's not positive!")
    
print("Program continues...")
```

**What happens:**
- If the number is 0 or negative, the error prints
- Either way, "Program continues..." prints
- The indented code only runs if the condition is `True`

### Example 2: Minimum Value Check

```python
import math

area = float(input("Enter the circle's area: "))

if area > 0:
    radius = math.sqrt(area / math.pi)
    print(f"The radius is {radius}")

# If area is not > 0, nothing happens
```

### Flowchart of If Statement

```
    ↓
   [condition?]─── False ───→
    │ True
    ↓
  [statements]
    │
    ↓
```

## Two-Way Selection: The If-Else Statement

Use `if-else` when you want to do one thing OR another.

### Syntax

```python
if condition:
    # Do this if True
    statement1
else:
    # Do this if False
    statement2
```

### Example 1: Area Calculator with Error Handling

```python
import math

area = float(input("Enter the circle's area: "))

if area > 0:
    radius = math.sqrt(area / math.pi)
    print(f"The radius is {radius:.2f}")
else:
    print("Error: Area must be positive!")
```

**What happens:**
- If area > 0: calculates and prints radius
- If area ≤ 0: prints error message
- **Exactly one** of these blocks will run

### Example 2: Grade Pass/Fail

```python
grade = int(input("Enter your grade: "))

if grade >= 60:
    print("You passed!")
else:
    print("You did not pass.")
```

### Flowchart of If-Else Statement

```
         ↓
    [condition?]
    │         │
  True      False
    │         │
    ↓         ↓
[statements1] [statements2]
    │         │
    └────┬────┘
         ↓
```

## Practical Examples

### Example 1: Discount Calculator

```python
total = float(input("Enter purchase total: $"))

if total >= 100:
    discount = total * 0.10
    total = total - discount
    print(f"10% discount applied: ${discount:.2f}")
else:
    print("No discount (need $100 minimum)")

print(f"Final total: ${total:.2f}")
```

### Example 2: Age Verification

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("You are an adult.")
    print("You can vote!")
else:
    print("You are a minor.")
    years_until = 18 - age
    print(f"You can vote in {years_until} years.")

print("Thank you!")
```

### Example 3: Temperature Advisory

```python
temp = int(input("Enter temperature in °F: "))

if temp > 90:
    print("It's hot! Stay hydrated.")
    print("Avoid strenuous activity.")
else:
    print("Temperature is comfortable.")

print("Have a great day!")
```

## When to Use Which?

**Use `if` (one-way) when:**
- You might do something extra
- The action is optional
- Example: Check for errors, add a bonus

**Use `if-else` (two-way) when:**
- You'll do one thing OR another
- Both possibilities need handling
- Example: Pass/fail, accept/reject

## Key Points

1. **Indentation is critical**
   ```python
   # WRONG - not indented
   if x > 0:
   print("positive")  # Error!
   
   # CORRECT - indented
   if x > 0:
       print("positive")
   ```

2. **Don't forget the colon**
   ```python
   # WRONG
   if x > 0
       print("positive")  # Error!
   
   # CORRECT
   if x > 0:
       print("positive")
   ```

3. **Use == for comparison, not =**
   ```python
   # WRONG - assignment
   if x = 5:  # Error!
   
   # CORRECT - comparison
   if x == 5:
   ```

4. **Only one block executes in if-else**
   - Either the if block OR the else block
   - Never both, never neither

## Testing Your Understanding

What will this print?

```python
x = 10

if x > 5:
    print("A")
else:
    print("B")
    
print("C")
```

**Answer:** 
```
A
C
```

- `x > 5` is True, so "A" prints
- "C" is not indented, so it always prints

## Practice

Try these in IDLE or VS Code:

```python
# Experiment 1: Compare values
print(5 == 5)    # What prints?
print(5 != 5)    # What prints?
print(10 > 5)    # What prints?
print(3 >= 3)    # What prints?

# Experiment 2: Test an if statement
number = 7
if number > 5:
    print("Big number!")
print("Done")

# Experiment 3: Test if-else
number = 3
if number > 5:
    print("Big number!")
else:
    print("Small number!")
print("Done")
```

What do you expect each to print? Run them and find out!