# Lesson 2a Tasks: Software Development & Documentation

## Task 1: Understanding the Development Process (Written Response)

Answer these questions in complete sentences:

1. Why is it more expensive to fix a bug during the maintenance phase than during the analysis phase?

2. List the 7 phases of the waterfall model in order.

3. Explain in your own words why testing is important in software development.

4. If you're writing a program to calculate student grades, which phase would involve deciding what letter grade (A, B, C, etc.) corresponds to each percentage range?

## Task 2: Comment Practice

Open IDLE or VS Code and create a new file called `comment_practice.py`. Add comments to this code to explain what it does:

```python
name = "Alex"
age = 16
city = "Portland"

print(name)
print(age)
print(city)

age = age + 1
print(age)
```

**Your task:** Add at least 4 meaningful comments to explain what this code does. Use `#` for your comments.

## Task 3: Create Your First Documented Program

Create a new file called `about_me.py` with the following:

1. A docstring at the top that includes:
   - Program name
   - Your name
   - Today's date
   - Description: "This program displays information about me"
   - Input: None
   - Output: Personal information

2. Create variables for:
   - Your name
   - Your age
   - Your favorite subject
   - Your favorite hobby

3. Add a comment above each variable explaining what it stores

4. Use `print()` to display all four pieces of information with labels

**Example output:**
```
Name: Jordan Smith
Age: 15
Favorite Subject: Computer Science
Favorite Hobby: Gaming
```

## Task 4: Fix the Comments

This code has comments, but they're not very helpful. Rewrite the comments to be more meaningful:

```python
# variable
temperature = 72

# math
celsius = (temperature - 32) * 5 / 9

# output
print(celsius)
```

## Task 5: Docstring Detective

Look at this program and answer the questions:

```python
"""
Program: mystery_calc.py
Author: Ms. Johnson
Date: March 15, 2024

This program calculates the area of a rectangle.
Input: Length and width from the user
Output: The area of the rectangle
"""

length = float(input("Enter the length: "))
width = float(input("Enter the width: "))
area = length * width
print(f"The area is {area} square units")
```

Questions:
1. What does this program do?
2. What inputs does it need?
3. Who wrote this program?
4. What would happen if you entered "ten" instead of "10" for the length?

## Task 6: Plan Before You Code

Before writing code, professional programmers plan! Practice this by:

1. Choose a simple program idea (examples: calculate pizza cost with tax, convert hours to minutes, calculate your age in days)

2. Write a program plan that includes:
   - What problem does it solve?
   - What inputs are needed?
   - What calculations or processing is needed?
   - What should be output?

3. Create a docstring for your planned program (you don't need to write the actual code yet - just the documentation!)

## Challenge Task: Documentation Review

Find a program you wrote in an earlier class or create a simple one now. Then:

1. Add a complete docstring if it doesn't have one
2. Add at least 3 helpful comments throughout the code
3. Make sure all variable names are clear and self-explanatory
4. If you have any "magic numbers" (like `0.07` for tax rate), create a named constant with a comment explaining it

## Reflection Questions

Write 2-3 sentences answering each:

1. Why do you think professional programmers spend time writing comments and documentation?

2. Have you ever gone back to look at old work (in any subject) and had trouble remembering what you did or why? How might good documentation have helped?

3. Do you think the waterfall model would work well for all types of projects? Why or why not?

## Submission Checklist

Before submitting your work, make sure:
- [ ] All Python files run without errors
- [ ] Every Python file has a docstring at the top
- [ ] You've used comments to explain your code
- [ ] Variable names are clear and meaningful
- [ ] You've answered all written questions in complete sentences
- [ ] Your code is properly indented and easy to read

## Going Further (Optional)

Research the "Agile" software development methodology. How is it different from the waterfall model? Which do you think would work better for a small team building a mobile app? Write a paragraph explaining your answer.