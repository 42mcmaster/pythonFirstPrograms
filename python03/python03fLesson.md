# Lesson 3f: Logical Operators and Compound Conditions

## Learning Objectives
- Use logical operators: and, or, not
- Create compound Boolean expressions
- Understand truth tables
- Apply short-circuit evaluation
- Simplify complex conditions

## The Problem

Sometimes we need to check multiple conditions at once:

- "If it's a weekend AND it's sunny, go to the beach"
- "If your grade is less than 0 OR greater than 100, print an error"
- "If the password is NOT correct, deny access"

We need a way to combine simple conditions!

## Logical Operators

Python has three logical operators:

| Operator | Meaning | Example |
|----------|---------|---------|
| `and` | Both must be True | `age >= 18 and age < 65` |
| `or` | At least one must be True | `day == 'Sat' or day == 'Sun'` |
| `not` | Reverses the condition | `not is_raining` |

## The AND Operator

`and` returns `True` only if BOTH conditions are `True`.

### Truth Table for AND

| A | B | A and B |
|---|---|---------|
| True | True | **True** |
| True | False | False |
| False | True | False |
| False | False | False |

### Examples

```python
# Both must be True
>>> True and True
True
>>> True and False
False
>>> False and True
False
>>> False and False
False

# In conditions
>>> age = 25
>>> age >= 18 and age < 65
True  # Both conditions are True

>>> temperature = 65
>>> temperature >= 60 and temperature <= 75
True  # Nice weather!
```

### Practical Example: Range Checking

```python
# Check if grade is valid (between 0 and 100)
number = int(input("Enter grade: "))

if number >= 0 and number <= 100:
    # Process the grade
    print("Valid grade")
else:
    print("Error: Grade must be between 0 and 100")
```

## The OR Operator

`or` returns `True` if AT LEAST ONE condition is `True`.

### Truth Table for OR

| A | B | A or B |
|---|---|--------|
| True | True | True |
| True | False | **True** |
| False | True | **True** |
| False | False | False |

### Examples

```python
# At least one must be True
>>> True or True
True
>>> True or False
True  # One is True!
>>> False or True
True  # One is True!
>>> False or False
False  # Both are False

# In conditions
>>> day = 'Saturday'
>>> day == 'Saturday' or day == 'Sunday'
True  # It is Saturday!

>>> grade = 105
>>> grade < 0 or grade > 100
True  # Grade is invalid
```

### Practical Example: Error Checking

```python
number = int(input("Enter grade: "))

if number < 0 or number > 100:
    print("Error: Grade must be between 0 and 100")
else:
    # Process the valid grade
    if number >= 90:
        letter = 'A'
    elif number >= 80:
        letter = 'B'
    # ... etc ...
```

## The NOT Operator

`not` reverses a Boolean value.

### Truth Table for NOT

| A | not A |
|---|-------|
| True | **False** |
| False | **True** |

### Examples

```python
>>> not True
False
>>> not False
True

# In conditions
>>> is_raining = False
>>> not is_raining
True  # It's NOT raining

>>> age = 15
>>> not (age >= 18)
True  # NOT an adult
```

### Practical Example

```python
# Keep looping while NOT done
done = False

while not done:
    choice = input("Continue? (yes/no): ")
    if choice == 'no':
        done = True
```

## Combining Multiple Operators

You can combine `and`, `or`, and `not`:

```python
# Check if someone can drive
age = 17
has_license = True
has_insurance = True

if age >= 16 and has_license and has_insurance:
    print("You can drive!")
else:
    print("You cannot drive.")
```

### Order of Operations

1. `not` (highest priority)
2. `and`
3. `or` (lowest priority)

```python
# This expression:
not a or b and c

# Is evaluated as:
(not a) or (b and c)

# Use parentheses to be clear!
not (a or b) and c  # Different meaning!
```

## Complex Example: Weekend Check

```python
day = input("Enter day: ")
is_holiday = input("Is it a holiday? (yes/no): ")

# Weekend is Saturday OR Sunday
is_weekend = day == 'Saturday' or day == 'Sunday'

# Day off is weekend OR holiday
is_day_off = is_weekend or is_holiday == 'yes'

if is_day_off:
    print("No school today!")
else:
    print("School day!")
```

## Short-Circuit Evaluation

