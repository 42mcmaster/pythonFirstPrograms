# Lesson 3l: Built-in Modules and Tools

## Learning Objectives
- Import and use built-in Python modules
- Perform mathematical operations with the math module
- Work with dates and times using datetime
- Interact with the operating system using os and os.path
- Use command-line arguments with sys

## What Are Modules?

**Module** = A file containing Python code (functions, variables, classes)

Python has many **built-in modules** ready to use:
- **math** - mathematical functions
- **datetime** - dates and times
- **random** - random numbers (you already know this!)
- **os** - operating system operations
- **sys** - system-specific functions

## The math Module

### Importing

```python
import math

# Now use math.function_name()
result = math.sqrt(16)
```

### Common Math Functions

```python
import math

# Square root
print(math.sqrt(25))           # 5.0

# Power
print(math.pow(2, 3))          # 8.0

# Absolute value
print(math.fabs(-10))          # 10.0

# Rounding functions
print(math.ceil(4.2))          # 5 (round up)
print(math.floor(4.8))         # 4 (round down)
print(math.trunc(4.9))         # 4 (remove decimals)

# Constants
print(math.pi)                 # 3.14159...
print(math.e)                  # 2.71828...

# Trig functions (in radians)
print(math.sin(math.pi / 2))   # 1.0
print(math.cos(0))             # 1.0
```

### More Math Functions

```python
import math

# Check if number is NaN (Not a Number)
print(math.isnan(float('nan')))  # True

# Modulo (remainder)
print(math.fmod(10, 3))          # 1.0

# Integer square root
print(math.isqrt(17))            # 4 (largest int whose square ≤ 17)
```

## Example 1: Circle Calculator

```python
import math

def circle_area(radius):
    """Calculate area of circle."""
    return math.pi * radius ** 2

def circle_circumference(radius):
    """Calculate circumference of circle."""
    return 2 * math.pi * radius

# Get radius
radius = float(input("Enter radius: "))

# Calculate and display
area = circle_area(radius)
circumference = circle_circumference(radius)

print(f"Area: {area:.2f}")
print(f"Circumference: {circumference:.2f}")
```

**Sample Run:**
```
Enter radius: 5
Area: 78.54
Circumference: 31.42
```

## The datetime Module

Work with dates and times!

### Getting Current Date/Time

```python
import datetime

# Current date and time
now = datetime.datetime.now()
print(now)  # 2025-11-09 14:30:45.123456

# Just the date
today = datetime.date.today()
print(today)  # 2025-11-09

# Components
print(now.year)        # 2025
print(now.month)       # 11
print(now.day)         # 9
print(now.hour)        # 14
print(now.minute)      # 30
print(now.weekday())   # 5 (0=Monday, 6=Sunday)
```

### Formatting Dates

```python
import datetime

now = datetime.datetime.now()

# Format as string
formatted = now.strftime("%Y-%m-%d %H:%M:%S")
print(formatted)  # 2025-11-09 14:30:45

# Different formats
print(now.strftime("%B %d, %Y"))        # November 09, 2025
print(now.strftime("%A"))               # Saturday
print(now.strftime("%I:%M %p"))         # 02:30 PM
```

**Common Format Codes:**
- `%Y` - Year (4 digits)
- `%m` - Month (01-12)
- `%d` - Day (01-31)
- `%H` - Hour (00-23)
- `%M` - Minute (00-59)
- `%S` - Second (00-59)
- `%A` - Weekday name
- `%B` - Month name

## Example 2: Birthday Calculator

```python
import datetime

# Get birthday
year = int(input("Birth year: "))
month = int(input("Birth month: "))
day = int(input("Birth day: "))

# Create birthday object
birthday = datetime.date(year, month, day)

# Calculate age
today = datetime.date.today()
age = today.year - birthday.year

# Adjust if birthday hasn't occurred this year
if (today.month, today.day) < (birthday.month, birthday.day):
    age -= 1

print(f"You are {age} years old")

# Days until next birthday
next_birthday = datetime.date(today.year, birthday.month, birthday.day)
if next_birthday < today:
    next_birthday = datetime.date(today.year + 1, birthday.month, birthday.day)

days_until = (next_birthday - today).days
print(f"Days until birthday: {days_until}")
```

## The os and os.path Modules

Interact with the file system!

### os Module

```python
import os

# Get current directory
print(os.getcwd())  # /Users/Ryan/Desktop

# List files in directory
files = os.listdir()
for file in files:
    print(file)

# Check if file exists
if os.path.exists("data.txt"):
    print("File exists!")

# Get file size (bytes)
size = os.path.getsize("data.txt")
print(f"Size: {size} bytes")

# Is it a file or directory?
print(os.path.isfile("data.txt"))  # True
print(os.path.isdir("folder"))     # True
```

### Working with Paths

