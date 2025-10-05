# Lesson 2d Tasks: Arithmetic Expressions

## Task 1: Calculator Practice

Create a file called `calculator.py` that performs all these operations on two numbers:

```python
num1 = 17
num2 = 5

# Print the results of:
# - Addition
# - Subtraction
# - Multiplication
# - Regular division
# - Integer division
# - Modulus
# - Exponentiation

# Example:
print(f"{num1} + {num2} = {num1 + num2}")
# Continue for all operations...
```

## Task 2: Even or Odd Checker

Create a file called `even_odd.py` that:

1. Asks the user for a number
2. Uses the modulus operator to determine if it's even or odd
3. Prints the result

**Example run:**
```
Enter a number: 47
47 is odd!
```

**Hint:** A number is even if `number % 2 == 0`

## Task 3: Division Explorer

Create a file called `division_practice.py` that shows the difference between `/` and `//`:

```python
# Try these divisions and observe the results
print("Regular division:")
print(f"10 / 3 = {10 / 3}")
print(f"15 / 5 = {15 / 5}")
print(f"7 / 2 = {7 / 2}")

print("\nInteger division:")
print(f"10 // 3 = {10 // 3}")
print(f"15 // 5 = {15 // 5}")
print(f"7 // 2 = {7 // 2}")

# Now try your own examples
# What patterns do you notice?
```

## Task 4: Temperature Converter

Create a file called `temp_convert.py` that:

1. Asks the user for a temperature in Fahrenheit
2. Converts it to Celsius using: `C = (F - 32) × 5/9`
3. Displays both temperatures

**Example run:**
```
Enter temperature in Fahrenheit: 98.6
98.6°F = 37.0°C
```

**Extension:** Also calculate and display Kelvin (K = C + 273.15)

## Task 5: Time Breakdown

Create a file called `time_converter.py` that:

1. Asks for a number of seconds
2. Converts to hours, minutes, and seconds
3. Displays the result

**Hints:**
- Hours = total seconds // 3600
- Remaining = total seconds % 3600
- Minutes = remaining // 60
- Seconds = remaining % 60

**Example run:**
```
Enter total seconds: 7384
7384 seconds = 2 hours, 3 minutes, 4 seconds
```

## Task 6: Circle Calculator

Create a file called `circle_calc.py` that:

1. Asks the user for a circle's radius
2. Calculates and displays:
   - Circumference (2 × π × r)
   - Area (π × r²)

Use `pi = 3.14159`

**Example run:**
```
Enter the radius: 5
Radius: 5
Circumference: 31.4159
Area: 78.53975
```

## Task 7: Order of Operations Quiz

Create a file called `order_quiz.py` with these expressions. **Before running**, write down what you think each will equal. Then run it to check!

```python
# Predict these results BEFORE running:

expr1 = 5 + 3 * 2
expr2 = (5 + 3) * 2
expr3 = 10 - 4 - 2
expr4 = 2 ** 3 ** 2
expr5 = 15 / 3 * 2
expr6 = 10 % 3 + 5
expr7 = 2 + 3 ** 2 * 4
expr8 = (2 + 3) ** (2 * 4)

print(f"5 + 3 * 2 = {expr1}")
# Print all of them...
```

Create a comment above each one with your prediction!

## Task 8: Modulus Applications

Create a file called `modulus_practice.py` that demonstrates three uses of the modulus operator:

1. **Check if divisible:** Check if 100 is divisible by 7
2. **Get last digit:** Get the last digit of 4567 (hint: `% 10`)
3. **Wrap around:** If you have 23 items and want to arrange them in groups of 5, how many are left over?

## Task 9: Money Calculator

Create a file called `money_calc.py` that:

1. Asks for a number of cents (as an integer)
2. Calculates how many dollars and cents that is
3. Displays the result

**Hint:** 
- Dollars = cents // 100
- Remaining cents = cents % 100

**Example run:**
```
Enter total cents: 347
$3.47
```

**Challenge:** Calculate how many quarters, dimes, nickels, and pennies!

## Task 10: Average Calculator

Create a file called `average.py` that:

1. Asks the user for three test scores
2. Calculates the average
3. Rounds to 2 decimal places using `round()`
4. Displays the result

**Example run:**
```
Enter score 1: 85
Enter score 2: 92
Enter score 3: 88
Your average is: 88.33
```

