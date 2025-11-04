# Lesson 3i: Introduction to Functions

## Learning Objectives
- Understand what functions are and why they're useful
- Write simple function definitions
- Call functions with and without parameters
- Return values from functions
- Use functions to organize code
- Combine functions with loops and selection

## What Are Functions?

A **function** is a named block of code that performs a specific task.

Think of a function like a recipe:
- It has a **name** (e.g., "Make Pancakes")
- It might need **ingredients** (parameters)
- It performs **steps** (the code inside)
- It might produce a **result** (return value)

### Why Use Functions?

1. **Avoid repetition** - Write code once, use it many times
2. **Organization** - Break large programs into smaller pieces
3. **Easier testing** - Test each function separately
4. **Easier to read** - Good function names explain what code does
5. **Easier to fix** - Change code in one place, not everywhere

### Real-World Analogy

Imagine you're writing instructions:

**Without functions:**
```
Walk to fridge
Open fridge
Take out butter
Close fridge
Walk to counter
Open butter
Spread on bread
Close butter
Walk to fridge
Open fridge
Put back butter
Close fridge
```

**With functions:**
```
getButter()
spreadOnBread()
putAwayButter()
```

Much clearer!

## Basic Function Syntax

### Defining a Function

```python
def function_name():
    # Code goes here
    print("This is inside the function")
```

- **`def`** - keyword that starts a function definition
- **`function_name`** - name you choose (use descriptive names!)
- **`()`** - parentheses (required, even if empty)
- **`:`** - colon marks the start of the function body
- **Indentation** - function body must be indented

### Calling a Function

```python
def greet():
    print("Hello!")
    print("Welcome to Python functions!")

# Call the function
greet()
```

**Output:**
```
Hello!
Welcome to Python functions!
```

The function doesn't run until you **call** it by using its name with parentheses.

## Example 1: Simple Function

```python
def print_banner():
    print("=" * 40)
    print("   WELCOME TO MY PROGRAM")
    print("=" * 40)

# Use the function
print_banner()
print("put something else here")
print_banner()

```

**Output:**
```
========================================
   WELCOME TO MY PROGRAM
========================================
put something else here
========================================
   WELCOME TO MY PROGRAM
========================================
```

We wrote the banner code once, but used it twice!

## Functions with Parameters

**Parameters** let you pass information into a function.

### Syntax

```python
def function_name(parameter):
    # Use parameter in the code
    print(parameter)
```

### Example: Greeting with Name

```python
def greet(name):
    print(f"Hello, {name}!")
    print("Nice to meet you!")

# Call with different names
greet("Alice")
greet("Bob")
greet("Charlie")
```
**Important note**: The parameter `(name)` is not a variable itself — it’s a placeholder that acts like a variable inside the function. When you call the function (e.g., `greet("Alice")`), Python creates a real variable named `name` inside the function and assigns it the value `"Alice"`.


**Output:**
```
Hello, Alice!
Nice to meet you!
Hello, Bob!
Nice to meet you!
Hello, Charlie!
Nice to meet you!
```

### Parameters vs Arguments

- **Parameter** - Variable in the function definition (`width`, `height`)
- **Argument** - Actual value you pass when calling (`5`, `3`)

```python
def add(a, b):        # a and b are parameters
    print(a + b)

add(5, 3)             # 5 and 3 are arguments
```

### Example of Multiple Parameters

```python
def describe_computer(brand, cpu, ram, storage):
    print(f"{brand} computer with a {cpu} CPU, {ram}GB RAM, and {storage}GB storage.")
```

Call the function: 

```python
describe_computer("Dell Dimension", "Intel Pentium II", 0.0625, 4)
```
### **Dial-Up Era** 💾 💾 💾 Now RAM is about 266 Times Bigger (16 GB) in 2020s vs 2000 (64 MB)

**Output:**
```
Dell Dimension computer with a Intel Pentium II CPU, 0.0625GB RAM, and 4GB storage.

```



## Return Values



Functions can send back a result using **`return`**.

### Syntax

```python
def function_name():
    # Do some work
    return result
```

### Example: Calculator Function

```python
def add(a, b):
    result = a + b
    return result  # RETURN sends value `result` back to main program

# Use the returned value
total = add(10, 5)
print(f"The sum is {total}")

# Or use it directly
print(f"8 + 7 = {add(8, 7)}")
```

**Output:**
```
The sum is 15
8 + 7 = 15
```

## 📺 Let's watch this explanation on `Return` vs `Print`: https://www.youtube.com/watch?v=LWdsF79H1Pg


### Functions Without Return

If a function doesn't have `return`, it returns `None`.

When you call a function with parentheses, **it always runs**.
But what happens after it runs depends on whether it has a return statement.

