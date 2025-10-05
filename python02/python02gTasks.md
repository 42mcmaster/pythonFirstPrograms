# Lesson 2g Tasks: Program Structure and Best Practices

## Task 1: Program Structure Practice

Create a file called `well_structured.py` that follows the proper structure:

```python
"""
[Your docstring here with program name, author, date, purpose]
"""

# === IMPORTS ===
import math

# === CONSTANTS ===
# Define at least 2 constants

# === INPUT ===
# Get at least 2 inputs from user

# === PROCESSING ===
# Perform some calculations

# === OUTPUT ===
# Display results nicely formatted
```

Choose your own program idea (calculator, converter, etc.)

## Task 2: Refactor a Messy Program

Here's a poorly structured program. Rewrite it following best practices:

```python
x=input("number: ")
y=input("number: ")
print(int(x)+int(y))
print(int(x)*int(y))
```

Save as `refactored.py` with:
- Proper docstring
- Good variable names
- Comments
- Nice output formatting
- All 6 program sections

## Task 3: Grade Calculator

Create a file called `grade_calc.py` that:

1. Has a complete docstring
2. Asks for scores on 4 assignments
3. Calculates the average
4. Determines letter grade:
   - A: 90-100
   - B: 80-89
   - C: 70-79
   - D: 60-69
   - F: below 60
5. Displays results in a nice format

Follow all best practices from this lesson!

## Task 4: Shopping Cart Calculator

Create a file called `shopping_cart.py` with proper structure that:

1. Asks for 3 items and their prices
2. Calculates subtotal
3. Applies sales tax (use a constant)
4. Calculates total
5. Displays a formatted receipt

**Example output:**
```
========================================
           RECEIPT
========================================
Item 1:           $12.99
Item 2:           $8.50
Item 3:           $15.25
----------------------------------------
Subtotal:         $36.74
Tax (7%):         $2.57
Total:            $39.31
========================================
```

## Task 5: Unit Converter

Create a file called `unit_converter.py` that:

1. Converts between units (your choice):
   - Temperature (F ↔ C)
   - Distance (miles ↔ km)
   - Weight (lbs ↔ kg)
2. Uses constants for conversion factors
3. Has proper structure and documentation
4. Displays results with appropriate units

## Task 6: Code Review Checklist

Create a program called `age_calculator.py`, then use this checklist to review it:

**Documentation:**
- [ ] Has docstring with all required info
- [ ] Has comments for complex sections
- [ ] Variable names are clear and descriptive

**Structure:**
- [ ] Imports at top
- [ ] Constants in UPPERCASE
- [ ] Clear sections (Input, Processing, Output)
- [ ] Blank lines separate sections

**Code Quality:**
- [ ] No magic numbers (unexplained constants)
- [ ] Consistent naming style
- [ ] Proper indentation (4 spaces)
- [ ] Lines under 79 characters

**Functionality:**
- [ ] Runs without errors
- [ ] Input converted to correct types
- [ ] Output is formatted nicely
- [ ] Results are labeled clearly

## Task 7: Fix the Style

This code works but has terrible style. Fix it:

```python
import math
x=float(input("radius:"))
a=math.pi*x**2
c=2*math.pi*x
print(a)
print(c)
```

Save as `circle_fixed.py` with:
- Docstring
- Good variable names
- Constants where appropriate
- Comments
- Nice output formatting

## Task 8: Terminal Practice

Create a file called `hello_terminal.py` that:

```python
"""
Program: hello_terminal.py
A simple program to practice running from terminal
"""

name = input("What's your name? ")
age = int(input("How old are you? "))

print(f"\nHello {name}!")
print(f"In 10 years, you'll be {age + 10} years old.")

input("\nPress Enter to exit...")
```

Then:
1. Save it to your Desktop or Documents
2. Open a terminal/command prompt
3. Navigate to the file location
4. Run it with: `python3 hello_terminal.py`

Take a screenshot of it running in the terminal!

## Task 9: Loan Calculator

Create a file called `loan_calculator.py` that:

1. Follows perfect structure
2. Calculates monthly loan payment using:
   - M = P × [r(1+r)^n] / [(1+r)^n - 1]
   - P = principal (loan amount)
   - r = monthly interest rate (annual rate / 12)
   - n = number of months
3. Uses constants appropriately
4. Formats output as money
5. Is well-documented

## Task 10: Debug These Programs

Each program has errors. Find and fix them:

### Program A: `debug_a.py`
```python
"""Tax Calculator"""
price = input("Price: ")
tax = price * 0.07
print("Tax: " + tax)
```

### Program B: `debug_b.py`
```python
"""Circle Area"""
import Math
radius = float(input("Radius: "))
area = Math.pi * radius ** 2
print(f"Area: {area}")
```

### Program C: `debug_c.py`
```python
"""Average Calculator
score1 = 85
score2 = 90
score3 = 88
average = score1 + score2 + score3 / 3
print("Average:", average)
```

Save fixed versions with `_fixed` added to filenames.

## Task 11: Complete Program: Student Report

Create a file called `student_report.py` that:

1. Has complete documentation
2. Asks for:
   - Student name
   - Student ID
   - 3 test scores
   - 1 final exam score (worth double)
3. Calculates weighted average
4. Determines letter grade
5. Displays a formatted report card

**Example output:**
```
========================================
         STUDENT REPORT CARD
========================================
Name:         Alice Johnson
ID:           12345
----------------------------------------
Test 1:       85
Test 2:       90
Test 3:       88
Final Exam:   92 (×2)
----------------------------------------
Average:      89.0
Grade:        B
========================================
```

## Task 12: Style Comparison

