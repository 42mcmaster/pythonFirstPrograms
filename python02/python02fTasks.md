# Lesson 2f Tasks: Functions and Modules

## Task 1: Function Exploration

Create a file called `function_practice.py` that explores these built-in functions:

```python
# Test these functions and observe the results:
print(abs(-15))
print(max(3, 7, 2, 9, 1))
print(min(3, 7, 2, 9, 1))
print(round(3.7))
print(round(3.14159, 2))
print(pow(2, 3))
print(len("Python Programming"))

# Now try combining them:
numbers = [3, -7, 2, -9, 1]
print(f"Maximum absolute value: {max(abs(-7), abs(-9))}")
```

## Task 2: Math Module Basics

Create a file called `math_basics.py` that:

1. Imports the math module
2. Prints these values:
   - Square root of 25
   - Pi (π)
   - Euler's number (e)
   - 2 to the power of 10 using `math.pow()`
   - Floor of 7.9 (round down)
   - Ceiling of 7.1 (round up)

```python
import math

# Your code here
```

## Task 3: Right Triangle Calculator

Create a file called `triangle_calc.py` that:

1. Asks for the two legs of a right triangle (a and b)
2. Calculates the hypotenuse using Pythagorean theorem: c = √(a² + b²)
3. Uses `math.sqrt()` for the square root
4. Displays the result

**Example run:**
```
Enter side a: 3
Enter side b: 4
The hypotenuse is 5.0
```

## Task 4: Circle Calculator with Math Module

Create a file called `circle_with_math.py` that:

1. Asks for a radius
2. Uses `math.pi` for calculations
3. Calculates and displays:
   - Circumference (2πr)
   - Area (πr²)

**Example run:**
```
Enter the radius: 5
Circumference: 31.42
Area: 78.54
```

## Task 5: Trigonometry Explorer

Create a file called `trig_practice.py` that demonstrates trig functions:

```python
import math

# Convert degrees to radians (needed for trig functions)
angle_degrees = 45
angle_radians = math.radians(angle_degrees)

print(f"Angle: {angle_degrees}°")
print(f"Sine: {math.sin(angle_radians):.4f}")
print(f"Cosine: {math.cos(angle_radians):.4f}")
print(f"Tangent: {math.tan(angle_radians):.4f}")

# Try with 30°, 60°, and 90° too!
```

## Task 6: Import Methods Comparison

Create a file called `import_comparison.py` that shows different import methods:

```python
# Method 1: Import module
import math
result1 = math.sqrt(16)
print(f"Method 1: {result1}")

# Method 2: Import specific functions
from math import sqrt, pi
result2 = sqrt(16)
area = pi * 5**2
print(f"Method 2: {result2}")
print(f"Circle area: {area}")

# Try both methods and see which you prefer!
```

## Task 7: Distance Calculator

Create a file called `distance_calc.py` that:

1. Asks for two points: (x1, y1) and (x2, y2)
2. Calculates distance using: d = √((x₂-x₁)² + (y₂-y₁)²)
3. Uses `math.sqrt()` for the calculation
4. Displays the distance

**Example run:**
```
Enter x1: 0
Enter y1: 0
Enter x2: 3
Enter y2: 4
Distance: 5.0
```

## Task 8: Logarithm Explorer

Create a file called `log_practice.py` that:

```python
import math

number = float(input("Enter a number: "))

# Calculate different logarithms
natural_log = math.log(number)
log_base_10 = math.log10(number)
log_base_2 = math.log2(number)

print(f"Natural log (ln): {natural_log}")
print(f"Log base 10: {log_base_10}")
print(f"Log base 2: {log_base_2}")
```

Test with: 10, 100, 8

## Task 9: Rounding Functions Comparison

Create a file called `rounding_comparison.py` that:

```python
import math

number = float(input("Enter a decimal number: "))

print(f"Original: {number}")
print(f"round(): {round(number)}")
print(f"math.floor(): {math.floor(number)}")
print(f"math.ceil(): {math.ceil(number)}")
print(f"math.trunc(): {math.trunc(number)}")
print(f"int(): {int(number)}")
```

Test with: 3.7, 3.2, -2.7

## Task 10: Help Function Practice

Create a file called `help_explorer.py` that uses `help()`:

```python
# Uncomment one at a time to see the help info:
# help(round)
# help(math.sqrt)
# help(len)
# help(max)

# Write comments explaining what you learned about each function
```

## Task 11: Scientific Calculator

Create a file called `calculator_advanced.py` that:

