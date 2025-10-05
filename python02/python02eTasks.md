# Lesson 5 Tasks: Type Conversions and Input

## Task 1: Conversion Practice

Create a file called `conversions.py` that demonstrates all these conversions:

```python
# Start with these values
str_int = "42"
str_float = "3.14"
num_int = 100
num_float = 2.718

# Convert and print:
# 1. str_int to integer
# 2. str_float to float
# 3. num_int to string
# 4. num_float to string
# 5. num_int to float
# 6. num_float to integer (observe what happens!)

# Example:
print(f"'{str_int}' as int: {int(str_int)}, type: {type(int(str_int))}")
# Continue for others...
```

## Task 2: Age Calculator

Create a file called `age_calc.py` that:

1. Asks for the user's current age
2. Asks for a number of years in the future
3. Calculates how old they'll be
4. Displays the result

**Example run:**
```
Enter your current age: 15
How many years in the future? 10
In 10 years, you will be 25 years old.
```

## Task 3: Rectangle Area Calculator

Create a file called `rect_area.py` that:

1. Asks the user for the length (can be decimal)
2. Asks the user for the width (can be decimal)
3. Calculates the area
4. Displays the result with 2 decimal places

**Example run:**
```
Enter length: 5.5
Enter width: 3.2
Area: 17.60 square units
```

**Hint:** Use `{area:.2f}` to format to 2 decimal places

## Task 4: Temperature Converter v2

Create a file called `temp_converter_v2.py` that:

1. Asks the user for a temperature in Fahrenheit
2. Converts to Celsius: C = (F - 32) × 5/9
3. Displays both temperatures nicely formatted

**Example run:**
```
Enter temperature in °F: 98.6
98.6°F = 37.0°C
```

## Task 5: Price Calculator

Create a file called `price_calc.py` that:

1. Asks for an item price
2. Asks for quantity
3. Asks for tax rate (as decimal, e.g., 0.07)
4. Calculates subtotal, tax, and total
5. Displays results formatted as money ($XX.XX)

**Example run:**
```
Enter price per item: $19.99
Enter quantity: 3
Enter tax rate (e.g., 0.07 for 7%): 0.07

Subtotal: $59.97
Tax:      $4.20
Total:    $64.17
```

## Task 6: Circle Measurements

Create a file called `circle_measurements.py` that:

1. Asks for the radius
2. Calculates:
   - Diameter (2 × radius)
   - Circumference (2 × π × radius)
   - Area (π × radius²)
3. Displays all measurements

Use `pi = 3.14159`

## Task 7: Average Grade Calculator

Create a file called `grade_average.py` that:

1. Asks for 4 test scores
2. Calculates the average
3. Displays the average rounded to 1 decimal place

**Example run:**
```
Enter test 1 score: 85
Enter test 2 score: 92
Enter test 3 score: 88
Enter test 4 score: 91

Your average is: 89.0
```

## Task 8: Conversion Error Handler

Create a file called `input_validator.py` that:

```python
# Try to convert user input
user_input = input("Enter a number: ")

try:
    number = int(user_input)
    print(f"✓ Successfully converted to integer: {number}")
except ValueError:
    print(f"✗ Could not convert '{user_input}' to integer")
    try:
        number = float(user_input)
        print(f"✓ But it works as a float: {number}")
    except ValueError:
        print(f"✗ Not a valid number at all!")
```

Test it with: "42", "3.14", "hello"

## Task 9: Time Converter with Input

Create a file called `time_input.py` that:

1. Asks for a number of seconds
2. Converts to hours, minutes, seconds
3. Displays formatted result

**Example run:**
```
Enter total seconds: 3665
3665 seconds = 1 hour(s), 1 minute(s), 5 second(s)
```

## Task 10: Money Exchange

Create a file called `currency_exchange.py` that:

1. Asks for amount in USD
2. Asks for exchange rate (e.g., 0.85 for USD to EUR)
3. Calculates and displays converted amount

**Example run:**
```
Enter amount in USD: $100
Enter exchange rate: 0.85
$100.00 USD = €85.00 EUR
```

## Task 11: BMI Calculator

Create a file called `bmi_calculator.py` that:

1. Asks for weight in kilograms
2. Asks for height in meters
3. Calculates BMI: weight / (height²)
4. Displays result with 1 decimal place

**Example run:**
```
Enter weight (kg): 70
Enter height (m): 1.75
Your BMI is: 22.9
```

## Task 12: Truncation vs Rounding

