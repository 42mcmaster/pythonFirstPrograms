# Lesson 3f Tasks: Logical Operators Practice

## Setup
Complete these tasks in IDLE or VS Code. Focus on using compound conditions!

---

## Task 1: Valid Range Checker 
**Difficulty: Easy**

Write a program that checks if a number is between 1 and 100 (inclusive).

**Sample Run 1:**
```
Enter a number: 50
50 is in the valid range.
```

**Sample Run 2:**
```
Enter a number: 150
150 is NOT in the valid range.
```

**Hints:**
- Use `and` to check both conditions
- `number >= 1 and number <= 100`

---

## Task 2: Weekend Detector 
**Difficulty: Easy**

Create a program that checks if a day is a weekend day.

**Sample Run:**
```
Enter a day: Saturday
It's the weekend!
```

**Hints:**
- Use `or` to check for Saturday OR Sunday
- Use `.lower()` or `.title()` for case-insensitive comparison

---

## Task 3: Password Validator 
**Difficulty: Medium**

Write a program that checks if a password is valid. A valid password must:
- Be at least 8 characters long
- Contain at least one number

**Sample Run:**
```
Enter password: Secret99
Password is valid!
```

**Hints:**
- Check length: `len(password) >= 8`
- Check for digit: `any(char.isdigit() for char in password)`
- Or use a loop to check each character
- Combine with `and`

---

## Task 4: Triangle Validity Checker 
**Difficulty: Medium**

Create a program that checks if three sides can form a valid triangle.
Remember: The sum of any two sides must be greater than the third.

**Sample Run:**
```
Enter side 1: 3
Enter side 2: 4
Enter side 3: 5
These sides form a valid triangle!
```

**Hints:**
- Check three conditions with `and`:
  - `a + b > c`
  - `a + c > b`
  - `b + c > a`
- All must be true

---

## Task 5: Leap Year Checker 
**Difficulty: Medium**

Write a program that determines if a year is a leap year using logical operators.

Rules:
- Divisible by 4 AND not by 100, OR
- Divisible by 400

**Sample Run:**
```
Enter a year: 2024
2024 is a leap year.
```

**Hints:**
- Combine conditions: `(year % 4 == 0 and year % 100 != 0) or (year % 400 == 0)`

---

## Task 6: Grade Calculator with Validation 
**Difficulty: Medium**

Create a program that converts a numeric grade to a letter, but first validates that the grade is between 0 and 100.

If invalid, print an error. If valid, show the letter grade.

**Sample Run:**
```
Enter grade: 105
Error: Grade must be between 0 and 100.
```

**Hints:**
- First check: `grade < 0 or grade > 100`
- If invalid, print error
- Else, proceed with grade conversion

---

## Task 7: Age Category Classifier 
**Difficulty: Hard**

Write a program that classifies age into categories:
- Child: 0-12
- Teen: 13-19
- Adult: 20-64
- Senior: 65+
- Invalid: negative numbers

Use compound conditions where appropriate.

**Sample Run:**
```
Enter age: 45
You are an adult.
```

**Hints:**
- Use `and` for range checks
- `age >= 13 and age <= 19` for teen

---

## Task 8: Safe Division Calculator 
**Difficulty: Hard**

Create a calculator that:
- Asks for two numbers and an operation (+, -, *, /)
- Performs the operation
- For division, check that divisor is not zero BEFORE dividing
- Show appropriate error messages

**Sample Run:**
```
Enter first number: 10
Enter second number: 0
Enter operation (+, -, *, /): /
Error: Cannot divide by zero!
```

**Hints:**
- Use `and` for safe division check
- `operation == '/' and num2 != 0`

---

## Task 9: Parking Permit Validator 
**Difficulty: Hard**

Write a program for a parking garage that checks if someone can park.

They can park if:
- They have a monthly pass, OR
- (They have a daily pass AND arrived before 5 PM)

Ask for:
- Do you have a monthly pass? (yes/no)
- Do you have a daily pass? (yes/no)
- What time is it? (0-23, military time)

**Sample Run:**
```
Monthly pass? (yes/no): no
Daily pass? (yes/no): yes
Current hour (0-23): 14
You may park!
```

**Hints:**
- `has_monthly or (has_daily and hour < 17)`
- Convert yes/no to boolean

---

## Task 10: Character Type Identifier 
**Difficulty: Hard**

Create a program that identifies what type of character was entered:
- Lowercase letter (a-z)
- Uppercase letter (A-Z)
- Digit (0-9)
- Special character (anything else)

**Sample Run:**
```
Enter a character: @
@ is a special character.
```

**Hints:**
- Use: `char >= 'a' and char <= 'z'`
- Or use: `char.islower()`, `char.isupper()`, `char.isdigit()`

---

## Submission Checklist

- [ ] Used compound conditions (`and`, `or`, `not`)
- [ ] Avoided nested ifs where compound conditions work
- [ ] Properly used parentheses for clarity
- [ ] Tested edge cases (boundary values)
- [ ] Code is readable and well-commented

## Truth Table Practice

Before coding, practice these:

1. `True and False` = ?
2. `True or False` = ?
3. `not True` = ?
4. `True and True or False` = ?
5. `not (True or False)` = ?

**Answers:** False, True, False, True, False

## Testing Strategy

For compound conditions, create a test table:

Example for: `age >= 18 and age < 65`

| Age | age >= 18 | age < 65 | Result |
|-----|-----------|----------|--------|
| 15 | False | True | False |
| 18 | True | True | **True** |
| 50 | True | True | **True** |
| 65 | True | False | False |
| 70 | True | False | False |

Test values that make conditions True, False, and combinations!