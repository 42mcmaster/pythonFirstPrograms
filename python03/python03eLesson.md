# Lesson 3e: Multi-Way Selection Statements

## Learning Objectives
- Understand when to use multi-way selection
- Write if-elif-else statements
- Handle multiple conditions efficiently
- Avoid common multi-way selection errors
- Understand the order of condition checking

## The Problem

Sometimes we need to choose between MORE than two options:

**Grade Conversion:**
- A: 90-100
- B: 80-89
- C: 70-79
- D: 60-69
- F: below 60

We *could* use nested if-else statements, but that gets messy!

## The Solution: elif

Python provides `elif` (short for "else if") for multi-way selection.

### Syntax

```python
if condition1:
    # Runs if condition1 is True
    statements
elif condition2:
    # Runs if condition1 is False AND condition2 is True
    statements
elif condition3:
    # Runs if condition1 and condition2 are False AND condition3 is True
    statements
else:
    # Runs if all conditions are False
    statements
```

## Example 1: Grade Converter

```python
number = int(input("Enter the numeric grade: "))

if number > 89:
    letter = 'A'
elif number > 79:
    letter = 'B'
elif number > 69:
    letter = 'C'
elif number > 59:
    letter = 'D'
else:
    letter = 'F'

print(f"The letter grade is {letter}")
```

**Sample Runs:**
```
Enter the numeric grade: 95
The letter grade is A

Enter the numeric grade: 75
The letter grade is C

Enter the numeric grade: 55
The letter grade is F
```

### How It Works

The program checks conditions **in order** from top to bottom:

1. If `number > 89`: assigns 'A' and **stops** (skips rest)
2. Else if `number > 79`: assigns 'B' and **stops**
3. Else if `number > 69`: assigns 'C' and **stops**
4. Else if `number > 59`: assigns 'D' and **stops**
5. Else (none above): assigns 'F'

**Key Point:** Only ONE block executes! Once a condition is True, the rest are skipped.

## Example 2: Temperature Categories

```python
temp = int(input("Enter temperature in °F: "))

if temp >= 100:
    print("Extremely hot!")
    print("Stay indoors if possible.")
elif temp >= 85:
    print("Very warm.")
    print("Stay hydrated.")
elif temp >= 70:
    print("Pleasant weather.")
elif temp >= 50:
    print("Cool weather.")
    print("Bring a jacket.")
else:
    print("Cold weather!")
    print("Dress warmly.")

print("Have a great day!")
```

## Example 3: Menu System

```python
print("Menu:")
print("1. Start Game")
print("2. Load Game")
print("3. Settings")
print("4. Quit")

choice = int(input("Enter choice: "))

if choice == 1:
    print("Starting new game...")
elif choice == 2:
    print("Loading saved game...")
elif choice == 3:
    print("Opening settings...")
elif choice == 4:
    print("Goodbye!")
else:
    print("Invalid choice!")
```

## Order Matters!

The order of conditions is VERY important!

### Wrong Order Example

```python
# WRONG - will never give C, D, or F!
if number > 59:
    letter = 'D'  # This catches 60-100!
elif number > 69:
    letter = 'C'  # Never reached
elif number > 79:
    letter = 'B'  # Never reached
elif number > 89:
    letter = 'A'  # Never reached
else:
    letter = 'F'
```

If `number = 95`:
- Checks: 95 > 59? **Yes!** → Assigns 'D' and stops
- Never checks the rest!

### Correct Order

```python
# CORRECT - most restrictive first
if number > 89:    # 90-100
    letter = 'A'
elif number > 79:  # 80-89
    letter = 'B'
elif number > 69:  # 70-79
    letter = 'C'
elif number > 59:  # 60-69
    letter = 'D'
else:              # 0-59
    letter = 'F'
```

**Rule:** Put most restrictive (specific) conditions first!

## When else is Optional

Sometimes you don't need the `else`:

