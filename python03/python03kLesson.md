# Lesson 3k: Error Handling and Exceptions

## Learning Objectives
- Understand what exceptions are
- Use try/except blocks to handle errors
- Handle multiple exception types
- Use else and finally clauses
- Raise exceptions intentionally
- Write more robust programs

## What Are Exceptions?

**Exception** = An error that occurs during program execution

Without handling, exceptions **crash** your program:

```python
# This crashes!
number = int("abc")  # ValueError!
```

**Error message:**
```
ValueError: invalid literal for int() with base 10: 'abc'
```

## Common Exception Types

| Exception | When It Occurs |
|-----------|----------------|
| **ValueError** | Invalid conversion (int("abc")) |
| **ZeroDivisionError** | Division by zero |
| **FileNotFoundError** | File doesn't exist |
| **IndexError** | List index out of range |
| **KeyError** | Dictionary key doesn't exist |
| **TypeError** | Wrong type (5 + "hello") |
| **NameError** | Variable not defined |

## The try/except Block

**Syntax:**
```python
try:
    # Code that might cause an error
    risky_code()
except ExceptionType:
    # What to do if error occurs
    handle_error()
```

## Example 1: Handling Invalid Input

**Without error handling (crashes):**
```python
age = int(input("Enter age: "))  # User types "abc" -> CRASH!
print(f"You are {age} years old")
```

**With error handling:**
```python
try:
    age = int(input("Enter age: "))
    print(f"You are {age} years old")
except ValueError:
    print("That's not a valid number!")
```

**Output when user enters "abc":**
```
Enter age: abc
That's not a valid number!
```

Program continues instead of crashing!

## Example 2: Safe Division

```python
try:
    num1 = int(input("Enter first number: "))
    num2 = int(input("Enter second number: "))
    result = num1 / num2
    print(f"Result: {result}")
except ValueError:
    print("Please enter valid numbers!")
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

**Sample runs:**
```
Enter first number: 10
Enter second number: 0
Cannot divide by zero!
```

```
Enter first number: abc
Please enter valid numbers!
```

## Catching Multiple Exceptions

### Method 1: Multiple except Blocks

```python
try:
    value = int(input("Enter a number: "))
    result = 100 / value
except ValueError:
    print("Invalid number format!")
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

### Method 2: Catch Multiple in One Block

```python
try:
    value = int(input("Enter a number: "))
    result = 100 / value
except (ValueError, ZeroDivisionError):
    print("Invalid input!")
```

### Method 3: Catch All Exceptions

```python
try:
    risky_operation()
except Exception as e:
    print(f"An error occurred: {e}")
```

**Note:** Be specific when possible - catching all exceptions can hide bugs!

## The else Clause

**`else`** runs if **NO** exception occurs:

```python
try:
    number = int(input("Enter a number: "))
except ValueError:
    print("Invalid input!")
else:
    print(f"You entered: {number}")  # Only if successful
    print("Processing...")
```

## The finally Clause

**`finally`** runs **no matter what** (exception or not):

```python
try:
    file = open("data.txt", "r")
    content = file.read()
except FileNotFoundError:
    print("File not found!")
finally:
    print("Cleanup code runs here")  # ALWAYS runs
```

**Common use:** Closing files, network connections, etc.

## Complete Example: Robust Input

```python
def get_integer(prompt, min_val=None, max_val=None):
    """Get a valid integer from user with optional range."""
    while True:
        try:
            value = int(input(prompt))
            
            # Check range if specified
            if min_val is not None and value < min_val:
                print(f"Must be at least {min_val}")
                continue
            if max_val is not None and value > max_val:
                print(f"Must be at most {max_val}")
                continue
                
            return value
            
        except ValueError:
            print("Please enter a valid integer!")

# Usage
age = get_integer("Enter age (1-120): ", 1, 120)
print(f"Age accepted: {age}")
```

**Sample run:**
```
Enter age (1-120): abc
Please enter a valid integer!
Enter age (1-120): 150
Must be at most 120
Enter age (1-120): 25
Age accepted: 25
```

## Raising Exceptions

You can **raise** exceptions intentionally with `raise`:

```python
def calculate_grade(score):
    """Calculate letter grade from score."""
    if score < 0 or score > 100:
        raise ValueError("Score must be between 0 and 100")
    
    if score >= 90:
        return "A"
    elif score >= 80:
        return "B"
    elif score >= 70:
        return "C"
    elif score >= 60:
        return "D"
    else:
        return "F"

# Using it
try:
    grade = calculate_grade(105)
except ValueError as e:
    print(f"Error: {e}")
```