Python uses **short-circuit evaluation**: it stops checking as soon as it knows the answer.

### For AND

If the first condition is `False`, Python doesn't check the second (because `False and anything = False`).

```python
>>> count = 0
>>> count > 0 and theSum // count > 10
False  # Doesn't check theSum // count (would cause error!)
```

This prevents a division by zero error!

### For OR

If the first condition is `True`, Python doesn't check the second (because `True or anything = True`).

```python
>>> age = 70
>>> age < 18 or age >= 65
True  # Doesn't check age >= 65 (already knows answer)
```

### Practical Use: Safe Division

```python
count = int(input("Enter count: "))
theSum = int(input("Enter sum: "))

# Safe - won't divide by zero
if count > 0 and theSum // count > 10:
    print("Average is greater than 10")
else:
    print("Count is 0 or average is <= 10")
```

## Simplifying Conditions

### Bad: Redundant Code

```python
# Don't do this!
if grade >= 0:
    if grade <= 100:
        print("Valid")
else:
    print("Invalid")
```

### Good: Compound Condition

```python
# Do this!
if grade >= 0 and grade <= 100:
    print("Valid")
else:
    print("Invalid")
```

### Bad: Multiple Separate Ifs

```python
# Don't do this!
if number > 100:
    print("Error!")
if number < 0:
    print("Error!")
```

### Good: Combined with OR

```python
# Do this!
if number > 100 or number < 0:
    print("Error!")
```

## De Morgan's Laws

These laws help simplify conditions:

1. `not (A and B)` = `not A or not B`
2. `not (A or B)` = `not A and not B`

### Example

```python
# These are equivalent:
not (age >= 18 and age < 65)
# Same as:
age < 18 or age >= 65
```

## Common Patterns

### Pattern 1: Range Check

```python
# Check if x is between 10 and 20 (inclusive)
if x >= 10 and x <= 20:
    print("In range")
```

### Pattern 2: Outside Range

```python
# Check if x is outside 10 to 20
if x < 10 or x > 20:
    print("Out of range")
```

### Pattern 3: Multiple Options

```python
# Check if character is a vowel
if ch == 'a' or ch == 'e' or ch == 'i' or ch == 'o' or ch == 'u':
    print("Vowel")

# Better way using 'in':
if ch in 'aeiou':
    print("Vowel")
```

### Pattern 4: Boolean Flags

```python
# Using Boolean variables
is_adult = age >= 18
has_permission = parental_consent == 'yes'

if is_adult or has_permission:
    print("Access granted")
```

## Complete Example: Login System

```python
correct_username = "admin"
correct_password = "pass123"
max_attempts = 3

attempts = 0
logged_in = False

while attempts < max_attempts and not logged_in:
    username = input("Username: ")
    password = input("Password: ")
    
    if username == correct_username and password == correct_password:
        print("Login successful!")
        logged_in = True
    else:
        attempts += 1
        remaining = max_attempts - attempts
        
        if remaining > 0:
            print(f"Incorrect. {remaining} attempts remaining.")
        else:
            print("Account locked!")
```

## Operator Precedence (Full Table)

| Priority | Operator | Description |
|----------|----------|-------------|
| 1 | `**` | Exponentiation |
| 2 | `-` (unary) | Negation |
| 3 | `*`, `/`, `%` | Multiplication, Division, Modulus |
| 4 | `+`, `-` | Addition, Subtraction |
| 5 | `==`, `!=`, `<`, `>`, `<=`, `>=` | Comparison |
| 6 | `not` | Logical NOT |
| 7 | `and` | Logical AND |
| 8 | `or` | Logical OR |

## Key Takeaways

1. **Use `and` when ALL conditions must be true**
2. **Use `or` when ANY condition must be true**
3. **Use `not` to reverse a condition**
4. **Short-circuit evaluation prevents errors**
5. **Use parentheses for clarity**
6. **Simplify nested ifs with compound conditions**
7. **`not` has higher priority than `and` and `or`**

## Practice

Try these in IDLE or VS Code:

```python
# Predict the output
A = True
B = False

print(A and B)      # ?
print(A or B)       # ?
print(not A)        # ?
print(not A or B)   # ?
print(A and not B)  # ?
```

**Answers:** False, True, False, False, True