# Lesson 2c Tasks: Numbers and Data Types

## Task 1: Type Detective

Create a file called `type_checker.py` that checks the type of different values:

```python
# Check the type of these values and predict what will print
# Then run the program to see if you were right!

value1 = 42
value2 = 42.0
value3 = "42"
value4 = 0
value5 = 0.0

print("Value:", value1, "Type:", type(value1))
print("Value:", value2, "Type:", type(value2))
# Add print statements for the remaining values
```

**Before running:** Write down what type you think each value is. Were you correct?

## Task 2: Integer Practice

Create a file called `integer_math.py` that:

1. Creates variables for:
   - Number of students in your class
   - Number of days in a year
   - Your birth year
   - Current year

2. Calculates and prints:
   - Your age (current year - birth year)
   - Days lived (age × 365) - approximate!
   - A fun fact using your numbers

**Example output:**
```
I am 15 years old.
I've lived approximately 5475 days.
There are 25 students in my class.
```

## Task 3: Float Practice

Create a file called `measurement_converter.py` that:

1. Asks the user for their height in inches
2. Converts to centimeters (1 inch = 2.54 cm)
3. Displays both measurements

```python
# Starter code
inches = float(input("Enter your height in inches: "))
# Your code here to convert and print
```

**Extension:** Also convert to meters (100 cm = 1 m)

## Task 4: Scientific Notation

Create a file called `big_numbers.py` that defines these values using scientific notation:

1. Speed of light: 299,792,458 m/s
2. Earth's population: approximately 7,900,000,000
3. Size of an atom: 0.0000000001 meters
4. Distance to the sun: 149,600,000,000 meters

Then print each with a descriptive label.

**Example:**
```python
speed_of_light = 2.99792458e8
print(f"Speed of light: {speed_of_light} m/s")
# Continue for others...
```

## Task 5: ASCII Explorer

Create a file called `ascii_fun.py` that:

1. Prints the ASCII codes for:
   - Your first initial
   - The first letter of your last name
   - The digits 0-9
   - The space character

2. Then prints the characters for these ASCII codes:
   - 65, 66, 67
   - 97, 98, 99
   - 48, 49, 50

**Example output:**
```
ASCII code for 'J': 74
ASCII code for 'S': 83
Character for ASCII 65: A
Character for ASCII 66: B
```

## Task 6: Caesar Cipher

Create a file called `simple_cipher.py` that:

1. Asks the user for a single letter
2. Gets its ASCII code
3. Adds 3 to the code (Caesar cipher with shift of 3)
4. Converts back to a character
5. Shows the encrypted letter

**Example run:**
```
Enter a letter: A
Original letter: A (ASCII 65)
Encrypted letter: D (ASCII 68)
```

**Challenge:** Make it work for the entire alphabet by wrapping around (Z → C)

## Task 7: Character Analysis

Create a file called `char_analyzer.py` that:

1. Asks the user for a single character
2. Gets its ASCII code
3. Determines and prints whether it is:
   - An uppercase letter (65-90)
   - A lowercase letter (97-122)
   - A digit (48-57)
   - Something else

**Example output:**
```
Enter a character: m
ASCII code: 109
This is a lowercase letter!
```

## Task 8: Type Conversion Exploration

Create a file called `type_conversions.py` that demonstrates these conversions:

```python
# Starting values
int_val = 42
float_val = 3.14
str_val = "100"

# Try these conversions and print results:
# 1. int to float
# 2. float to int (what happens to the decimal?)
# 3. string to int
# 4. int to string
# 5. string to float

# Example:
print(f"int {int_val} to float: {float(int_val)}")
# Add more...
```

**Question to answer:** What happens when you convert 3.14 to an int?

## Task 9: Number Patterns

Create a file called `number_patterns.py` that prints these ASCII patterns:

```
Pattern 1: Print ASCII codes 65-75
Pattern 2: Print the characters for those codes
Pattern 3: Print both together like: 65 = A
```

Use a for loop or just print each one individually for now.

## Task 10: Guess the Output

Create a file called `guess_output.py` with these lines. **Before running**, write down what you think each will print. Then run it and check!

```python
print(type(5))
print(type(5.0))
print(type("5"))
print(type(5) == type(5.0))
print(5 == 5.0)

print(ord('A'))
print(chr(65))
print(chr(ord('Z')))
print(ord(chr(100)))

print(1_000_000)
print(1e6)
```

## Challenge Task: Alphabet Shifter

Create `alphabet_shifter.py` that:

1. Asks for a letter (A-Z only, uppercase)
2. Asks for a shift amount (e.g., 3)
3. Shifts the letter by that amount
4. Wraps around if needed (e.g., Y + 3 = B)
5. Prints the result

**Hints:**
- Get the ASCII code with `ord()`
- Add the shift amount
- If the result > 90, subtract 26 to wrap around
- Convert back with `chr()`

**Example:**
```
Enter a letter: W
Enter shift amount: 5
W shifted by 5 is: B
```

## Debugging Challenge

Find and fix the errors in this code:

```python
# Bug Hunt!
number = "42"
result = number + 10
print(result)

decimal = 3.14.15
print(type(decimal))

code = ord("Hello")
print(code)

char = chr(3.5)
print(char)

big = 1,000,000
print(big)
```

Save the corrected version as `types_fixed.py`.

## Research Task

Answer these questions in a file called `types_research.txt`:

1. What is the difference between `float` and `int` division in Python? Try `10 / 3` vs `10 // 3` and explain what you observe.

2. What happens if you try `ord("AB")`? Why do you think this error occurs?

3. What's the ASCII code for your space bar? For the Enter/Return key?

4. Python can handle huge integers. Try calculating `2 ** 100` (2 to the power of 100). How many digits does the result have?

5. What is the difference between `5` and `5.0` to Python? When would it matter?

## Reflection Questions

In a file called `lesson3_reflection.txt`, answer:

1. Why do you think computers use numbers to represent characters instead of just storing the letters directly?

2. When would you choose to use an `int` vs a `float`? Give three examples of each.

3. Explain in your own words what ASCII is and why it's important.

4. What surprised you most about how Python handles numbers and characters?

## Submission Checklist

Files to submit:
- [ ] `type_checker.py`
- [ ] `integer_math.py`
- [ ] `measurement_converter.py`
- [ ] `big_numbers.py`
- [ ] `ascii_fun.py`
- [ ] `simple_cipher.py`
- [ ] `char_analyzer.py`
- [ ] `type_conversions.py`
- [ ] `number_patterns.py`
- [ ] `guess_output.py`
- [ ] `types_fixed.py`
- [ ] `types_research.txt`
- [ ] `lesson3_reflection.txt`
- [ ] (Optional) `alphabet_shifter.py`

Make sure each file has:
- [ ] Docstring at the top
- [ ] Comments explaining your code
- [ ] Good variable names
- [ ] Proper output formatting

## Going Further (Optional)

1. Research Unicode and how it differs from ASCII. Why was Unicode created?

2. Create a program that converts lowercase letters to uppercase without using `.upper()` - just using ASCII math!

3. Build a program that determines if a character is a vowel or consonant by checking its ASCII code.

4. Explore what happens with very large numbers in Python. Can you find Python's limits for integers? For floats?