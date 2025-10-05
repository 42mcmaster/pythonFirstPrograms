# Lesson 2a: Software Development & Documentation

## Learning Objectives
By the end of this lesson, you will be able to:
- Describe the basic phases of software development
- Understand why testing is important
- Write comments in Python using `#`
- Create docstrings using triple quotes
- Explain why documentation matters

## The Software Development Process

When professional programmers create software, they follow a structured process. One common approach is called the **waterfall model**, which includes these phases:

1. **Customer Request** - Understanding what needs to be built
2. **Analysis** - Figuring out the requirements and constraints
3. **Design** - Planning how the program will work
4. **Implementation** - Actually writing the code
5. **Integration** - Combining different parts together
6. **Testing** - Making sure everything works correctly
7. **Maintenance** - Fixing bugs and adding features

### Why Testing Matters

Here's an important fact: **Programs rarely work correctly the first time they're run!**

Look at this chart showing the cost of fixing mistakes in different phases:

- Fixing a mistake during **Analysis**: Low cost
- Fixing a mistake during **Design**: Medium cost  
- Fixing a mistake during **Implementation**: Higher cost
- Fixing a mistake during **Integration**: Even higher cost
- Fixing a mistake during **Maintenance**: VERY HIGH cost!

**The lesson:** It's much cheaper to catch mistakes early. That's why testing is so important!

## Comments in Python

Comments are notes you write in your code that Python ignores. They help other programmers (and future you!) understand what your code does.

### End-of-Line Comments

Use the `#` symbol to create a comment that goes to the end of the line:

```python
# This is a comment - Python will ignore this line
print("Hello!")  # This comment explains the code to the left

# Comments can explain what variables mean
age = 15  # The student's age in years
```

### Docstrings

A **docstring** is a special multi-line comment that describes what a program does. Use triple quotes (`"""` or `'''`):

```python
"""
Program: greeting.py
Author: Your Name
Date: Today's date

This program greets the user and tells them their age next year.
Input: The user's name and current age
Output: A personalized greeting and their age next year
"""

name = input("What is your name? ")
age = int(input("How old are you? "))
print(f"Hello {name}! Next year you'll be {age + 1} years old.")
```

## Documentation Best Practices

Good programmers document their code well. Here are some tips:

1. **Start with a docstring** - Put one at the beginning of every program with:
   - Program name
   - Your name
   - Date
   - What the program does
   - What inputs it needs
   - What outputs it produces

2. **Comment your variables** - Especially if the purpose isn't obvious:
   ```python
   TAX_RATE = 0.07  # 7% sales tax rate for our state
   ```

3. **Explain complex sections** - If code is tricky, add a comment explaining why:
   ```python
   # Convert Fahrenheit to Celsius using the formula: C = (F - 32) × 5/9
   celsius = (fahrenheit - 32) * 5 / 9
   ```

4. **Keep comments current** - If you change code, update the comments too!

## When NOT to Comment

Don't write obvious comments that just repeat what the code says:

```python
# BAD - This comment just repeats the code
age = age + 1  # Add 1 to age

# GOOD - This comment explains WHY
age = age + 1  # Calculate age on next birthday
```

## Summary

- Software development follows structured phases
- Testing is crucial and gets more expensive the later you do it
- Use `#` for single-line comments
- Use `"""..."""` for docstrings and multi-line comments
- Good documentation makes code easier to understand and maintain
- Every program should start with a docstring explaining what it does

## Key Terms

- **Software Development** - The process of planning and creating computer programs
- **Waterfall Model** - A sequential software development process
- **Comment** - Text in code that Python ignores, used to explain code to humans
- **Docstring** - A multi-line string used for documentation, enclosed in triple quotes
- **Testing** - Running a program to find and fix errors

## Next Lesson Preview

In the next lesson, we'll learn about strings (text data) and variables, which let us store and manipulate information in our programs.