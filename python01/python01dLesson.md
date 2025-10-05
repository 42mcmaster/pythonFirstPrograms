# Lesson 1d: Input, Processing, and Output

## Learning Objectives
- Use the input() function to get user input
- Convert between data types using int(), float(), and str()
- Process data with arithmetic operations
- Display formatted output using print()

## The Input-Process-Output Pattern

Most programs follow this pattern:
1. **INPUT**: Get data from the user
2. **PROCESS**: Do something with that data
3. **OUTPUT**: Display results to the user

## Getting User Input

The `input()` function pauses the program and waits for the user to type something:

```python
>>> name = input("Enter your name: ")
Enter your name: Alex
>>> name
'Alex'
```

**Important:** `input()` ALWAYS returns a string!

```python
>>> age = input("Enter your age: ")
Enter your age: 16
>>> age
'16'        # This is a string, not a number!
>>> type(age)
<class 'str'>
```

## Type Conversion

To use input as a number, you must convert it:

### int() - Convert to Integer

```python
>>> age = input("Enter your age: ")
Enter your age: 16
>>> age = int(age)    # Convert string to integer
>>> age
16
>>> type(age)
<class 'int'>
```

**Shortcut:** Combine input() and int():

```python
>>> age = int(input("Enter your age: "))
Enter your age: 16
>>> age
16
```

### float() - Convert to Decimal

```python
>>> price = float(input("Enter price: "))
Enter price: 19.99
>>> price
19.99
>>> type(price)
<class 'float'>
```

### str() - Convert to String

```python
>>> age = 16
>>> message = "I am " + str(age) + " years old"
>>> print(message)
I am 16 years old
```

## Processing Data

Once you have input, you can process it:

### Example 1: Adding Two Numbers

```python
>>> first = int(input("Enter the first number: "))
Enter the first number: 23
>>> second = int(input("Enter the second number: "))
Enter the second number: 44
>>> total = first + second
>>> print("The sum is", total)
The sum is 67
```

### Example 2: Calculating Area

```python
>>> length = float(input("Enter the length: "))
Enter the length: 5.5
>>> width = float(input("Enter the width: "))
Enter the width: 3.2
>>> area = length * width
>>> print("The area is", area)
The area is 17.6
```

## Displaying Output

### Basic print()

```python
>>> print("Hello")
Hello

>>> print(42)
42

>>> print(3.14)
3.14
```

### Printing Multiple Values

Values are separated by spaces automatically:

```python
>>> name = "Alex"
>>> age = 16
>>> print("My name is", name, "and I am", age, "years old")
My name is Alex and I am 16 years old
```

### String Concatenation vs. print()

**Concatenation** (joins strings):
```python
>>> name = "Alex"
>>> age = 16
>>> message = "I am " + str(age)  # Must convert age to string!
>>> print(message)
I am 16
```

**print()** (automatic spacing, no conversion needed):
```python
>>> print("I am", age)  # No conversion needed!
I am 16
```

## Common Input/Output Patterns

### Pattern 1: Simple Calculator

```python
>>> num1 = float(input("First number: "))
First number: 10
>>> num2 = float(input("Second number: "))
Second number: 3
>>> print("Sum:", num1 + num2)
Sum: 13.0
>>> print("Difference:", num1 - num2)
Difference: 7.0
>>> print("Product:", num1 * num2)
Product: 30.0
>>> print("Quotient:", num1 / num2)
Quotient: 3.333333333333333
```

### Pattern 2: Unit Conversion

```python
>>> fahrenheit = float(input("Enter temperature in Fahrenheit: "))
Enter temperature in Fahrenheit: 98.6
>>> celsius = (fahrenheit - 32) * 5 / 9
>>> print(fahrenheit, "F =", celsius, "C")
98.6 F = 37.0 C
```

### Pattern 3: Personalized Greeting

```python
>>> first_name = input("Enter your first name: ")
Enter your first name: Alex
>>> last_name = input("Enter your last name: ")
Enter your last name: Smith
>>> print("Welcome,", first_name, last_name + "!")
Welcome, Alex Smith!
```

## Common Errors and Solutions

### Error 1: Trying to do math with strings

```python
>>> age = input("Enter age: ")  # Don't forget int()!
Enter age: 16
>>> next_year = age + 1
TypeError: can only concatenate str (not "int") to str
```

**Solution:** Convert to int first!
```python
>>> age = int(input("Enter age: "))
Enter age: 16
>>> next_year = age + 1
>>> print("Next year you'll be", next_year)
Next year you'll be 17
```

### Error 2: Concatenating number to string

```python
>>> age = 16
>>> message = "I am " + age + " years old"
TypeError: can only concatenate str (not "int") to str
```

**Solution:** Use print() with commas OR convert to string:
```python
>>> print("I am", age, "years old")  # Option 1
I am 16 years old

>>> message = "I am " + str(age) + " years old"  # Option 2
>>> print(message)
I am 16 years old
```

### Error 3: Converting non-numeric input

```python
>>> age = int(input("Enter age: "))
Enter age: sixteen
ValueError: invalid literal for int() with base 10: 'sixteen'
```

**Solution:** Make sure user enters numbers!

## Input/Output Summary Table

| Function | What It Does | Example |
|----------|--------------|---------|
| `input(prompt)` | Gets text from user | `name = input("Name: ")` |
| `int(value)` | Converts to integer | `age = int("16")` |
| `float(value)` | Converts to decimal | `price = float("19.99")` |
| `str(value)` | Converts to string | `text = str(42)` |
| `print(...)` | Displays output | `print("Hello", name)` |

## Best Practices

1. **Use descriptive prompts:**
   - Good: `input("Enter your age in years: ")`
   - Bad: `input()`

2. **Convert input immediately:**
   ```python
   age = int(input("Age: "))  # Good!
   ```

3. **Use print() with commas for mixed types:**
   ```python
   print("Total:", total)  # Good!
   ```

4. **Add spaces in prompts:**
   ```python
   input("Name: ")    # Note the space after :
   ```