Create TWO versions of the same program:

**`messy_version.py`:**
- No docstring
- Poor variable names
- No comments
- No formatting
- But it works!

**`clean_version.py`:**
- Perfect structure
- Great documentation
- Clear variable names
- Nice formatting

Choose a simple program (temperature converter, tip calculator, etc.)

Compare them - which is easier to understand?

## Challenge Task 1: Complete Application

Create a file called `bmi_analyzer.py` that:

1. Calculates BMI: weight(kg) / height(m)²
2. Determines category:
   - Underweight: < 18.5
   - Normal: 18.5-24.9
   - Overweight: 25-29.9
   - Obese: ≥ 30
3. Follows perfect structure
4. Has excellent documentation
5. Produces professional-looking output
6. Includes input validation (checks for positive numbers)

## Challenge Task 2: Multi-Function Program

Create `math_suite.py` that:

1. Shows a menu of operations:
   - Circle calculations
   - Triangle calculations
   - Rectangle calculations
   - Sphere calculations
2. Lets user choose operation
3. Gets appropriate inputs
4. Calculates and displays results
5. Is perfectly structured and documented

## Challenge Task 3: Financial Calculator

Create `financial_planner.py` that:

1. Asks for:
   - Monthly income
   - Monthly expenses
   - Savings goal
   - Current savings
2. Calculates:
   - Monthly savings (income - expenses)
   - Months to reach goal
   - Percentage of income being saved
3. Displays comprehensive report
4. Uses constants for tax rates, etc.
5. Is production-quality code

## Testing Task

Create `test_cases.py` that tests one of your programs with:

1. Normal input
2. Edge cases (very large/small numbers)
3. Zero values
4. Decimal values vs integers

Document the results of each test.

## Code Review Task

Exchange programs with a classmate (or review your own old code):

1. Use the best practices checklist
2. Identify 3 things done well
3. Identify 3 things to improve
4. Write suggestions in comments
5. Create a `code_review.txt` file with feedback

## Reflection: Best Practices

Answer in `best_practices_reflection.txt`:

1. Why is program structure important?

2. How do good variable names help you and others understand code?

3. What's the purpose of a docstring? Why put it at the top?

4. Why use constants instead of just typing numbers in your calculations?

5. How does adding `input("\nPress Enter to exit...")` help?

6. What was the hardest part about following all the best practices?

7. Look at a program you wrote at the beginning of this chapter. How would you improve it now?

## Final Project: Chapter 2 Showcase

Create `chapter2_showcase.py` that demonstrates EVERYTHING you learned:

**Requirements:**
- ✓ Perfect program structure (all 6 sections)
- ✓ Complete, professional docstring
- ✓ Import at least one module
- ✓ Use constants appropriately
- ✓ Get user input (multiple types)
- ✓ Perform calculations using various operators
- ✓ Use type conversions
- ✓ Call functions with arguments
- ✓ Format output beautifully
- ✓ Include comments where helpful
- ✓ Follow all PEP 8 conventions
- ✓ Add pause before exit

**Choose from:**
- Complete budget calculator
- Grade management system
- Fitness tracker
- Recipe scaler
- Travel planner
- Or your own idea!

Make it your best work - this represents everything from Chapter 2!

## Submission Checklist

Files to submit:
- [ ] `well_structured.py`
- [ ] `refactored.py`
- [ ] `grade_calc.py`
- [ ] `shopping_cart.py`
- [ ] `unit_converter.py`
- [ ] `age_calculator.py`
- [ ] `circle_fixed.py`
- [ ] `hello_terminal.py` (+ screenshot)
- [ ] `loan_calculator.py`
- [ ] `debug_a_fixed.py`
- [ ] `debug_b_fixed.py`
- [ ] `debug_c_fixed.py`
- [ ] `student_report.py`
- [ ] `messy_version.py`
- [ ] `clean_version.py`
- [ ] `best_practices_reflection.txt`
- [ ] `chapter2_showcase.py`
- [ ] (Optional) Challenge tasks

## Final Checklist for Every Program

Before submitting ANY program, verify:

**Documentation:**
- [ ] Docstring with: name, author, date, purpose, inputs, outputs
- [ ] Comments explain WHY, not just WHAT
- [ ] Complex sections have explanatory comments

**Structure:**
- [ ] Imports at very top
- [ ] Constants clearly defined (UPPERCASE)
- [ ] Logical flow: Input → Process → Output
- [ ] Blank lines separate major sections

**Naming:**
- [ ] Variables use lowercase_with_underscores
- [ ] Constants use UPPERCASE_WITH_UNDERSCORES
- [ ] Names are descriptive (no x, y, temp)

**Code Quality:**
- [ ] Proper indentation (4 spaces, consistent)
- [ ] No lines over 79 characters
- [ ] Spaces around operators
- [ ] No magic numbers (unexplained values)

**Functionality:**
- [ ] Runs without errors
- [ ] Handles expected inputs correctly
- [ ] Output is formatted nicely
- [ ] Results are clearly labeled

## Going Further (Optional)

1. Research Python's `argparse` module for handling command-line arguments

2. Explore Python IDEs (PyCharm, VSCode) and compare to IDLE

3. Learn about virtual environments for Python projects

4. Read the full PEP 8 style guide: https://pep8.org/

5. Create a personal style guide for your Python projects

## Congratulations!

You've completed Chapter 2! You now know:

- How to structure professional Python programs
- Best practices for clean, readable code
- How to run programs from the terminal
- How to debug common errors
- How to write well-documented code

These skills form the foundation for everything you'll do in Python. Keep practicing and always strive to write clean, professional code!