```python
import os.path

filename = "data.txt"

# Check existence
print(os.path.exists(filename))

# Get absolute path
print(os.path.abspath(filename))

# Split filename
name, extension = os.path.splitext(filename)
print(f"Name: {name}")        # data
print(f"Extension: {extension}")  # .txt

# Join paths (works on any OS)
path = os.path.join("folder", "subfolder", "file.txt")
print(path)  # folder/subfolder/file.txt (or folder\subfolder\file.txt on Windows)
```

## Example 3: File Information Display

```python
import os
import os.path
import datetime

filename = input("Enter filename: ")

if os.path.exists(filename):
    # Get file size
    size = os.path.getsize(filename)
    
    # Get modification time
    mod_time = os.path.getmtime(filename)
    mod_date = datetime.datetime.fromtimestamp(mod_time)
    
    # Display info
    print(f"\nFile: {filename}")
    print(f"Size: {size} bytes")
    print(f"Modified: {mod_date.strftime('%Y-%m-%d %H:%M:%S')}")
    print(f"Is file: {os.path.isfile(filename)}")
else:
    print("File not found!")
```

## The sys Module

System-specific parameters and functions.

### Command-Line Arguments

```python
import sys

# sys.argv is a list of command-line arguments
# sys.argv[0] is the script name
# sys.argv[1], sys.argv[2], etc. are additional arguments

print(f"Script name: {sys.argv[0]}")
print(f"Number of arguments: {len(sys.argv) - 1}")

if len(sys.argv) > 1:
    print("Arguments:")
    for i, arg in enumerate(sys.argv[1:], 1):
        print(f"  {i}. {arg}")
```

**Running from command line:**
```bash
python script.py hello world 123
```

**Output:**
```
Script name: script.py
Number of arguments: 3
Arguments:
  1. hello
  2. world
  3. 123
```

## Example 4: Simple File Processor

```python
import sys
import os.path

# Check if filename provided
if len(sys.argv) < 2:
    print("Usage: python script.py <filename>")
    sys.exit(1)

filename = sys.argv[1]

# Check if file exists
if not os.path.exists(filename):
    print(f"Error: {filename} not found!")
    sys.exit(1)

# Process file
with open(filename, "r") as file:
    lines = file.readlines()
    print(f"File has {len(lines)} lines")
    
    # Count words
    word_count = sum(len(line.split()) for line in lines)
    print(f"Total words: {word_count}")
```

## Combining Modules

Real programs often use multiple modules together:

```python
import math
import datetime
import os

def log_calculation(operation, result):
    """Log a calculation to file with timestamp."""
    timestamp = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    
    with open("calc_log.txt", "a") as file:
        file.write(f"[{timestamp}] {operation} = {result}\n")

# Perform calculation
radius = 5
area = math.pi * radius ** 2

# Log it
log_calculation(f"Circle area (r={radius})", f"{area:.2f}")

print("Calculation logged!")
```

## Module Import Variations

### Import entire module
```python
import math
print(math.sqrt(16))
```

### Import specific functions
```python
from math import sqrt, pi
print(sqrt(16))  # No "math." needed
print(pi)
```

### Import with alias
```python
import datetime as dt
now = dt.datetime.now()
```

### Import everything (not recommended)
```python
from math import *
print(sqrt(16))  # Works, but can cause name conflicts
```

## Key Takeaways

1. **import module_name** to use built-in modules
2. **math** - sqrt, pow, ceil, floor, pi, trig functions
3. **datetime** - now(), today(), strftime(), date calculations
4. **os/os.path** - file operations, path handling, file info
5. **sys** - command-line arguments (sys.argv)
6. **Combine modules** for powerful programs
7. **Read documentation** - these modules have many more functions!

## Quick Reference

### Math Module
```python
import math
math.sqrt(x)      # Square root
math.pow(x, y)    # x to the power y
math.ceil(x)      # Round up
math.floor(x)     # Round down
math.fabs(x)      # Absolute value
math.pi           # 3.14159...
```

### Datetime Module
```python
import datetime
datetime.datetime.now()           # Current date/time
datetime.date.today()             # Current date
now.strftime("%Y-%m-%d")         # Format as string
now.weekday()                     # Day of week (0-6)
```

### OS Module
```python
import os
os.path.exists(file)              # Check if exists
os.path.getsize(file)             # File size
os.path.isfile(file)              # Is it a file?
os.getcwd()                       # Current directory
os.listdir()                      # List files
```

## Practice Exercise

Try combining modules:

```python
import math
import datetime

# Calculate and log
def calculate_and_log():
    # Get input
    radius = float(input("Circle radius: "))
    
    # Calculate
    area = math.pi * radius ** 2
    
    # Create log entry
    timestamp = datetime.datetime.now()
    log_entry = f"{timestamp.strftime('%Y-%m-%d %H:%M:%S')} - Radius: {radius}, Area: {area:.2f}\n"
    
    # Save to file
    with open("calculations.log", "a") as file:
        file.write(log_entry)
    
    print(f"Area: {area:.2f}")
    print("Calculation logged!")

calculate_and_log()
```
