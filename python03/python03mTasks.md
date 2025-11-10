# Lesson 3m Tasks: Unit Testing with unittest

## Setup
Create two files for each task: one with functions, one with tests.

---

## Task 1: Test Basic Math Functions
**Difficulty: Easy**

Create `math_ops.py` with these functions:
```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b
```

Then create `test_math_ops.py` that tests:
- Adding positive numbers
- Adding negative numbers
- Subtracting to get negative result
- Multiplying by zero
- Multiplying negative numbers

**Expected Output:**
```
.....
----------------------------------------------------------------------
Ran 5 tests in 0.001s

OK
```

**Hints:**
- Import unittest and the functions
- Create TestMathOps class
- Use assertEqual for all tests
- Test at least 5 different cases

---

## Task 2: Test String Functions
**Difficulty: Easy**

Create `string_utils.py`:
```python
def is_uppercase(text):
    """Check if all letters are uppercase."""
    return text.isupper()

def count_vowels(text):
    """Count vowels in text."""
    vowels = "aeiouAEIOU"
    return sum(1 for char in text if char in vowels)
```

Create tests for:
- is_uppercase with "HELLO" (should be True)
- is_uppercase with "Hello" (should be False)
- count_vowels with "hello" (should be 2)
- count_vowels with "aeiou" (should be 5)

**Expected Output:**
```
....
----------------------------------------------------------------------
Ran 4 tests in 0.001s

OK
```

**Hints:**
- Use assertTrue and assertFalse
- Use assertEqual for count_vowels
- Test edge cases like empty strings

---

## Task 3: Test List Functions
**Difficulty: Medium**

Create `list_utils.py`:
```python
def find_average(numbers):
    """Calculate average of numbers in list."""
    if not numbers:
        return 0
    return sum(numbers) / len(numbers)

def find_min_max(numbers):
    """Return tuple of (min, max) from list."""
    if not numbers:
        return (None, None)
    return (min(numbers), max(numbers))
```

Write tests for:
- Average of [1, 2, 3, 4, 5]
- Average of empty list
- Min/max of [10, 5, 8, 12, 3]
- Min/max of empty list
- Average with negative numbers

**Expected Output:**
```
.....
----------------------------------------------------------------------
Ran 5 tests in 0.001s

OK
```

**Hints:**
- Use assertEqual for average
- Test the tuple returned by find_min_max
- Use assertIsNone for None values
- Test edge cases

---

## Task 4: Test Grade Calculator
**Difficulty: Medium**

Create `grade_calculator.py`:
```python
def calculate_letter_grade(score):
    """Convert numeric score (0-100) to letter grade."""
    if score < 0 or score > 100:
        raise ValueError("Score must be between 0 and 100")
    if score >= 90:
        return "A"
    elif score >= 80:
        return "B"
    elif score >= 70:
        return "C"
    elif score >= 60:
        return "D"
    else:
        return "F"
```

Write tests for:
- Each letter grade (A, B, C, D, F)
- Boundary values (89, 90, 79, 80, etc.)
- Invalid scores (raises ValueError)
- Score of 100 and 0

**Expected Output:**
```
........
----------------------------------------------------------------------
Ran 8 tests in 0.001s

OK
```

**Hints:**
- Use assertEqual for letter grades
- Test boundaries carefully
- Use `with self.assertRaises(ValueError):` for invalid scores
- Make sure to test both 59 and 60, 89 and 90, etc.

---

## Task 5: Test Temperature Converter
**Difficulty: Medium**

Create `temperature.py`:
```python
def celsius_to_fahrenheit(celsius):
    """Convert Celsius to Fahrenheit."""
    return (celsius * 9/5) + 32

def fahrenheit_to_celsius(fahrenheit):
    """Convert Fahrenheit to Celsius."""
    return (fahrenheit - 32) * 5/9

def is_freezing_celsius(temp):
    """Check if temperature is at or below freezing (0°C)."""
    return temp <= 0
```

Write tests for:
- 0°C = 32°F
- 100°C = 212°F
- 32°F = 0°C
- is_freezing with -5°C (True)
- is_freezing with 10°C (False)
- Round results to 1 decimal place

**Expected Output:**
```
......
----------------------------------------------------------------------
Ran 6 tests in 0.001s

OK
```

**Hints:**
- Use assertAlmostEqual for floating point comparisons
- `self.assertAlmostEqual(result, expected, places=1)`
- Test conversion both ways
- Use assertTrue and assertFalse for is_freezing

---

## Testing Checklist

- [ ] All test methods start with `test_`
- [ ] Test class inherits from unittest.TestCase
- [ ] Use appropriate assert methods
- [ ] Test edge cases (empty, zero, negative)
- [ ] Test boundary values
- [ ] All tests pass (shows OK)
- [ ] Tests are in separate file from functions
