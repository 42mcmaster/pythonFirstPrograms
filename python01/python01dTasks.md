# Tasks: Input, Processing, and Output

## Task 1: Input Practice (15 minutes)

Open IDLE and create these simple input programs. Test each one!

**Program 1: Name Greeter**
```python
>>> name = input("What is your name? ")
>>> print("Hello,", name + "!")
```

Test it with your name. What appears? ___________________________

**Program 2: Favorite Things**
```python
>>> color = input("What's your favorite color? ")
>>> food = input("What's your favorite food? ")
>>> print("You like", color, "and", food)
```

Test it. Write the output: ___________________________

**Program 3: Age Next Year**
```python
>>> age = int(input("How old are you? "))
>>> next_year = age + 1
>>> print("Next year you will be", next_year)
```

Test it. Does it work correctly? ___________________________

## Task 2: Type Conversion Challenge (15 minutes)

For each scenario, write the code and test it:

**Challenge 1:** Ask for someone's height in inches, convert to feet (divide by 12), and display the result.

```python
>>> 
>>> 
>>> 
```

**Challenge 2:** Ask for two decimal numbers, multiply them, and show the product.

```python
>>> 
>>> 
>>> 
```

**Challenge 3:** Ask for a number, then print that number multiplied by itself (squared).

```python
>>> 
>>> 
>>> 
```

## Task 3: Error Detective (10 minutes)

Each of these programs has an error. Type them in IDLE, find the error, and fix it:

**Program 1:**
```python
>>> age = input("Enter your age: ")
>>> next_age = age + 1
>>> print("Next year:", next_age)
```

Error message: ___________________________
What's wrong? ___________________________
How to fix: ___________________________

**Program 2:**
```python
>>> num = 42
>>> message = "The answer is " + num
>>> print(message)
```

Error message: ___________________________
What's wrong? ___________________________
How to fix: ___________________________

**Program 3:**
```python
>>> price = float(input("Enter price: "))
>>> quantity = int(input("Enter quantity: "))
>>> total = "Total: $" + price * quantity
>>> print(total)
```

Error message: ___________________________
What's wrong? ___________________________
How to fix: ___________________________

## Task 4: Calculator Programs (20 minutes)

Create these calculator programs. Test each one with different numbers!

**Program 1: Rectangle Area Calculator**
```python
# Ask for length and width
# Calculate area (length × width)
# Display the result

>>> 
>>> 
>>> 
>>> 
```

Test with length=5, width=3. Expected area: ___________
Your result: ___________

**Program 2: Temperature Converter**
```python
# Ask for temperature in Celsius
# Convert to Fahrenheit: F = C × 9/5 + 32
# Display the result

>>> 
>>> 
>>> 
```

Test with 0°C. Expected: 32°F
Your result: ___________

Test with 100°C. Expected: 212°F
Your result: ___________

**Program 3: Circle Circumference**
```python
# Ask for radius
# Calculate circumference: C = 2 × π × radius
# (Use 3.14159 for π)
# Display the result

>>> 
>>> 
>>> 
>>> 
```

Test with radius=5. Expected: ~31.4159
Your result: ___________

## Task 5: Multi-Step Programs (15 minutes)

**Program 1: Shopping Cart**
Ask for:
- Item name
- Price per item
- Quantity

Calculate and display:
- Item name
- Total cost (price × quantity)

```python
>>> 
>>> 
>>> 
>>> 
>>> 
```

Example output:
```
Item: Apples
Total cost: $ 4.50
```

**Program 2: Trip Calculator**
Ask for:
- Distance in miles
- Miles per gallon (MPG)
- Price per gallon of gas

Calculate and display:
- Gallons needed (distance ÷ MPG)
- Total cost (gallons × price per gallon)

```python
>>> 
>>> 
>>> 
>>> 
>>> 
>>> 
```

Test with: 300 miles, 25 MPG, $3.50/gallon
Expected: 12 gallons, $42.00
Your result: ___________

## Task 6: String vs. Number Operations (10 minutes)

Predict what each will output, then test:

**Example 1:**
```python
>>> x = "5"
>>> y = "3"
>>> print(x + y)
```
Your prediction: ___________
Actual result: ___________

**Example 2:**
```python
>>> x = 5
>>> y = 3
>>> print(x + y)
```
Your prediction: ___________
Actual result: ___________

**Example 3:**
```python
>>> x = "5"
>>> y = 3
>>> print(x * y)
```
Your prediction: ___________
Actual result: ___________

**Example 4:**
```python
>>> x = 5
>>> y = 3
>>> print(x * y)
```
Your prediction: ___________
Actual result: ___________

**Question:** What's the difference between adding strings and adding numbers?
___________________________________________________________

## Extension Challenge (Optional)

### BMI Calculator

Create a program that:
1. Asks for weight in pounds
2. Asks for height in inches
3. Calculates BMI using: BMI = (weight × 703) ÷ (height²)
4. Displays the result

```python
>>> 
>>> 
>>> 
>>> 
```

Test with: 150 pounds, 65 inches
Expected BMI: ~24.96
Your result: ___________

### Grade Calculator

Create a program that:
1. Asks for three test scores
2. Calculates the average
3. Displays the average

Can you make it display a message like "Your average is 85.67"?

## Reflection Questions

1. Why do we need to convert input from strings to numbers?
   ___________________________________________________________

2. When would you use `int()` vs `float()`?
   ___________________________________________________________

3. What's easier: using print() with commas or string concatenation? Why?
   ___________________________________________________________