## Task 11: Rectangle Calculator

Create a file called `rectangle.py` that:

1. Asks for length and width of a rectangle
2. Calculates and displays:
   - Perimeter (2 × length + 2 × width)
   - Area (length × width)

**Example run:**
```
Enter length: 5
Enter width: 3
Perimeter: 16
Area: 15
```

## Challenge Task 1: Quadratic Formula

Create a file called `quadratic.py` that solves quadratic equations using the formula:

x = (-b ± √(b² - 4ac)) / 2a

1. Ask user for a, b, and c
2. Calculate both solutions
3. Display the results

**Hint:** Use `** 0.5` for square root, or import math and use `math.sqrt()`

## Challenge Task 2: Distance Calculator

Create a file called `distance.py` that calculates the distance between two points using:

distance = √((x₂ - x₁)² + (y₂ - y₁)²)

Ask for (x1, y1) and (x2, y2) and display the distance.

## Challenge Task 3: Compound Interest

Create a file called `interest.py` that calculates compound interest:

A = P(1 + r/n)^(nt)

Where:
- P = principal amount
- r = annual interest rate (as decimal)
- n = times interest compounds per year
- t = number of years

Ask the user for these values and calculate the final amount.

## Debugging Challenge

Find and fix all the errors in this code:

```python
# Bug Hunt!

# Calculate area of triangle
base = 10
height = 5
area = 1/2 * base * height
print(f"Area: {area}")

# Check if divisible by 3
number = 17
if number / 3 == 0:
    print("Divisible by 3")

# Calculate hours and minutes
total_minutes = 150
hours = total_minutes / 60
minutes = total_minutes / 60
print(f"{hours} hours and {minutes} minutes")

# Convert temperature
fahrenheit = 98.6
celsius = fahrenheit - 32 * 5 / 9
print(f"{celsius}°C")
```

Save the fixed version as `arithmetic_fixed.py`.

## Prediction Practice

Before running this code, predict what will print:

```python
a = 10
b = 3

result1 = a / b
result2 = a // b  
result3 = a % b
result4 = a ** b

print(f"a / b = {result1}")
print(f"a // b = {result2}")
print(f"a % b = {result3}")
print(f"a ** b = {result4}")

print(f"Check: {result2} * {b} + {result3} = {result2 * b + result3}")
```

Write your predictions, then run it!

## Research Questions

Answer these in a file called `arithmetic_research.txt`:

1. What is the difference between `/` and `//`? Give three examples showing when you'd use each.

2. Explain how the modulus operator `%` works. Give three practical uses for it.

3. What does "operator precedence" mean? Why is it important?

4. If you see this expression: `2 ** 3 ** 2`, what is the result and why?

5. When mixing integers and floats in calculations, what type is the result? Why does Python work this way?

## Reflection Questions

In `lesson4_reflection.txt`, answer:

1. Which arithmetic operator was most confusing at first? Do you understand it now?

2. Why do you think Python has both `/` and `//` for division instead of just one?

3. Give a real-world situation where you would need to use the modulus operator.

4. How does understanding operator precedence help you write better code?

## Submission Checklist

Files to submit:
- [ ] `calculator.py`
- [ ] `even_odd.py`
- [ ] `division_practice.py`
- [ ] `temp_convert.py`
- [ ] `time_converter.py`
- [ ] `circle_calc.py`
- [ ] `order_quiz.py`
- [ ] `modulus_practice.py`
- [ ] `money_calc.py`
- [ ] `average.py`
- [ ] `rectangle.py`
- [ ] `arithmetic_fixed.py`
- [ ] `arithmetic_research.txt`
- [ ] `lesson4_reflection.txt`
- [ ] (Optional) Challenge tasks

Each Python file should have:
- [ ] Docstring explaining what it does
- [ ] Comments for complex calculations
- [ ] Clear variable names
- [ ] Proper formatting and output labels

## Going Further (Optional)

1. Research the `math` module in Python. What additional mathematical functions does it provide?

2. Create a BMI (Body Mass Index) calculator that uses the formula: BMI = weight(kg) / height(m)²

3. Build a tip calculator that computes the tip amount and total bill based on a percentage.

4. Create a program that converts between different units (miles to kilometers, pounds to kilograms, etc.).