```python
def greet(name):
    print(f"Hello, {name}!")
    # No return statement

result = greet("Alice")  # greet("Alice") will run because a function always runs
print(f"Result: {result}")  # However, because no return statement, the value Alice isn't stored anywhere
```

**Output:**
```
Hello, Alice!
Result: None
```

**Corrected Version:**

```python
def greet(name):
    return f"Hello, {name}!"   # Return the greeting string

result = greet("Alice")
print(result)
```
**Output:**

```
Hello, Alice!
```

### Why not just `return name`?

If you wrote:

```python
def greet(name):
    return name
```

Then `result` would only store `"Alice"`, not the full greeting message.
That’s valid Python, but it’s not as meaningful — you’re just handing back the *input*, not the *result* of your function’s work.


### Think of it like this

* `print()` = **shows** the greeting on the screen
* `return` = **hands back** the greeting text to your program

To *fix it*, you add a `return`, but you return the **value** your function is supposed to *produce*, not just the variable name itself.


## Example 2: Area Calculator

```python
def calculate_area(length, width):
    """Calculate the area of a rectangle."""
    area = length * width
    return area

def calculate_perimeter(length, width):
    """Calculate the perimeter of a rectangle."""
    perimeter = 2 * (length + width)
    return perimeter

# Use the functions
l = 8
w = 5

area = calculate_area(l, w)
perimeter = calculate_perimeter(l, w)

print(f"Rectangle: {l} x {w}")
print(f"Area: {area}")
print(f"Perimeter: {perimeter}")
```

**Output:**
```
Rectangle: 8 x 5
Area: 40
Perimeter: 26
```

## Functions with Loops

Functions can contain any code, including loops!

```python
def print_pattern(symbol, count):  # reminder (symbol, count) are Parameters 
    """Print a symbol multiple times."""
    for i in range(count):
        print(symbol, end="")
    print()  # New line

# Use it
print_pattern("*", 10)   # these are the Arguments 
print_pattern("-", 20)
print_pattern("#", 15)
```

**Output:**
```
**********
--------------------
###############
```

## Example 3: Count Vowels

```python
def count_vowels(text):              # Define function
    """Count vowels in a string."""  # Description
    vowels = "aeiouAEIOU"            # Vowel list
    count = 0                        # Start counter
    
    for char in text:                # Loop through each letter
        if char in vowels:           # If it's a vowel
            count += 1               # Add 1
    
    return count                     # Send back total

# Test it
sentence = "Hello World"             # Example text
num_vowels = count_vowels(sentence)  # Call the function
print(f"'{sentence}' has {num_vowels} vowels")  # Show result

# Try another
word = input("Enter a word: ")       # Get user input
print(f"Your word has {count_vowels(word)} vowels")  # Show count


```

**Sample Output:**
```
'Hello World' has 3 vowels
Enter a word: Python
Your word has 1 vowels
```

## Functions with Selection

Combine functions with if/elif/else:

```python
def check_grade(points):               
    """Return letter grade for a numeric score."""
    if points >= 90:
        return "A"
    elif points >= 80:
        return "B"
    elif points >= 70:
        return "C"
    elif points >= 60:
        return "D"
    else:
        return "F"

# Use it
score = int(input("Enter your score: "))
grade = check_grade(score)     # pass the score into the function
print(f"Your grade is: {grade}")

```

## Example 4: Validating Input

Functions are great for input validation!

```python
def get_positive_number(prompt):
    """Get a positive number from the user."""
    while True:
        num = int(input(prompt))
        if num > 0:
            return num
        else:
            print("Error: Must be positive!")

# Use it
age = get_positive_number("Enter your age: ")
print(f"You are {age} years old.")

quantity = get_positive_number("How many items? ")
print(f"You ordered {quantity} items.")
```

**Sample Run:**
```
Enter your age: -5
Error: Must be positive!
Enter your age: 0
Error: Must be positive!
Enter your age: 25
You are 25 years old.
```

## Example 5: Temperature Converter

```python
def celsius_to_fahrenheit(celsius):
    """Convert Celsius to Fahrenheit."""
    fahrenheit = (celsius * 9/5) + 32
    return fahrenheit

def fahrenheit_to_celsius(fahrenheit):
    """Convert Fahrenheit to Celsius."""
    celsius = (fahrenheit - 32) * 5/9
    return celsius

# Menu-driven program
while True:
    print("\nTemperature Converter")
    print("1. Celsius to Fahrenheit")
    print("2. Fahrenheit to Celsius")
    print("3. Quit")
    
    choice = input("Choose an option: ")
    
    if choice == "1":
        temp = float(input("Enter temperature in Celsius: "))
        result = celsius_to_fahrenheit(temp)
        print(f"{temp}°C = {result:.1f}°F")
    elif choice == "2":
        temp = float(input("Enter temperature in Fahrenheit: "))
        result = fahrenheit_to_celsius(temp)
        print(f"{temp}°F = {result:.1f}°C")
    elif choice == "3":
        print("Goodbye!")
        break
    else:
        print("Invalid choice!")
```

