---
marp: true
theme: default
paginate: true
---

# Python Refresher 02
## Conditionals (if/elif/else)

**Medina County Career Center**
Instructor: Mr. McMaster

---

## Learning Objectives

By the end of this lesson, you will be able to:
- Use `if` statements to make decisions
- Use `elif` for multiple conditions
- Use `else` for default cases
- Use comparison operators
- Write properly indented conditional code

---

## What are Conditionals?

**Conditionals** let your program make decisions.

Think of them like traffic lights:
- **IF** the light is green → go
- **ELSE IF** the light is yellow → slow down
- **ELSE** (it's red) → stop

---

## The if Statement

Basic syntax:

```python
if condition:
    # Code to run if condition is True
    print("The condition was true!")
```

**Important:** Notice the **indentation**! Python requires it.

---

## Simple Example

```python
age = 18

if age >= 18:
    print("You are an adult.")
```

If `age` is 18 or greater, the message prints.
Otherwise, nothing happens.

---

## Comparison Operators

Used to compare values:

| Operator | Meaning | Example |
|----------|---------|---------|
| `==` | Equal to | `x == 5` |
| `!=` | Not equal to | `x != 5` |
| `>` | Greater than | `x > 5` |
| `<` | Less than | `x < 5` |
| `>=` | Greater than or equal | `x >= 5` |
| `<=` | Less than or equal | `x <= 5` |

---

## Common Mistake: = vs ==

❌ **WRONG:**
```python
if age = 18:  # Error! This tries to assign, not compare
    print("Adult")
```

✅ **CORRECT:**
```python
if age == 18:  # This compares
    print("Adult")
```

---

## The else Statement

`else` runs when the `if` condition is False:

```python
age = 15

if age >= 18:
    print("You are an adult.")
else:
    print("You are not an adult yet.")
```

**Output:** `You are not an adult yet.`

---

## Indentation is Critical

✅ **CORRECT:**
```python
if age >= 18:
    print("Adult")
    print("Can vote")
```

❌ **WRONG:**
```python
if age >= 18:
print("Adult")      # Error! Not indented
    print("Can vote")
```

---

## The elif Statement

Use `elif` (else if) for multiple conditions:

```python
grade = 85

if grade >= 90:
    print("A")
elif grade >= 80:
    print("B")
elif grade >= 70:
    print("C")
else:
    print("Below C")
```

---

## How elif Works

Python checks conditions **in order**:
1. If the first condition is True → run that block, skip the rest
2. If False → check the next elif
3. If all conditions are False → run else (if present)

Only **one** block runs!

---

## Example: Grade Calculator

```python
score = int(input("Enter your score: "))

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")
```

---

## Example: Age Categories

```python
age = int(input("Enter your age: "))

if age < 13:
    print("You are a child.")
elif age < 20:
    print("You are a teenager.")
elif age < 65:
    print("You are an adult.")
else:
    print("You are a senior.")
```

---

## Comparing Strings

You can compare strings with `==` and `!=`:

```python
name = input("Enter your name: ")

if name == "Ryan":
    print("Hello, Mr. McMaster!")
else:
    print("Hello,", name)
```

**Note:** Comparison is case-sensitive!

---

## Making String Comparisons Flexible

```python
answer = input("Do you like pizza? (yes/no) ")

# Convert to lowercase so YES, Yes, yes all work
if answer.lower() == "yes":
    print("Pizza is great!")
else:
    print("More pizza for me!")
```

---

## Nested if Statements

You can put `if` statements inside other `if` statements:

```python
age = int(input("Enter your age: "))

if age >= 16:
    print("You can drive.")
    
    license = input("Do you have a license? (yes/no) ")
    if license.lower() == "yes":
        print("Great! Drive safely.")
    else:
        print("You need to get your license first.")
else:
    print("You're too young to drive.")
```

---

## Multiple Conditions in One Line

We'll cover this more in the next lesson, but here's a preview:

```python
# Later we'll use "and" and "or"
if age >= 16 and age < 18:
    print("You're a teenager who can drive.")
```

---

## Common Mistakes

**Mistake 1:** Forgetting the colon
```python
if age >= 18  # Missing colon!
    print("Adult")
```

**Fix:**
```python
if age >= 18:
    print("Adult")
```

---

## Common Mistakes

**Mistake 2:** Not indenting
```python
if age >= 18:
print("Adult")  # Not indented!
```

**Fix:**
```python
if age >= 18:
    print("Adult")
```

---

## Common Mistakes

**Mistake 3:** Using = instead of ==
```python
if name = "Sam":  # Wrong!
    print("Hi Sam")
```

**Fix:**
```python
if name == "Sam":
    print("Hi Sam")
```

---

## Practice Example

```python
# Simple number comparison program
num = int(input("Enter a number: "))

if num > 0:
    print("The number is positive.")
elif num < 0:
    print("The number is negative.")
else:
    print("The number is zero.")
```

---

## When to Use What

- **if** → Always needed to start a conditional
- **elif** → When you have multiple specific conditions to check
- **else** → When you want a default case (everything else)

You can have:
- `if` alone
- `if` and `else`
- `if`, `elif`, and `else`
- Multiple `elif` statements

---

## Decision Flow

```
Start
  ↓
Check if condition
  ↓
Is it True? → Yes → Run if block → End
  ↓
  No
  ↓
Check elif condition (if present)
  ↓
Is it True? → Yes → Run elif block → End
  ↓
  No
  ↓
Run else block (if present) → End
```

---

## Lesson Summary

✓ `if` statements make decisions based on conditions
✓ Use comparison operators: `==`, `!=`, `>`, `<`, `>=`, `<=`
✓ `elif` checks additional conditions
✓ `else` handles all other cases
✓ Always indent code inside conditionals
✓ Only one block runs (first True condition or else)

---

## Task Time!

Open **python_refresher_02_task.py**

Complete the practice problems to reinforce conditional statements.

**Remember:**
- Check your indentation
- Use `==` to compare, not `=`
- Test your code with different inputs!
