# Lesson 3.6 Tasks: Logical Operators Practice

## Setup
Complete these tasks in IDLE or VS Code. Focus on using compound conditions!

---

## Task 1: Valid Range Checker ⭐
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

## Task 2: Weekend Detector ⭐
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

## Task 3: Password Validator ⭐⭐
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

## Task 4: Triangle Validity Checker ⭐⭐
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

## Task 5: Leap Year Checker ⭐⭐
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

## Task 6: Grade Calculator with Validation ⭐⭐
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

## Task 7: Age Category Classifier ⭐⭐⭐
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

## Task 8: Safe Division Calculator ⭐⭐⭐
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

## Task 9: Parking Permit Validator ⭐⭐⭐
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

## Task 10: Character Type Identifier ⭐⭐⭐
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

## Challenge Task 1: Login System 🌟
**Difficulty: Challenge**

Create a secure login system with these features:
- Maximum 3 attempts
- Correct username AND password required
- After 3 failed attempts, lock the account
- Show remaining attempts after each failure

**Sample Run:**
```
Attempt 1 of 3
Username: admin
Password: wrong
Login failed. 2 attempts remaining.

Attempt 2 of 3
Username: admin
Password: password123
Login successful!
Welcome, admin!
```

**Hints:**
- Use a while loop with compound condition
- `attempts < 3 and not logged_in`
- Check: `username == correct_user and password == correct_pass`

---

## Challenge Task 2: Date Validator 🌟
**Difficulty: Challenge**

Write a program that validates a date (month/day/year):
- Month must be 1-12
- Day must be valid for the month
  - Jan, Mar, May, Jul, Aug, Oct, Dec: 1-31
  - Apr, Jun, Sep, Nov: 1-30
  - Feb: 1-29 (if leap year), 1-28 (if not)
- Year must be positive

**Sample Run:**
```
Enter month (1-12): 2
Enter day: 30
Enter year: 2024
Invalid date: February doesn't have 30 days.
```

**Hints:**
- Lots of compound conditions!
- Check month first, then valid days for that month
- Use leap year logic for February

---

## Bonus Challenge: Complex Discount Calculator 🌟🌟
**Difficulty: Very Hard**

Create a discount calculator with these rules:
- 10% discount if total >= $100
- Additional 5% if customer is a member
- Additional 10% if it's a holiday
- Show original price, all discounts applied, and final price

**Sample Run:**
```
Enter total: $150
Member? (yes/no): yes
Holiday? (yes/no): yes
Original price: $150.00
Bulk discount (10%): $15.00
Member discount (5%): $7.50
Holiday discount (10%): $15.00
Final price: $112.50
```

**Hints:**
- Apply discounts sequentially to running total
- Each discount may or may not apply
- Use compound conditions to determine which discounts apply

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