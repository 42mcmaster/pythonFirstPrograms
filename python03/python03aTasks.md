# Lesson 3.1 Tasks: For Loops Practice

## Setup
You can complete these tasks in either:
- **IDLE**: Python's built-in editor
- **VS Code**: With Python extension installed

Save each task as a separate `.py` file with a descriptive name.

---

## Task 1: Countdown Timer ⭐
**Difficulty: Easy**

Write a program that prints "Blast off!" exactly 10 times using a for loop.

**Expected Output:**
```
Blast off!
Blast off!
Blast off!
(... 7 more times ...)
```

**Hints:**
- Use `range(10)`
- Remember to indent the print statement

---

## Task 2: Square Calculator ⭐
**Difficulty: Easy**

Create a program that prints the squares of numbers 1 through 5.

**Expected Output:**
```
1
4
9
16
25
```

**Hints:**
- You'll need a loop that runs 5 times
- Use a variable to track the current number
- Multiply the number by itself to get its square

---

## Task 3: Name Repeater ⭐⭐
**Difficulty: Medium**

Write a program that:
1. Asks the user for their name
2. Asks how many times to print it
3. Prints the name that many times on the same line, separated by spaces

**Sample Run:**
```
Enter your name: Alex
How many times? 4
Alex Alex Alex Alex
```

**Hints:**
- Use `input()` to get the name and number
- Use `int()` to convert the number to an integer
- Use `end=" "` in your print statement

---

## Task 4: Factorial Calculator ⭐⭐
**Difficulty: Medium**

Write a program that calculates the factorial of a number.
- Factorial means: 5! = 5 × 4 × 3 × 2 × 1 = 120

Your program should:
1. Ask the user for a number
2. Calculate its factorial using a for loop
3. Print the result

**Sample Run:**
```
Enter a number: 5
The factorial of 5 is 120
```

**Hints:**
- Start with `product = 1`
- Use `range(1, number + 1)` to get numbers 1 through the user's number
- Multiply product by each number in the loop

---

## Task 5: Power Calculator ⭐⭐⭐
**Difficulty: Hard**

Create a program that calculates any number raised to any power WITHOUT using the `**` operator.

Your program should:
1. Ask for a base number
2. Ask for an exponent
3. Calculate base^exponent using a for loop
4. Display each step of the calculation

**Sample Run:**
```
Enter the base: 3
Enter the exponent: 4
3
9
27
81
3 to the power of 4 is 81
```

**Hints:**
- Start with `result = 1`
- Multiply result by the base number, exponent times
- Print the result after each multiplication
- Print a final summary message

---

## Task 6: Pattern Printer ⭐⭐⭐
**Difficulty: Hard**

Write a program that prints this pattern:
```
*
**
***
****
*****
```

**Requirements:**
- Use a for loop
- Use string concatenation or augmented assignment

**Hints:**
- Start with an empty string: `stars = ""`
- Each iteration, add one more star
- Print the stars each time through the loop

---

## Challenge Task: Triangle Area Calculator 🌟
**Difficulty: Challenge**

Create a program that calculates the area of multiple triangles.

Your program should:
1. Ask how many triangles to process
2. For each triangle:
   - Ask for the base
   - Ask for the height
   - Calculate the area (area = 0.5 × base × height)
   - Print the result
3. After all triangles, print the total area

**Sample Run:**
```
How many triangles? 3

Triangle 1:
Enter base: 10
Enter height: 5
Area: 25.0

Triangle 2:
Enter base: 6
Enter height: 4
Area: 12.0

Triangle 3:
Enter base: 8
Enter height: 3
Area: 12.0

Total area of all triangles: 49.0
```

---

## Submission Guidelines

1. Test each program thoroughly
2. Make sure your code is properly indented
3. Add comments explaining what your code does
4. Save each task as a separate file: `task_3_1_1.py`, `task_3_1_2.py`, etc.

## Getting Help

If you get stuck:
1. Review the lesson content
2. Try running the examples from the lesson
3. Check your indentation carefully
4. Ask a classmate or your teacher for help