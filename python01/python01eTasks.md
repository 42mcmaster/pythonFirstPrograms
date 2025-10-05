# Tasks: Writing Python Scripts

## Task 1: Your First Script (15 minutes)

Create a new script file and write this program:

**File name:** `about_me.py`

```python
# About Me Program
# Author: [Your Name]
# Date: [Today's Date]

print("About Me")
print("=" * 20)

name = input("What is your name? ")
age = int(input("What is your age? "))
grade = int(input("What grade are you in? "))

print()
print("Hi", name + "!")
print("You are", age, "years old")
print("You are in grade", grade)
```

**Testing:**
1. Save the file
2. Run it (F5)
3. Test with your information
4. Run it again with different information

**Questions:**
1. What does `"=" * 20` do? ___________________________
2. What happens if you type letters for age? ___________________________
3. Where does the output appear? ___________________________

## Task 2: Calculator Script (20 minutes)

Create a new script for each calculator:

### Calculator 1: Circle Calculator

**File name:** `circle.py`

```python
# Circle Calculator
# Calculates circumference and area of a circle

# Your code here:
# 1. Print a title
# 2. Ask for radius
# 3. Calculate circumference (2 × π × radius)
# 4. Calculate area (π × radius²)
# 5. Display both results
# Use 3.14159 for π
```

Test with radius = 5:
- Expected circumference: ~31.4159
- Expected area: ~78.5398
- Your results: ___________________________

### Calculator 2: Time Converter

**File name:** `time_converter.py`

```python
# Time Converter
# Converts minutes to hours and minutes

# Your code here:
# 1. Ask for total minutes
# 2. Calculate hours (minutes // 60)
# 3. Calculate remaining minutes (minutes % 60)
# 4. Display result as "X hours and Y minutes"
```

Test with 135 minutes:
- Expected: 2 hours and 15 minutes
- Your result: ___________________________

## Task 3: Comments Practice (15 minutes)

Open your `about_me.py` file and add comments:

1. Add a comment above each section explaining what it does
2. Add a comment explaining what `"=" * 20` does
3. Add inline comments (after code) for the input lines

**Example:**
```python
# Display header
print("About Me")
print("=" * 20)  # Creates a line of 20 equal signs

# Get user information
name = input("What is your name? ")  # Store user's name
```

Save your improved file as `about_me_commented.py`

## Task 4: Error Hunting (15 minutes)

Create a new file called `errors.py` and type this code EXACTLY as shown (errors included):

```python
# Error Practice
print("Finding Errors)

name = input("Enter name: ")
  print("Hello", name)

age = input("Enter age: "
age = int(age)
print("You are, age, "years old")
```

1. Try to run it. What happens? ___________________________
2. Fix ONE error, save, and try again
3. Repeat until the program runs successfully
4. List the errors you found:
   - Error 1: ___________________________
   - Error 2: ___________________________
   - Error 3: ___________________________
   - Error 4: ___________________________

## Task 5: Multi-Step Programs (25 minutes)

Create these complete programs:

### Program 1: Grade Calculator

**File name:** `grade_calculator.py`

```python
# Grade Calculator
# Calculates average of three test scores

# Display program title

# Get three test scores from user

# Calculate the average

# Display the average
```

Requirements:
- Use appropriate variable names
- Include comments
- Test with: 85, 90, 78
- Expected average: 84.33...

### Program 2: Shopping Calculator

**File name:** `shopping.py`

```python
# Shopping Calculator
# Calculates total cost with tax

# Your code here:
# 1. Print a title
# 2. Ask for item price
# 3. Ask for quantity
# 4. Ask for tax rate (as a percentage, like 8.5)
# 5. Calculate subtotal (price × quantity)
# 6. Calculate tax amount (subtotal × tax_rate / 100)
# 7. Calculate total (subtotal + tax)
# 8. Display subtotal, tax, and total
```

Test with: $10 item, quantity 3, 7% tax
- Expected subtotal: $30.00
- Expected tax: $2.10
- Expected total: $32.10
- Your results: ___________________________

## Task 6: Program Design (20 minutes)

Design and write a program from scratch:

### Allowance Calculator

**File name:** `allowance.py`

**What it should do:**
- Ask how much allowance per week
- Ask how many weeks to save
- Calculate total saved
- Calculate how many months that is (weeks ÷ 4.33)
- Display both results

**Your planning:**

What inputs do you need?
1. ___________________________
2. ___________________________

What calculations will you do?
1. ___________________________
2. ___________________________

What will you output?
1. ___________________________
2. ___________________________

Now write the program!

Test with $10/week for 20 weeks:
- Expected total: $200
- Expected months: ~4.62
- Your results: ___________________________

## Task 7: Script Organization (15 minutes)

Create a well-organized script with clear sections:

**File name:** `pizza_party.py`

**Purpose:** Calculate how many pizzas needed for a party

```python
# Program: Pizza Party Calculator
# Author: 
# Date: 
# Description: 

# Display header


# Input section
# - Number of people
# - Slices per person
# - Slices per pizza


# Processing section
# - Calculate total slices needed
# - Calculate pizzas needed (round up!)
# - Hint: use // for whole pizzas, then add 1 if there's a remainder


# Output section
# - Display number of pizzas to order

```

Test with: 15 people, 3 slices each, 8 slices per pizza
- Expected: 6 pizzas (15 × 3 = 45 slices, 45 ÷ 8 = 5.625, round up to 6)

## Task 8: Personal Project (Optional)

Create a program that solves a real problem in your life!

Ideas:
- Movie collection tracker (how many movies, how many hours total?)
- Study time calculator (time per subject, break time, total time needed)
- Money tracker (income, expenses, savings)
- Exercise tracker (calories burned based on activity and time)
- Reading progress (pages per day, days to finish book)

Requirements:
- At least 3 inputs
- At least 2 calculations
- Clear output
- Well-commented
- Organized into sections

## Reflection Questions

1. What's the main advantage of scripts over using the shell?
   ___________________________________________________________

2. Why are comments important in your code?
   ___________________________________________________________

3. Describe your process for fixing errors in your scripts:
   ___________________________________________________________

4. What was the most challenging part of writing scripts?
   ___________________________________________________________

## Challenge Problems (Extra Credit)

### Challenge 1: Advanced Calculator

Create a program that:
- Asks for two numbers
- Displays the sum, difference, product, quotient, and remainder
- Make it look nice with clear labels

### Challenge 2: Unit Converter Suite

Create one program that converts:
- Inches to centimeters (× 2.54)
- Fahrenheit to Celsius
- Miles to kilometers (× 1.60934)

Ask the user which conversion they want to do!

### Challenge 3: Receipt Generator

Create a program that:
- Asks for store name
- Asks for 3 item names and prices
- Calculates subtotal
- Adds 8% tax
- Displays a formatted receipt with all items and total

## Debugging Checklist

Before asking for help, check:
- [ ] Did you save your file?
- [ ] Does your filename end in .py?
- [ ] Are all your quotes matched? ("..." or '...')
- [ ] Are all your parentheses matched? (...)
- [ ] Did you convert input to int() or float() when needed?
- [ ] Are your variable names spelled consistently?
- [ ] Are you using print() to display output?
- [ ] Did you test with simple values first?