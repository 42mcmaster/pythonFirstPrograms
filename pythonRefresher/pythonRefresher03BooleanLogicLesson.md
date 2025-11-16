---
marp: true
theme: default
paginate: true
---

# Python Refresher 03
## Boolean Logic (and, or, not)

**Medina County Career Center**
Instructor: Mr. McMaster

---

## Learning Objectives

By the end of this lesson, you will be able to:
- Use `and` to combine conditions
- Use `or` to check alternative conditions
- Use `not` to reverse conditions
- Combine multiple logical operators
- Write complex conditional statements

---

## What is Boolean Logic?

**Boolean logic** lets you combine multiple conditions.

Instead of checking just one thing, you can check multiple things:
- "Is it raining **AND** cold?" → Wear a warm, waterproof jacket
- "Do you have a pen **OR** pencil?" → You can take the test
- "Is it **NOT** a school day?" → Sleep in!

---

## Boolean Values

There are only two Boolean values:
- `True`
- `False`

Every condition evaluates to one of these:

```python
print(5 > 3)    # True
print(5 < 3)    # False
print(5 == 5)   # True
```

---

## The and Operator

`and` requires **BOTH** conditions to be True.

```python
age = 17
has_license = True

if age >= 16 and has_license:
    print("You can drive!")
else:
    print("You cannot drive yet.")
```

Both conditions must be True for the message to print.

---

## How and Works

| Condition 1 | Condition 2 | Result |
|-------------|-------------|--------|
| True | True | **True** |
| True | False | False |
| False | True | False |
| False | False | False |

**Both must be True** for the result to be True.

---

## Example: Age Range Check

```python
age = int(input("Enter your age: "))

if age >= 13 and age <= 19:
    print("You are a teenager.")
else:
    print("You are not a teenager.")
```

Must be at least 13 **AND** at most 19.

---

## The or Operator

`or` requires **AT LEAST ONE** condition to be True.

```python
day = input("What day is it? ")

if day == "Saturday" or day == "Sunday":
    print("It's the weekend!")
else:
    print("It's a weekday.")
```

If **either** condition is True, the message prints.

---

## How or Works

| Condition 1 | Condition 2 | Result |
|-------------|-------------|--------|
| True | True | **True** |
| True | False | **True** |
| False | True | **True** |
| False | False | False |

**At least one must be True** for the result to be True.

---

## Example: Multiple Valid Answers

```python
answer = input("Is water wet? (yes/y/true) ").lower()

if answer == "yes" or answer == "y" or answer == "true":
    print("Correct!")
else:
    print("Incorrect.")
```

Any of the three options will work.

---

## The not Operator

`not` reverses a condition (True becomes False, False becomes True).

```python
is_raining = False

if not is_raining:
    print("You don't need an umbrella.")
else:
    print("Bring an umbrella!")
```

---

## How not Works

| Original | Result |
|----------|--------|
| True | False |
| False | True |

`not` simply flips the Boolean value.

---

## Example: not with Comparisons

```python
age = 25

if not age < 18:
    print("You are an adult.")

# This is the same as:
if age >= 18:
    print("You are an adult.")
```

Often there are simpler ways to write the same logic!

---

## Combining and, or, not

You can combine multiple operators:

```python
age = 16
has_license = True
has_car = False

if age >= 16 and has_license and not has_car:
    print("You can drive, but you need a car!")
```

---

## Order of Operations

When combining operators, Python evaluates in this order:
1. `not` (highest priority)
2. `and`
3. `or` (lowest priority)

Use **parentheses** to make your intent clear!

---

## Example: Parentheses for Clarity

```python
# Without parentheses (might be confusing)
if age >= 16 and has_license or has_permit:
    print("You can drive")

# With parentheses (much clearer)
if age >= 16 and (has_license or has_permit):
    print("You can drive")
```

---

## Example: Eligibility Check

```python
age = int(input("Enter your age: "))
gpa = float(input("Enter your GPA: "))

if (age >= 16 and age <= 18) and gpa >= 3.0:
    print("You are eligible for the scholarship!")
else:
    print("You do not meet the requirements.")
```

---

## Example: Valid Input Check

```python
answer = input("Enter yes or no: ").lower()

if answer != "yes" and answer != "no":
    print("Invalid input! Please enter yes or no.")
else:
    print("Thank you for your response.")
```

---

## Common Mistake: Redundant Comparisons

❌ **INEFFICIENT:**
```python
if x == 5 or x == 6 or x == 7 or x == 8:
    print("x is between 5 and 8")
```

✅ **BETTER:**
```python
if x >= 5 and x <= 8:
    print("x is between 5 and 8")
```

---

## Common Mistake: Wrong Syntax

❌ **WRONG:**
```python
if age >= 13 and <= 19:  # Error!
    print("Teenager")
```

✅ **CORRECT:**
```python
if age >= 13 and age <= 19:
    print("Teenager")
```

---

## Practice: Grade and Attendance

```python
grade = int(input("Enter your grade: "))
absences = int(input("Enter number of absences: "))

if grade >= 60 and absences <= 3:
    print("You pass the class!")
elif grade >= 60 and absences > 3:
    print("Your grade is passing, but you have too many absences.")
elif grade < 60 and absences <= 3:
    print("You need to improve your grade.")
else:
    print("You are failing due to grade and absences.")
```

---

## Practice: Password Requirements

```python
password = input("Create a password: ")
length = len(password)

if length >= 8 and length <= 20:
    print("Password length is valid.")
else:
    print("Password must be between 8 and 20 characters.")
```

---

## Truth Tables Summary

**AND:** Both must be True
```
True and True = True
True and False = False
```

**OR:** At least one must be True
```
True or False = True
False or False = False
```

**NOT:** Flips the value
```
not True = False
not False = True
```

---

## When to Use Each Operator

**Use `and` when:**
- All conditions must be met
- "Must be 16 **and** have a license"

**Use `or` when:**
- Any condition can be met
- "Must pay cash **or** credit"

**Use `not` when:**
- You want to check the opposite
- "If **not** logged in, show login page"

---

## Complex Example

```python
age = int(input("Age: "))
is_student = input("Are you a student? (yes/no) ").lower() == "yes"
is_senior = age >= 65

if (age < 18 or is_senior or is_student):
    print("You get a discount!")
else:
    print("Regular price applies.")
```

Multiple conditions with different logic!

---

## Lesson Summary

✓ `and` requires all conditions to be True
✓ `or` requires at least one condition to be True
✓ `not` reverses a Boolean value
✓ Use parentheses to make complex logic clear
✓ Every condition evaluates to True or False
✓ Can combine multiple operators in one statement

---

## Task Time!

Open **python_refresher_03_task.py**

Complete the practice problems to master Boolean logic.

**Remember:**
- Test with different inputs
- Use parentheses when combining operators
- Think through your logic carefully!
