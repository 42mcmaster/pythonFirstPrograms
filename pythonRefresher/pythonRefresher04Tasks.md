# Python Refresher 04 - Task File
## Loops (while and for)


## Instructions
- Complete each problem below in its own separate Python file
- Name each file according to the problem (e.g., `problem_4_01.py`, `problem_4_02.py`)
- Test your code thoroughly
- Make sure your loops don't run forever!
- Save all files in a folder called `pythonRefresherTasks`
- Commit and push to your Python GitHub repo

---

## PROBLEM 1: Count to 10 
**File name:** `problem_4_01.py`

Use a for loop to print the numbers 1 through 10.
Each number should be on its own line.

---

## PROBLEM 2: Countdown 
**File name:** `problem_4_02.py`

Use a for loop to count down from 10 to 1.
Then print "Blastoff!" 

---

## PROBLEM 3: Sum Calculator 
**File name:** `problem_4_03.py`

Ask the user how many numbers they want to enter.
Use a for loop to get that many numbers from the user.
Calculate and print the sum of all the numbers.

---

## PROBLEM 4: Even Numbers 
**File name:** `problem_4_04.py`

Use a for loop to print all even numbers from 2 to 20.

**Hint:** Use `range(2, 21, 2)`

---

## PROBLEM 5: Multiplication Table 
**File name:** `problem_4_05.py`

Ask the user for a number.
Use a for loop to print the multiplication table for that number (1-10).

**Example:** If user enters 5, print:
```
5 x 1 = 5
5 x 2 = 10
...
5 x 10 = 50
```

---

## PROBLEM 6: Password Validator 
**File name:** `problem_4_06.py`

Use a while loop to keep asking for a password until the user enters "python123".
If they enter the wrong password, print "Incorrect, try again."
When they get it right, print "Access granted!" 

---

## PROBLEM 7: Positive Numbers Only 
**File name:** `problem_4_07.py`

Use a while loop to keep asking the user for numbers.
Stop when they enter a negative number.
Calculate and print the sum of all positive numbers entered.

---

## PROBLEM 8: Factorial Calculator 
**File name:** `problem_4_08.py`

Ask the user for a positive integer.
Calculate the factorial using a for loop.

**Factorial of n** = n × (n-1) × (n-2) × ... × 1

**Example:** Factorial of 5 = 5 × 4 × 3 × 2 × 1 = 120

---

## PROBLEM 9: Find the Average 
**File name:** `problem_4_09.py`

Ask the user how many test scores they want to enter.
Use a for loop to get each score.
Calculate and print:
- The highest score
- The lowest score  
- The average score

---

## PROBLEM 10: Number Guessing Game
**File name:** `problem_4_10.py`

Generate a random number between 1 and 50.
Use a while loop to let the user keep guessing.
After each guess, tell them if they're too high or too low.
When they guess correctly, tell them how many tries it took.

**You'll need:**
```python
import random
secret = random.randint(1, 50)
```

---


## Submission Checklist

When you're finished:
- [ ] Test each problem thoroughly
- [ ] Make sure no infinite loops!
- [ ] Save all your `.py` files in the `pythonRefresherTasks` folder
- [ ] Ensure you have created files for all problems: `problem_4_01.py` through `problem_4_10.py`
- [ ] Add, commit, and push your folder to your Python GitHub repo
- [ ] Verify your submission appears on GitHub

