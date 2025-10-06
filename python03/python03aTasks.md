# Lesson 3a Tasks: For Loops Practice

## Setup
You can complete these tasks in either:
- **IDLE**: Python's built-in editor
- **VS Code**: With Python extension installed

Save each task as a separate `.py` file with a descriptive name.

Create a new GitHub Repo called pythonCh3 and push all of your completed files to the Repo. 

Submit the link to your public Repo in the Google Classroom Assignment. 

---

## Task 1: Countdown Timer 
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

## Task 2: Square Calculator 
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
- Multiply the number by itself to get its square (i * i), but you can also use the exponent operator "**"

---

## Task 3: Name Repeater 
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

## Task 4: Factorial Calculator 
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
- The answer to this one is at the end, if you're really struggling

---

## Task 5: Free Throw Tracker 
**Difficulty: Hard**

Create a program that tracks the score of a basketball player’s free throws.

Your program should:
1. Ask the user how many free throw attempts they want to simulate.
2. For each attempt, ask if the shot was made (y) or missed (n).
3. Use a loop to keep track of the total points (each made shot = 1 point).
4. Print the score after each attempt.
5. Print the final score at the end.

**Sample Run**
```sql
How many free throws will you attempt? 5
Shot 1 (y/n): y
Current score: 1
Shot 2 (y/n): n
Current score: 1
Shot 3 (y/n): y
Current score: 2
Shot 4 (y/n): y
Current score: 3
Shot 5 (y/n): n
Current score: 3
Final score: 3 out of 5
```
Hints
* Start with score = 0
* Use for i in range(attempts): to loop through the shots
* Each time the user enters y, add 1 point to the score
* Print the running total inside the loop

---

## Task 6: Pattern Printer 
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
- Use string concatenation `( + )`or augmented assignment `( += )`

**Hints:**
- Start with an empty string: `stars = ""`
- Each iteration, add one more star
- Print the stars each time through the loop
- The answer to this one is also at the end, but try to work this out yourself, first!

---

## Challenge Task: Triangle Area Calculator 
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
5. Push your files to your GitHub Repo called `pythonCh3`
6. Share the link to your GitHub Repo (make sure it's public) in Google Classroom

## Getting Help

If you get stuck:
1. Review the lesson content
2. Try running the examples from the lesson
3. Check your indentation carefully
4. Ask a classmate or your teacher for help

```python
## Task 4: Factorial Calculator 

# Ask the user for a number
number = int(input("Enter a number: "))

# Start with product = 1 (factorial identity)
product = 1

# Loop through numbers 1 up to the entered number
for i in range(1, number + 1):
    product = product * i   # multiply product by i

# Print the result
print(f"The factorial of {number} is {product}")
```

```python
## Task 6: Pattern Printer

# Start with an empty string
stars = ""

# Loop 5 times
for i in range(5):
    stars += "*"      # add one star 
    print(stars)      # print the current string

```