**Output:**
```
Error: Score must be between 0 and 100
```

## Example: Safe File Reading

```python
def read_scores(filename):
    """Read scores from file, return list of integers."""
    scores = []
    
    try:
        with open(filename, "r") as file:
            for line in file:
                try:
                    score = int(line.strip())
                    scores.append(score)
                except ValueError:
                    print(f"Skipping invalid line: {line.strip()}")
    except FileNotFoundError:
        print(f"File {filename} not found!")
        return []
    
    return scores

# Using it
scores = read_scores("grades.txt")
if scores:
    print(f"Average: {sum(scores) / len(scores):.1f}")
else:
    print("No valid scores found")
```

## When to Use try/except

**Use try/except when:**
- Getting user input that needs conversion
- Opening files that might not exist
- Performing operations that could fail (division, etc.)
- Working with data that might be invalid

**Don't use try/except for:**
- Normal program logic (use if/else instead)
- Bugs you should fix
- Expected conditions (check with if first when possible)

## Good Practice vs Bad Practice

**❌ Bad: Hiding all errors**
```python
try:
    # 100 lines of code
except:
    pass  # Silently ignore all errors!
```

**✅ Good: Specific error handling**
```python
try:
    age = int(input("Age: "))
except ValueError:
    print("Please enter a number")
    age = 0  # Provide default
```

**❌ Bad: Using exceptions for control flow**
```python
try:
    result = 10 / value
except:
    result = 0  # Should use if instead!
```

**✅ Good: Check first when possible**
```python
if value != 0:
    result = 10 / value
else:
    result = 0
```

## Complete Program: Calculator with Error Handling

```python
def safe_calculate():
    """Perform calculation with full error handling."""
    print("=== CALCULATOR ===")
    
    try:
        # Get first number
        num1 = float(input("First number: "))
        
        # Get operator
        operator = input("Operator (+, -, *, /): ")
        if operator not in ['+', '-', '*', '/']:
            raise ValueError("Invalid operator")
        
        # Get second number
        num2 = float(input("Second number: "))
        
        # Calculate
        if operator == '+':
            result = num1 + num2
        elif operator == '-':
            result = num1 - num2
        elif operator == '*':
            result = num1 * num2
        elif operator == '/':
            if num2 == 0:
                raise ZeroDivisionError("Cannot divide by zero")
            result = num1 / num2
        
        print(f"Result: {result}")
        
    except ValueError as e:
        print(f"Invalid input: {e}")
    except ZeroDivisionError as e:
        print(f"Math error: {e}")
    except Exception as e:
        print(f"Unexpected error: {e}")
    else:
        print("Calculation successful!")
    finally:
        print("Calculator closing...")

# Run calculator
safe_calculate()
```

## Error Messages: Getting Information

```python
try:
    risky_operation()
except Exception as e:
    print(f"Error type: {type(e).__name__}")
    print(f"Error message: {e}")
```

## Key Takeaways

1. **try/except** prevents crashes from exceptions
2. **Be specific** - catch specific exception types when possible
3. **else** runs only if no exception occurred
4. **finally** always runs (cleanup code)
5. **raise** to trigger exceptions intentionally
6. **Don't hide errors** - handle them appropriately
7. **Use for unpredictable situations** (user input, files, etc.)

## Common Patterns

### Pattern 1: Retry Loop
```python
while True:
    try:
        value = int(input("Number: "))
        break  # Success! Exit loop
    except ValueError:
        print("Try again!")
```

### Pattern 2: Default Value
```python
try:
    age = int(input("Age: "))
except ValueError:
    age = 0  # Use default
    print("Using default age: 0")
```

### Pattern 3: File with Fallback
```python
try:
    with open("config.txt") as f:
        config = f.read()
except FileNotFoundError:
    config = "default settings"  # Use defaults
```

## Practice

Try running this and enter invalid inputs:

```python
def test_exceptions():
    """Test different exception types."""
    
    # Test 1: ValueError
    try:
        number = int(input("Enter a number: "))
        print(f"You entered: {number}")
    except ValueError:
        print("ValueError caught!")
    
    # Test 2: ZeroDivisionError
    try:
        result = 10 / 0
    except ZeroDivisionError:
        print("ZeroDivisionError caught!")
    
    # Test 3: IndexError
    try:
        my_list = [1, 2, 3]
        print(my_list[10])
    except IndexError:
        print("IndexError caught!")
    
    print("Program completed without crashing!")

test_exceptions()
```
