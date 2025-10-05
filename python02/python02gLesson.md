# Lesson 2f: Program Structure and Best Practices

## Learning Objectives
By the end of this lesson, you will be able to:
- Structure a complete Python program properly
- Follow Python coding conventions and best practices
- Run Python scripts from the terminal/command line
- Debug common errors in Python programs
- Write clean, readable, well-documented code

## The Structure of a Good Python Program

Every well-written Python program follows a similar structure:

```python
"""
1. DOCSTRING - Program documentation at the very top
"""

# 2. IMPORTS - All import statements
import math
from datetime import date

# 3. CONSTANTS - Values that never change (UPPERCASE names)
TAX_RATE = 0.07
MAX_SCORE = 100
PI = 3.14159

# 4. INPUT - Get data from the user
name = input("Enter your name: ")
age = int(input("Enter your age: "))

# 5. PROCESSING - Perform calculations and logic
years_to_100 = 100 - age
birth_year = date.today().year - age

# 6. OUTPUT - Display results
print(f"Hello {name}!")
print(f"You were born around {birth_year}")
print(f"You'll be 100 in about {years_to_100} years")
```

### The Six Components

1. **Docstring** - Explains what the program does, who wrote it, when, and any other important information
2. **Imports** - Bring in any needed modules
3. **Constants** - Define values that won't change
4. **Input** - Gather information needed for the program
5. **Processing** - Do calculations and make decisions
6. **Output** - Display results to the user

## Complete Example: Tax Calculator

```python
"""
Program: tax_calculator.py
Author: Jordan Smith
Date: March 15, 2024

Purpose: Calculate sales tax and total cost for a purchase
Input: Item price and quantity
Output: Subtotal, tax amount, and total cost
"""

# Imports
import math

# Constants
SALES_TAX_RATE = 0.07  # 7% sales tax
CURRENCY_SYMBOL = "$"

# Input Section
print("=" * 40)
print("Sales Tax Calculator")
print("=" * 40)

price = float(input("Enter item price: $"))
quantity = int(input("Enter quantity: "))

# Processing Section
subtotal = price * quantity
tax = subtotal * SALES_TAX_RATE
total = subtotal + tax

# Round to 2 decimal places for money
tax = round(tax, 2)
total = round(total, 2)

# Output Section
print("\n" + "=" * 40)
print("Receipt")
print("=" * 40)
print(f"Price per item: {CURRENCY_SYMBOL}{price:.2f}")
print(f"Quantity:       {quantity}")
print(f"Subtotal:       {CURRENCY_SYMBOL}{subtotal:.2f}")
print(f"Tax ({SALES_TAX_RATE * 100}%):      {CURRENCY_SYMBOL}{tax:.2f}")
print(f"Total:          {CURRENCY_SYMBOL}{total:.2f}")
print("=" * 40)
```

## Python Coding Conventions (PEP 8)

Python has official style guidelines called **PEP 8**. Following these makes your code easier to read and more professional.

### Variable Naming

```python
# ✅ Good - lowercase with underscores
student_name = "Alice"
final_score = 95
total_points = 100

# ❌ Bad - inconsistent style
StudentName = "Alice"
finalScore = 95
TOTAL_POINTS = 100  # This looks like a constant!

# ✅ Constants - all uppercase
MAX_STUDENTS = 30
TAX_RATE = 0.07
PI = 3.14159
```

### Spacing and Indentation

```python
# ✅ Good - spaces around operators
total = price + tax
average = (a + b + c) / 3

# ❌ Bad - no spaces
total=price+tax
average=(a+b+c)/3

# ✅ Good - 4 spaces for indentation (not tabs!)
if age >= 18:
    print("Adult")
    print("Can vote")

# ✅ Good - blank lines between sections
name = input("Name: ")
age = int(input("Age: "))

result = age * 2
print(result)
```

### Comments