1. Shows a menu of operations:
   - Square root
   - Power
   - Sine
   - Cosine
   - Logarithm
2. Asks user to choose an operation
3. Gets necessary inputs
4. Performs calculation using math module
5. Displays result

**Example run:**
```
Calculator Menu:
1. Square root
2. Power
3. Sine
Choose operation (1-3): 1
Enter number: 16
Result: 4.0
```

## Task 12: Compound Interest Calculator

Create a file called `compound_interest.py` that:

1. Uses the formula: A = P(1 + r/n)^(nt)
   - P = principal (initial amount)
   - r = annual interest rate (as decimal)
   - n = times interest compounds per year
   - t = number of years
2. Uses `math.pow()` for the exponent
3. Calculates and displays final amount

**Example run:**
```
Enter principal: $1000
Enter annual rate (e.g., 0.05 for 5%): 0.05
Enter compounds per year: 12
Enter number of years: 10
Final amount: $1647.01
```

## Challenge Task 1: Quadratic Formula with Math

Create a file called `quadratic_complete.py` that:

1. Solves ax² + bx + c = 0
2. Uses `math.sqrt()` for the square root
3. Checks if solutions are real (b² - 4ac ≥ 0)
4. Displays both solutions or error message

## Challenge Task 2: Temperature Statistics

Create a file called `temp_stats.py` that:

1. Asks for 5 temperature readings
2. Calculates:
   - Maximum (use `max()`)
   - Minimum (use `min()`)
   - Average
   - Standard deviation (use math.sqrt and formulas)
3. Displays all statistics

## Challenge Task 3: Angle Converter

Create a file called `angle_converter.py` that:

1. Asks for an angle in degrees
2. Converts to radians using `math.radians()`
3. Calculates sin, cos, tan
4. Converts back to degrees using `math.degrees()`
5. Displays all values

## Debugging Challenge

Fix all the errors in this code:

```python
# Bug Hunt!

# Calculate square root
import Math
number = input("Enter number: ")
result = math.sqrt(number)
print(result)

# Calculate circle area
from math import Pi
radius = 5
area = Pi * radius ** 2
print(area)

# Use floor function
math.floor(3.7)
print("Floored!")

# Calculate sine
angle = 45
result = math.sin(angle)
print(result)
```

Save fixed version as `modules_fixed.py`.

## Research Questions

Answer in `modules_research.txt`:

1. What's the difference between `math.pow(2, 3)` and `2 ** 3`? When would you use each?

2. Why do you need to convert degrees to radians for trig functions? Use `math.radians()` in your answer.

3. What's the difference between `math.floor()`, `math.ceil()`, and `int()`?

4. Explore the `random` module. How would you:
   - Generate a random integer between 1 and 10?
   - Generate a random float between 0 and 1?
   - Choose a random item from a list?

5. What does it mean when a function "returns" a value? Give three examples of functions that return values.

## Exploration Task

Create a file called `module_explorer.py` that:

```python
import math

# Print all available functions in math module
print("Math module contents:")
print(dir(math))

# Try out 3 functions you haven't used yet
# Document what they do
```

## Reflection Questions

Answer in `lesson6_reflection.txt`:

1. Why are modules useful? Give three reasons.

2. What's the advantage of `import math` vs `from math import *`?

3. How does the `help()` function help you learn about new functions?

4. Give an example of when you'd need to use the `math` module instead of basic arithmetic operators.

## Submission Checklist

Files to submit:
- [ ] `function_practice.py`
- [ ] `math_basics.py`
- [ ] `triangle_calc.py`
- [ ] `circle_with_math.py`
- [ ] `trig_practice.py`
- [ ] `import_comparison.py`
- [ ] `distance_calc.py`
- [ ] `log_practice.py`
- [ ] `rounding_comparison.py`
- [ ] `calculator_advanced.py`
- [ ] `compound_interest.py`
- [ ] `modules_fixed.py`
- [ ] `module_explorer.py`
- [ ] `modules_research.txt`
- [ ] `lesson6_reflection.txt`
- [ ] (Optional) Challenge tasks

Each file should:
- [ ] Import modules at the top
- [ ] Have a descriptive docstring
- [ ] Use functions correctly with proper arguments
- [ ] Handle return values appropriately
- [ ] Include comments explaining complex parts

## Going Further (Optional)

1. Explore the `random` module - create a dice rolling simulator

2. Research the `statistics` module - create a program that calculates mean, median, and mode

3. Investigate the `datetime` module - create a program that calculates someone's exact age in days

4. Create your own simple module with helper functions and import it into another program