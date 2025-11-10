# Lesson 3k Tasks: Error Handling and Exceptions

## Setup
Create programs that handle errors gracefully - no crashes allowed!

---

## Task 1: Safe Number Input
**Difficulty: Easy**

Write a program that asks for 3 numbers and adds them. Handle ValueError if user enters non-numbers. Keep asking until valid input is received.

**Expected Run:**
```
Enter number 1: abc
Invalid! Try again.
Enter number 1: 10
Enter number 2: twenty
Invalid! Try again.
Enter number 2: 20
Enter number 3: 30
Sum: 60
```

**Hints:**
- Use a while loop for each input
- try/except ValueError
- break when successful

---

## Task 2: Safe Division Calculator
**Difficulty: Easy**

Create a calculator that divides two numbers. Handle both ValueError (invalid input) and ZeroDivisionError (divide by zero).

**Expected Runs:**
```
Numerator: 100
Denominator: 0
Error: Cannot divide by zero!
```

```
Numerator: abc
Error: Please enter valid numbers!
```

```
Numerator: 100
Denominator: 4
Result: 25.0
```

**Hints:**
- Need two except blocks
- Check ValueError first, then ZeroDivisionError

---

## Task 3: Grade Validator
**Difficulty: Medium**

Create a function `get_valid_grade()` that:
- Asks for a grade (0-100)
- Handles ValueError for non-numbers
- Raises ValueError if grade is outside 0-100 range
- Keeps asking until valid

**Expected Run:**
```
Enter grade: abc
Invalid number!
Enter grade: 150
Grade must be between 0 and 100!
Enter grade: 85
Grade accepted: 85
```

**Hints:**
- Use try/except inside a while loop
- Use `raise ValueError("message")` for range check
- Return valid grade

---

## Task 4: Safe File Reader
**Difficulty: Medium**

Write a program that:
- Asks for a filename
- Tries to open and read the file
- Handles FileNotFoundError
- Allows user to try different filename
- Displays file contents when successful

**Expected Run:**
```
Enter filename: missing.txt
File not found! Try again.
Enter filename: data.txt
File contents:
---------------
Hello, World!
This is a test.
---------------
```

**Hints:**
- Use try/except for FileNotFoundError
- Loop until successful or user quits
- Option to quit if file not found

---

## Task 5: Robust Menu Program
**Difficulty: Medium**

Create a menu program with complete error handling:
```
1. Calculate area of circle
2. Calculate square root
3. Quit
```

Handle:
- ValueError for menu choice
- ValueError for invalid numbers
- Negative numbers for square root

**Expected Run:**
```
1. Calculate area of circle
2. Calculate square root  
3. Quit
Choice: abc
Invalid choice!

Choice: 1
Radius: 5
Area: 78.5

Choice: 2
Number: -4
Cannot calculate square root of negative number!

Choice: 3
Goodbye!
```

**Hints:**
- Import math for sqrt and pi
- try/except in multiple places
- Check for negative before sqrt

---

## Testing Checklist

- [ ] Test with invalid input (letters instead of numbers)
- [ ] Test with out-of-range values
- [ ] Test with extreme values (very large, negative)
- [ ] Verify program never crashes
- [ ] Ensure error messages are clear and helpful