```python
# ✅ Good - helpful, explains WHY
age = age + 1  # Calculate age on next birthday

# ❌ Bad - obvious, explains WHAT
age = age + 1  # Add 1 to age

# ✅ Good - explains complex logic
# Convert Fahrenheit to Celsius using standard formula
celsius = (fahrenheit - 32) * 5 / 9

# ✅ Good - section headers
# === INPUT SECTION ===
name = input("Name: ")
age = int(input("Age: "))

# === PROCESSING ===
result = calculate_score(age)
```

### Line Length

Keep lines under 79 characters when possible:

```python
# ✅ Good - readable
message = "This is a long message that needs to be " + \
          "split across multiple lines for readability"

# ✅ Better - using parentheses
message = ("This is a long message that needs to be "
           "split across multiple lines for readability")

# ❌ Bad - too long
message = "This is a very long message that goes on and on and on and makes the code hard to read"
```

## Running Python Programs from Terminal

### Opening a Terminal

**Windows:**
1. Press Windows key
2. Type "Command Prompt" or "cmd"
3. Press Enter

**Mac:**
1. Press Cmd + Space
2. Type "Terminal"
3. Press Enter

### Navigate to Your File

Use `cd` (change directory) to navigate:

```bash
# See current directory
pwd  # Mac/Linux
cd   # Windows

# List files
ls   # Mac/Linux
dir  # Windows

# Change to a directory
cd Documents
cd pythonfiles

# Go up one level
cd ..
```

### Run Your Program

```bash
python3 program_name.py
# or
python program_name.py
```

**Example:**
```bash
cd Documents/python_programs
python3 tax_calculator.py
```

### The Fly-By Window Problem

If you double-click a Python file, the window might close immediately after running. **Solution:** Add this line at the end:

```python
input("\nPress Enter to exit...")
```

## Debugging Common Errors

### Syntax Errors

**Problem:** Forgetting quotes, parentheses, or colons

```python
# ❌ Error - missing quotes
print(Hello)

# ✅ Fixed
print("Hello")

# ❌ Error - missing colon
if age > 18
    print("Adult")

# ✅ Fixed
if age > 18:
    print("Adult")
```

### Type Errors

**Problem:** Using wrong type in operation

```python
# ❌ Error - can't add string and int
age = input("Age: ")
next_year = age + 1

# ✅ Fixed - convert to int first
age = int(input("Age: "))
next_year = age + 1
```

### Name Errors

**Problem:** Using undefined variables or misspelling

```python
# ❌ Error - variable not defined
print(total)

# ✅ Fixed - define first
total = 0
print(total)

# ❌ Error - typo
student_name = "Alice"
print(studnet_name)

# ✅ Fixed - correct spelling
print(student_name)
```

### Value Errors

**Problem:** Invalid conversion

```python
# ❌ Error - can't convert "hello" to int
age = int("hello")

# ✅ Fixed - validate input first
age_str = input("Age: ")
if age_str.isdigit():
    age = int(age_str)
else:
    print("Invalid number!")
```

## Best Practices Checklist

Use this checklist for every program you write:

### Documentation
- [ ] Docstring at the top with program info
- [ ] Comments explaining complex sections
- [ ] Clear variable names (no `x`, `y`, `temp`)

### Structure
- [ ] Imports at the top
- [ ] Constants in UPPERCASE
- [ ] Logical flow: Input → Processing → Output
- [ ] Blank lines between sections

### Code Quality
- [ ] Meaningful variable names
- [ ] Consistent naming style
- [ ] Proper indentation (4 spaces)
- [ ] No lines over 79 characters

### Functionality
- [ ] Input converted to correct types
- [ ] Results formatted nicely
- [ ] Program runs without errors
- [ ] Output is clear and labeled

## Example: Well-Structured Program