```python
day = int(input("Enter day (1-7): "))

if day == 1:
    print("Monday")
elif day == 2:
    print("Tuesday")
elif day == 3:
    print("Wednesday")
elif day == 4:
    print("Thursday")
elif day == 5:
    print("Friday")
elif day == 6:
    print("Saturday")
elif day == 7:
    print("Sunday")
# No else - if input is invalid, nothing prints
```

But it's often better to include it for error handling:

```python
# Better - handles invalid input
if day == 1:
    print("Monday")
elif day == 2:
    print("Tuesday")
# ... etc ...
else:
    print("Invalid day!")
```

## Flowchart

```
         ↓
    [condition1?]──False──→[condition2?]──False──→[condition3?]──False──→[else]
         │True                 │True                 │True                  │
         ↓                     ↓                     ↓                      ↓
    [statements1]         [statements2]         [statements3]         [statements4]
         │                     │                     │                      │
         └──────────────────┬──┴──────────────────┬──┴──────────────────────┘
                            ↓
```

## Complete Example: BMI Calculator

```python
weight = float(input("Enter weight in pounds: "))
height = float(input("Enter height in inches: "))

bmi = (weight / (height ** 2)) * 703

print(f"Your BMI is {bmi:.1f}")

if bmi < 18.5:
    print("You are underweight.")
elif bmi < 25:
    print("You are at a healthy weight.")
elif bmi < 30:
    print("You are overweight.")
else:
    print("You are obese.")

print("Consult a doctor for health advice.")
```

## Multiple Statements in Each Block

Each block can have multiple statements:

```python
grade = int(input("Enter grade: "))

if grade >= 90:
    letter = 'A'
    print("Excellent work!")
    print("Keep it up!")
elif grade >= 80:
    letter = 'B'
    print("Good job!")
elif grade >= 70:
    letter = 'C'
    print("Satisfactory.")
elif grade >= 60:
    letter = 'D'
    print("You passed, but study more.")
else:
    letter = 'F'
    print("You did not pass.")
    print("Please see the teacher.")

print(f"Your grade is: {letter}")
```

## Common Mistakes

### Mistake 1: Wrong Comparison Operators

```python
# WRONG - Using >= when > is needed
if number >= 90:  # 90 counts as A
    letter = 'A'
elif number >= 80:  # But 90 is also >= 80!
    letter = 'B'    # Never reached for 90+!
```

### Mistake 2: Overlapping Conditions

```python
# WRONG - conditions overlap
if age < 18:
    print("Minor")
elif age < 21:  # OK
    print("Young adult")
elif age < 65:  # OK
    print("Adult")
elif age > 50:  # BAD! Overlaps with age < 65
    print("Senior")  # Never reached!
```

### Mistake 3: Using Multiple Separate Ifs

```python
# WRONG - inefficient, checks all conditions
if grade >= 90:
    letter = 'A'
if grade >= 80:  # Still checks even if grade was 95!
    letter = 'B'  # OVERWRITES the A!
if grade >= 70:
    letter = 'C'
# Result: grade 95 gets letter = 'C' (WRONG!)

# CORRECT - use elif
if grade >= 90:
    letter = 'A'
elif grade >= 80:  # Skipped if grade >= 90
    letter = 'B'
elif grade >= 70:  # Skipped if grade >= 80
    letter = 'C'
```

## Practice Problem

What letter grade does this give for a grade of 85?

```python
if number > 89:
    letter = 'A'
elif number > 79:
    letter = 'B'
elif number > 69:
    letter = 'C'
else:
    letter = 'F'
```

**Answer:** B
- 85 > 89? No
- 85 > 79? **Yes!** → letter = 'B', done

## Key Takeaways

1. Use `elif` for multiple conditions (not multiple `if` statements)
2. Only ONE block executes in an if-elif-else chain
3. Order conditions from most to least restrictive
4. The `else` is optional but useful for error handling
5. Once a condition is True, the rest are skipped
6. Each block can have multiple statements