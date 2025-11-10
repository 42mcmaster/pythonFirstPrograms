# Lesson 3m: Unit Testing with unittest

## Learning Objectives
- Understand what unit testing is and why it's important
- Write test cases using the unittest module
- Use common assert methods
- Run and interpret test results
- Test functions and methods effectively

## What is Unit Testing?

**Unit Testing** = Testing individual "units" (functions) of code to verify they work correctly

**Why test?**
- Find bugs early
- Verify code works as expected
- Make sure changes don't break existing code
- Document how code should behave

## Manual Testing vs Automated Testing

**Manual Testing (what you've been doing):**
```python
def add(a, b):
    return a + b

# Manual test
print(add(2, 3))  # Should be 5
print(add(-1, 1))  # Should be 0
```

**Problems:**
- Tedious to run every test each time
- Easy to forget tests
- Hard to test many cases

**Automated Testing:**
```python
import unittest

class TestAdd(unittest.TestCase):
    def test_add_positive(self):
        self.assertEqual(add(2, 3), 5)
    
    def test_add_negative(self):
        self.assertEqual(add(-1, 1), 0)

# Run tests automatically!
```

## The unittest Module

Python's built-in testing framework.

### Basic Structure

```python
import unittest

# 1. Import the function you want to test
def add(a, b):
    return a + b

# 2. Create a test class (inherits from unittest.TestCase)
class TestMathFunctions(unittest.TestCase):
    
    # 3. Write test methods (must start with "test_")
    def test_add_positive_numbers(self):
        result = add(2, 3)
        self.assertEqual(result, 5)
    
    def test_add_negative_numbers(self):
        result = add(-5, -3)
        self.assertEqual(result, -8)

# 4. Run the tests
if __name__ == "__main__":
    unittest.main()
```

## Common Assert Methods

These are the most important methods for testing:

### assertEqual(a, b)
Tests if a == b

```python
def test_addition(self):
    self.assertEqual(2 + 2, 4)
    self.assertEqual("hello", "hello")
```

### assertNotEqual(a, b)
Tests if a != b

```python
def test_not_equal(self):
    self.assertNotEqual(5, 10)
```

### assertTrue(x)
Tests if x is True

```python
def test_is_even(self):
    self.assertTrue(is_even(4))
    self.assertTrue(10 > 5)
```

### assertFalse(x)
Tests if x is False

```python
def test_is_odd(self):
    self.assertFalse(is_even(3))
```

### assertIn(item, container)
Tests if item is in container

```python
def test_membership(self):
    self.assertIn(3, [1, 2, 3, 4])
    self.assertIn("a", "banana")
```

### assertIsInstance(obj, class)
Tests if obj is an instance of class

```python
def test_type(self):
    self.assertIsInstance(5, int)
    self.assertIsInstance("hello", str)
    self.assertIsInstance([1, 2], list)
```

### assertIs(a, b)
Tests if a is b (identity, not equality)

```python
def test_identity(self):
    x = [1, 2]
    y = x
    self.assertIs(x, y)  # Same object
```

## Example 1: Testing a Grade Function

```python
import unittest

def get_letter_grade(score):
    """Convert numeric score to letter grade."""
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

class TestGradeFunction(unittest.TestCase):
    
    def test_grade_a(self):
        self.assertEqual(get_letter_grade(95), "A")
        self.assertEqual(get_letter_grade(90), "A")
    
    def test_grade_b(self):
        self.assertEqual(get_letter_grade(85), "B")
        self.assertEqual(get_letter_grade(80), "B")
    
    def test_grade_f(self):
        self.assertEqual(get_letter_grade(59), "F")
        self.assertEqual(get_letter_grade(0), "F")
    
    def test_boundary_values(self):
        """Test values at grade boundaries."""
        self.assertEqual(get_letter_grade(89), "B")  # Just below A
        self.assertEqual(get_letter_grade(90), "A")  # At boundary

if __name__ == "__main__":
    unittest.main()
```

**Output:**
```
....
----------------------------------------------------------------------
Ran 4 tests in 0.001s

OK
```

## Example 2: Testing Multiple Functions

```python
import unittest

def is_even(n):
    """Check if number is even."""
    return n % 2 == 0

def is_positive(n):
    """Check if number is positive."""
    return n > 0

def absolute_value(n):
    """Return absolute value of number."""
    if n < 0:
        return -n
    return n

class TestNumberFunctions(unittest.TestCase):
    
    def test_is_even_true(self):
        self.assertTrue(is_even(4))
        self.assertTrue(is_even(0))
        self.assertTrue(is_even(-2))
    
    def test_is_even_false(self):
        self.assertFalse(is_even(3))
        self.assertFalse(is_even(-1))
    
    def test_is_positive(self):
        self.assertTrue(is_positive(1))
        self.assertFalse(is_positive(0))
        self.assertFalse(is_positive(-5))
    
    def test_absolute_value(self):
        self.assertEqual(absolute_value(5), 5)
        self.assertEqual(absolute_value(-5), 5)
        self.assertEqual(absolute_value(0), 0)

if __name__ == "__main__":
    unittest.main()
```

## Running Tests

### Run from command line:
```bash
python test_file.py
```

### Run specific test:
```bash
python test_file.py TestNumberFunctions.test_is_even_true
```

### Verbose output:
```bash
python test_file.py -v
```

**Verbose Output:**
```
test_absolute_value (__main__.TestNumberFunctions) ... ok
test_is_even_false (__main__.TestNumberFunctions) ... ok
test_is_even_true (__main__.TestNumberFunctions) ... ok
test_is_positive (__main__.TestNumberFunctions) ... ok

----------------------------------------------------------------------
Ran 4 tests in 0.001s

OK
```

## Understanding Test Results

### All Tests Pass
```
....
----------------------------------------------------------------------
Ran 4 tests in 0.001s

OK
```
- Each dot (`.`) = one passed test
- `OK` = all tests passed

### A Test Fails
```
..F.
======================================================================
FAIL: test_grade_b (__main__.TestGradeFunction)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "test.py", line 20, in test_grade_b
    self.assertEqual(get_letter_grade(85), "A")
AssertionError: 'B' != 'A'

----------------------------------------------------------------------
Ran 4 tests in 0.002s

FAILED (failures=1)
```
- `F` = failed test
- Shows which assertion failed and why

## Example 3: Testing with Lists

```python
import unittest

def find_max(numbers):
    """Find maximum value in list."""
    if not numbers:
        return None
    return max(numbers)

def remove_duplicates(items):
    """Remove duplicates from list."""
    return list(set(items))

class TestListFunctions(unittest.TestCase):
    
    def test_find_max_normal(self):
        self.assertEqual(find_max([1, 5, 3, 9, 2]), 9)
    
    def test_find_max_negative(self):
        self.assertEqual(find_max([-5, -1, -10]), -1)
    
    def test_find_max_empty(self):
        self.assertIsNone(find_max([]))
    
    def test_remove_duplicates(self):
        result = remove_duplicates([1, 2, 2, 3, 3, 3])
        self.assertEqual(len(result), 3)
        self.assertIn(1, result)
        self.assertIn(2, result)
        self.assertIn(3, result)

if __name__ == "__main__":
    unittest.main()
```

## Testing Edge Cases

**Edge cases** = unusual or extreme inputs

Always test:
- Empty inputs (empty list, empty string, zero)
- Boundary values (min/max allowed)
- Negative numbers
- Very large numbers
- Invalid inputs

```python
import unittest

def divide(a, b):
    """Divide a by b."""
    if b == 0:
        raise ValueError("Cannot divide by zero")
    return a / b

class TestDivide(unittest.TestCase):
    
    def test_normal_division(self):
        self.assertEqual(divide(10, 2), 5)
    
    def test_divide_by_one(self):
        self.assertEqual(divide(7, 1), 7)
    
    def test_divide_zero(self):
        self.assertEqual(divide(0, 5), 0)
    
    def test_divide_by_zero_raises_error(self):
        with self.assertRaises(ValueError):
            divide(10, 0)
    
    def test_negative_numbers(self):
        self.assertEqual(divide(-10, 2), -5)

if __name__ == "__main__":
    unittest.main()
```

## Organizing Test Files

**Good practice:** Keep tests in separate files

**Project structure:**
```
my_project/
    math_functions.py      # Your code
    test_math_functions.py # Your tests
```

**test_math_functions.py:**
```python
import unittest
from math_functions import add, subtract, multiply

class TestMathFunctions(unittest.TestCase):
    def test_add(self):
        self.assertEqual(add(2, 3), 5)
    
    # More tests...

if __name__ == "__main__":
    unittest.main()
```

## Complete Example: Calculator with Tests

**calculator.py:**
```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero")
    return a / b
```

**test_calculator.py:**
```python
import unittest
from calculator import add, subtract, multiply, divide

class TestCalculator(unittest.TestCase):
    
    def test_add(self):
        self.assertEqual(add(5, 3), 8)
        self.assertEqual(add(-1, 1), 0)
        self.assertEqual(add(0, 0), 0)
    
    def test_subtract(self):
        self.assertEqual(subtract(10, 5), 5)
        self.assertEqual(subtract(5, 10), -5)
    
    def test_multiply(self):
        self.assertEqual(multiply(4, 5), 20)
        self.assertEqual(multiply(-2, 3), -6)
        self.assertEqual(multiply(0, 100), 0)
    
    def test_divide(self):
        self.assertEqual(divide(10, 2), 5)
        self.assertEqual(divide(9, 3), 3)
    
    def test_divide_by_zero(self):
        with self.assertRaises(ValueError):
            divide(10, 0)

if __name__ == "__main__":
    unittest.main()
```

**Run tests:**
```bash
python test_calculator.py -v
```

## Why Unit Testing Matters

1. **Catches bugs early** - before users find them
2. **Documents behavior** - tests show how functions should work
3. **Enables refactoring** - change code with confidence
4. **Saves time** - automated testing is faster than manual
5. **Professional practice** - industry standard

## Key Takeaways

1. **unittest** is Python's built-in testing framework
2. **Test class** inherits from `unittest.TestCase`
3. **Test methods** start with `test_`
4. **assertEqual(a, b)** - most common assertion
5. **assertTrue/False** - test boolean conditions
6. **assertIn** - test membership
7. **assertIsInstance** - test types
8. **assertIs** - test identity
9. **Test edge cases** - empty, boundary, invalid inputs
10. **Run with** `python test_file.py`

## Quick Reference

```python
import unittest

class TestMyFunction(unittest.TestCase):
    
    def test_something(self):
        # Common assertions:
        self.assertEqual(a, b)          # a == b
        self.assertNotEqual(a, b)       # a != b
        self.assertTrue(x)              # x is True
        self.assertFalse(x)             # x is False
        self.assertIn(item, container)  # item in container
        self.assertIsInstance(obj, cls) # isinstance(obj, cls)
        self.assertIs(a, b)             # a is b

if __name__ == "__main__":
    unittest.main()
```

## Practice Exercise

Create and test this function:

```python
import unittest

def is_palindrome(text):
    """Check if text is a palindrome (reads same forwards and backwards)."""
    cleaned = text.lower().replace(" ", "")
    return cleaned == cleaned[::-1]

class TestPalindrome(unittest.TestCase):
    
    def test_simple_palindrome(self):
        self.assertTrue(is_palindrome("racecar"))
    
    def test_not_palindrome(self):
        self.assertFalse(is_palindrome("hello"))
    
    def test_palindrome_with_spaces(self):
        self.assertTrue(is_palindrome("race car"))
    
    def test_mixed_case(self):
        self.assertTrue(is_palindrome("RaceCar"))

if __name__ == "__main__":
    unittest.main()
```