```python
"""
Program: grade_calculator.py
Author: Alex Johnson
Date: March 15, 2024

Calculate final grade based on assignments, midterm, and final exam.
Weights: Assignments 40%, Midterm 30%, Final 30%

Input: Three scores (0-100)
Output: Weighted average and letter grade
"""

# === IMPORTS ===
import math

# === CONSTANTS ===
ASSIGNMENT_WEIGHT = 0.40
MIDTERM_WEIGHT = 0.30
FINAL_WEIGHT = 0.30

# === INPUT SECTION ===
print("Grade Calculator")
print("=" * 40)

assignment_score = float(input("Enter assignment average (0-100): "))
midterm_score = float(input("Enter midterm score (0-100): "))
final_score = float(input("Enter final exam score (0-100): "))

# === PROCESSING SECTION ===
# Calculate weighted average
weighted_avg = (assignment_score * ASSIGNMENT_WEIGHT +
                midterm_score * MIDTERM_WEIGHT +
                final_score * FINAL_WEIGHT)

# Round to 2 decimal places
weighted_avg = round(weighted_avg, 2)

# Determine letter grade
if weighted_avg >= 90:
    letter_grade = "A"
elif weighted_avg >= 80:
    letter_grade = "B"
elif weighted_avg >= 70:
    letter_grade = "C"
elif weighted_avg >= 60:
    letter_grade = "D"
else:
    letter_grade = "F"

# === OUTPUT SECTION ===
print("\n" + "=" * 40)
print("Final Results")
print("=" * 40)
print(f"Assignments: {assignment_score:.1f}")
print(f"Midterm:     {midterm_score:.1f}")
print(f"Final Exam:  {final_score:.1f}")
print("-" * 40)
print(f"Weighted Average: {weighted_avg:.2f}")
print(f"Letter Grade:     {letter_grade}")
print("=" * 40)

# Prevent window from closing immediately
input("\nPress Enter to exit...")
```

## Testing Your Programs

Always test your programs with different inputs:

### Test Cases to Try

1. **Normal values** - Typical expected input
2. **Edge cases** - Minimum and maximum values
3. **Invalid input** - What if user enters text instead of numbers?
4. **Zero** - Does your program handle zero correctly?
5. **Negative numbers** - If applicable

**Example Test Plan for Tax Calculator:**

| Test | Input | Expected Output |
|------|-------|----------------|
| Normal | Price: $10, Qty: 2 | Total: $21.40 |
| Large | Price: $1000, Qty: 10 | Total: $10,700 |
| Decimal | Price: $5.99, Qty: 3 | Total: $19.22 |
| One item | Price: $15, Qty: 1 | Total: $16.05 |

## Summary

- Well-structured programs have: docstring, imports, constants, input, processing, output
- Follow PEP 8 style guidelines for professional code
- Use meaningful variable names and comments
- Test programs with various inputs
- Run programs from terminal with `python3 filename.py`
- Add `input()` at end to prevent window from closing
- Debug errors systematically: read error messages carefully
- Keep code organized and readable

## Key Terms

- **PEP 8** - Python's official style guide
- **Docstring** - Documentation string at top of program
- **Constant** - Variable that shouldn't change (UPPERCASE)
- **Edge Case** - Unusual or extreme input value
- **Terminal/Command Line** - Text-based interface for running programs
- **Syntax Error** - Code that doesn't follow Python's rules
- **Runtime Error** - Error that occurs while program is running

## Chapter 2 Review

Congratulations! You've completed Chapter 2. You've learned:

✓ Software development process and testing
✓ Strings and escape sequences
✓ Variables and naming conventions  
✓ Data types: int, float, str
✓ Arithmetic expressions and operators
✓ Type conversions (int(), float(), str())
✓ Getting user input
✓ Functions and return values
✓ Modules and importing
✓ Program structure and best practices

You now have the foundational skills to write complete, well-structured Python programs!

## Next Steps

In the next chapter, you'll learn about:
- Selection statements (if/elif/else)
- Boolean expressions and logic
- Making programs that make decisions
- More complex program flow

Keep practicing what you've learned in this chapter - these fundamentals are essential for everything that comes next!