## Complete Example: Guessing Game with Functions

```python
import random

def get_difficulty():
    """Let user choose difficulty level."""
    print("Choose difficulty:")
    print("1. Easy (1-50)")
    print("2. Medium (1-100)")
    print("3. Hard (1-500)")
    
    while True:
        choice = input("Enter choice: ")
        if choice in ["1", "2", "3"]:
            return int(choice)
        print("Invalid! Try again.")

def get_max_number(difficulty):
    """Return max number based on difficulty."""
    if difficulty == 1:
        return 50
    elif difficulty == 2:
        return 100
    else:
        return 500

def get_max_guesses(difficulty):
    """Return max guesses based on difficulty."""
    if difficulty == 1:
        return 10
    elif difficulty == 2:
        return 7
    else:
        return 10

def play_game():
    """Play one round of the guessing game."""
    difficulty = get_difficulty()
    max_num = get_max_number(difficulty)
    max_guesses = get_max_guesses(difficulty)
    secret = random.randint(1, max_num)
    
    print(f"\nI'm thinking of a number between 1 and {max_num}.")
    
    for guess_num in range(1, max_guesses + 1):
        guess = int(input(f"Guess #{guess_num}: "))
        
        if guess == secret:
            print(f"Correct! You won in {guess_num} guesses!")
            return True
        elif guess < secret:
            print("Too low!")
        else:
            print("Too high!")
    
    print(f"Out of guesses! The number was {secret}.")
    return False

def play_again():
    """Ask if user wants to play again."""
    answer = input("Play again? (yes/no): ")
    return answer.lower() == "yes"

# Main program
print("=== Number Guessing Game ===")
wins = 0
games = 0

while True:
    games += 1
    if play_game():
        wins += 1
    
    if not play_again():
        break

print(f"\nFinal Score: {wins} wins out of {games} games")
print("Thanks for playing!")
```

Notice how breaking the program into functions makes it:
- Easier to understand
- Easier to modify
- Easier to test each part

## Function Design Tips

1. **One job per function** - Each function should do one thing well
2. **Descriptive names** - Use verbs: `calculate_area()`, `get_input()`, `display_result()`
3. **Keep them short** - If a function is too long, break it into smaller functions
4. **Use docstrings** - Add a description right after `def`
   ```python
   def calculate_area(length, width):
       """Calculate and return the area of a rectangle."""
       return length * width
   ```
5. **Test individually** - Make sure each function works before combining them

## Common Mistakes

### 1. Forgetting Parentheses When Calling

```python
def greet():
    print("Hello!")

greet     # WRONG - doesn't call the function
greet()   # CORRECT
```

### 2. Using Function Before Definition

```python
greet()   # ERROR - function doesn't exist yet!

def greet():
    print("Hello!")
```

Define functions before you call them!

### 3. Forgetting to Return

```python
def add(a, b):
    result = a + b
    # Forgot return!

total = add(5, 3)
print(total)  # None (not what we wanted!)
```

### 4. Wrong Number of Arguments

```python
def greet(name, age):
    print(f"Hello, {name}! You are {age}.")

greet("Alice")  # ERROR - missing age
greet("Alice", 25)  # CORRECT
```

## Key Takeaways

1. **Functions** organize code into reusable blocks
2. **`def`** starts a function definition
3. **Parameters** let you pass data into functions
4. **`return`** sends data back from functions
5. **Call functions** using their name with parentheses
6. **Break large programs** into smaller functions
7. **One task per function** makes code clearer
8. **Test functions individually** before combining them

## Practice

Try this in IDLE or VS Code:

```python
# Write these functions:

def is_even(number):
    """Return True if number is even, False otherwise."""
    # Your code here
    pass

def count_even_numbers(numbers):
    """Count how many numbers in the list are even."""
    # Your code here
    pass

# Test them
print(is_even(4))   # Should print True
print(is_even(7))   # Should print False

my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(count_even_numbers(my_list))  # Should print 5
```

**Solution:**
```python
def is_even(number):
    """Return True if number is even, False otherwise."""
    return number % 2 == 0

def count_even_numbers(numbers):
    """Count how many numbers in the list are even."""
    count = 0
    for num in numbers:
        if is_even(num):
            count += 1
    return count
```

Notice how `count_even_numbers()` uses `is_even()` - functions can call other functions!

## Next Steps

Now that you understand functions, you can:
- Break complex programs into manageable pieces
- Reuse code efficiently
- Test and debug more easily
- Work on team projects where different people write different functions
