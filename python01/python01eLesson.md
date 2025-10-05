# Lesson 5: Writing Python Scripts

## Learning Objectives
- Create and save Python script files (.py)
- Run scripts from IDLE
- Understand the difference between shell and script mode
- Write programs with multiple lines of code
- Add comments to document code

## Shell vs. Script Mode

### Shell Mode (What we've been doing)
- Interactive: type code, get immediate results
- Great for: testing, experimenting, quick calculations
- **Problem:** Code disappears when you close IDLE!

### Script Mode (What we're learning now)
- Write code in a file, save it, run it anytime
- Great for: real programs you want to keep and share
- Files are saved with **.py** extension

## Creating Your First Script

### Step 1: Open a New Window

In IDLE:
- Click **File** → **New File**
- Or press **Ctrl+N** (Windows/Linux) or **Cmd+N** (Mac)

A new blank window appears - this is your **script editor**.

### Step 2: Write Your Code

Type this program:

```python
# My first Python program
# This program greets the user

name = input("What is your name? ")
print("Hello,", name + "!")
print("Welcome to Python programming!")
```

### Step 3: Save Your File

1. Click **File** → **Save** (or **Ctrl+S** / **Cmd+S**)
2. Choose where to save (create a "Python Programs" folder!)
3. Name your file: **greeting.py**
4. Click **Save**

**Important:** 
- Always use **.py** extension
- Use underscores for spaces: `my_program.py` (not `my program.py`)
- No special characters in filename

### Step 4: Run Your Script

- Click **Run** → **Run Module** 
- Or press **F5**

The shell window will appear and your program will run!

## Comments

**Comments** are notes in your code that Python ignores. They help humans understand what the code does.

### Single-Line Comments

Use `#` for comments:

```python
# This is a comment
name = input("Enter your name: ")  # Get the user's name
```

### Why Use Comments?

1. **Explain what code does**: Helps others (and future you!) understand
2. **Document your thinking**: Why did you write it this way?
3. **Temporarily disable code**: Add # to "turn off" a line

```python
# Calculate the area
width = 5
# height = 10  # Commented out for testing
height = 8
area = width * height
```

### Comment Best Practices

**Good comments:**
```python
# Convert Celsius to Fahrenheit
celsius = float(input("Enter temperature in C: "))
fahrenheit = celsius * 9/5 + 32
```

**Bad comments:**
```python
# Get input  (too obvious!)
celsius = float(input("Enter temperature in C: "))
# Multiply by nine fifths and add 32  (just repeating the code!)
fahrenheit = celsius * 9/5 + 32
```

**Rule:** Comment *why*, not *what* (if the what is obvious)

## Multi-Line Programs

Scripts can have many lines that execute in order, top to bottom:

```python
# Trip cost calculator
print("=== Trip Cost Calculator ===")
print()

distance = float(input("Enter distance in miles: "))
mpg = float(input("Enter your car's MPG: "))
price_per_gallon = float(input("Enter gas price: $"))

gallons_needed = distance / mpg
total_cost = gallons_needed * price_per_gallon

print()
print("Gallons needed:", gallons_needed)
print("Total cost: $", total_cost)
```

### Program Structure

Good programs have clear sections:

```python
# 1. Header comment (what the program does)
# 2. Input section (get data from user)
# 3. Processing section (do calculations)
# 4. Output section (display results)
```

## Common Script Errors

### Error 1: Forgot to Save

If you run without saving, you'll get:
```
Source Must Be Saved
   OK to Save?
```

Click **OK** to save first!

### Error 2: Syntax Error Before Running

IDLE won't run if there are syntax errors. Look for:
- Missing quotes: `print("Hello)`
- Missing parentheses: `print "Hello"`
- Misspelled keywords: `pint("Hello")`

### Error 3: IndentationError

```python
# Wrong!
name = input("Name: ")
  print("Hello", name)  # Extra spaces before print!
```

Python is picky about indentation (spaces at the start of lines). Don't indent unless you have a reason!

## Editing and Re-running Scripts

After you run a script:
1. Make changes in the editor window
2. **Save** (Ctrl+S)
3. **Run** again (F5)

You can run the same script over and over to test it!

## Testing Your Programs

Always test with different inputs:

```python
# Temperature converter
fahrenheit = float(input("Enter temperature in F: "))
celsius = (fahrenheit - 32) * 5 / 9
print(fahrenheit, "F =", celsius, "C")
```

**Test cases:**
- 32°F → 0°C ✓
- 212°F → 100°C ✓
- 98.6°F → 37°C ✓
- -40°F → -40°C ✓

## Script Template

Use this template for new programs:

```python
# Program: [Name]
# Author: [Your Name]
# Date: [Today's Date]
# Description: [What this program does]

# Input


# Processing


# Output

```

## Example Complete Script

```python
# Program: Rectangle Calculator
# Author: Alex Smith
# Date: October 4, 2025
# Description: Calculates area and perimeter of a rectangle

print("=== Rectangle Calculator ===")
print()

# Input
length = float(input("Enter the length: "))
width = float(input("Enter the width: "))

# Processing
area = length * width
perimeter = 2 * (length + width)

# Output
print()
print("Area:", area, "square units")
print("Perimeter:", perimeter, "units")
```

## Key Differences: Shell vs Script

| Aspect | Shell | Script |
|--------|-------|--------|
| Where you type | Shell window (>>>) | Editor window |
| When it runs | Immediately after Enter | When you press F5 |
| Saved? | No | Yes (.py file) |
| Can edit? | No (must retype) | Yes (save and run again) |
| Good for | Testing, exploring | Real programs |
| Shows prompts? | Yes (>>>) | No |

## Tips for Writing Scripts

1. **Start simple**: Get something working, then add features
2. **Test often**: Run your script frequently as you write it
3. **Save often**: Press Ctrl+S after every few lines
4. **Use comments**: Explain tricky parts
5. **Use blank lines**: Separate sections for readability
6. **Use descriptive names**: `total_cost` not `tc`

## Running Scripts Outside IDLE

You can also run scripts from your computer's terminal/command prompt:

```bash
python greeting.py
```

But for now, we'll use IDLE!