Create a file called `truncate_vs_round.py` that shows the difference:

```python
# Get a decimal number
number = float(input("Enter a decimal number: "))

# Show different conversions
print(f"Original: {number}")
print(f"int() (truncate): {int(number)}")
print(f"round(): {round(number)}")
print(f"round to 1 decimal: {round(number, 1)}")
print(f"round to 2 decimals: {round(number, 2)}")
```

Test with: 3.7, 3.2, 3.5, -2.7

## Challenge Task 1: Tip Calculator

Create a file called `tip_calculator.py` that:

1. Asks for the bill amount
2. Asks for tip percentage (15, 18, 20, etc.)
3. Asks how many people are splitting the bill
4. Calculates and displays:
   - Tip amount
   - Total bill (including tip)
   - Amount per person

**Example run:**
```
Enter bill amount: $45.50
Enter tip percentage: 18
Number of people: 3

Tip amount: $8.19
Total bill: $53.69
Per person: $17.90
```

## Challenge Task 2: Quadratic Solver

Create a file called `quadratic_solver.py` that:

1. Asks for a, b, c in ax² + bx + c = 0
2. Calculates both solutions using quadratic formula
3. Handles the square root (use `** 0.5`)
4. Displays results

**Note:** Don't worry about imaginary numbers for now - assume real solutions!

## Challenge Task 3: Fuel Efficiency

Create a file called `fuel_calc.py` that:

1. Asks for miles driven
2. Asks for gallons used
3. Calculates MPG (miles per gallon)
4. Calculates cost if gas is $3.50/gallon
5. Displays all results

## Debugging Challenge

Find and fix all the errors:

```python
# Bug Hunt!

# Get user's age
age = input("Enter age: ")
print("Next year you'll be " + age + 1)

# Calculate total
price = input("Enter price: ")
quantity = input("Enter quantity: ")
total = price * quantity
print("Total: $" + total)

# Convert temperature
fahr = input("Enter °F: ")
celsius = (fahr - 32) * 5 / 9
print(celsius + "°C")

# Round number
num = "3.7"
print(round(num))
```

Save fixed version as `conversions_fixed.py`.

## Type Detective

For each line, predict what will print **before** running:

```python
# Prediction quiz
print(int("42"))
print(int("42.5"))  # What happens here?
print(float("42"))
print(float(42))
print(int(3.9))
print(int(3.1))
print(str(42) + str(10))
print("5" * 3)
print(int("5") * 3)
print(type(input("Enter: ")))
```

Create a file with your predictions as comments, then run it!

## Research Questions

Answer in `conversions_research.txt`:

1. What error do you get if you try `int("3.14")`? Why?

2. What's the difference between `int(3.7)` and `round(3.7)`?

3. Why does `input()` always return a string instead of automatically detecting if it's a number?

4. What happens if you try to convert an empty string: `int("")`?

5. Can you convert a boolean to an int? Try `int(True)` and `int(False)`. What do you get?

## Reflection Questions

Answer in `lesson5_reflection.txt`:

1. Why is it important to convert user input to the correct type?

2. Give an example of when you'd use `int()` vs `float()` for user input.

3. What's the most common mistake you made with type conversions? How did you fix it?

4. Explain in your own words what "strongly typed" means.

## Submission Checklist

Files to submit:
- [ ] `conversions.py`
- [ ] `age_calc.py`
- [ ] `rect_area.py`
- [ ] `temp_converter_v2.py`
- [ ] `price_calc.py`
- [ ] `circle_measurements.py`
- [ ] `grade_average.py`
- [ ] `input_validator.py`
- [ ] `time_input.py`
- [ ] `currency_exchange.py`
- [ ] `bmi_calculator.py`
- [ ] `truncate_vs_round.py`
- [ ] `conversions_fixed.py`
- [ ] `conversions_research.txt`
- [ ] `lesson5_reflection.txt`
- [ ] (Optional) Challenge tasks

Each file should:
- [ ] Have a descriptive docstring
- [ ] Use appropriate variable names
- [ ] Convert input to correct types
- [ ] Format output nicely
- [ ] Handle decimal places appropriately

## Going Further (Optional)

1. Add input validation using try/except to handle invalid input gracefully

2. Create a program that converts between different units (feet to meters, pounds to kg, etc.)

3. Build a calorie calculator that takes height, weight, age, and gender to estimate daily calorie needs

4. Make a grade calculator that converts percentage scores to letter grades (A, B, C, etc.)