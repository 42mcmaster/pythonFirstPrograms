# Lesson 3g Tasks: While Loops Practice

## Setup
Complete these tasks in IDLE or VS Code. Be careful to avoid infinite loops!

---

## Task 1: Countdown Timer 
**Difficulty: Easy**

Write a program that counts down from 10 to 1, then prints "Blastoff!"

**Expected Output:**
```
10
9
8
7
6
5
4
3
2
1
Blastoff!
```

**Hints:**
- Start with `count = 10`
- Use `while count > 0:`
- Decrement with `count -= 1`

---

## Task 2: Sum Until Zero 
**Difficulty: Easy**

Create a program that keeps asking for numbers and adds them up until the user enters 0.

**Sample Run:**
```python
Enter a number (0 to stop): 5
Enter a number (0 to stop): 10
Enter a number (0 to stop): 3
Enter a number (0 to stop): 0
Total sum: 18
```

**Hints:**
- Use `while True:` loop
- Check if number is 0, then break
- Keep a running total

---

## Task 3: Password Validator 
**Difficulty: Medium**

Write a program that keeps asking for a password until the user enters the correct one.
The correct password is "python123".

**Sample Run:**
```python
Enter password: hello
Incorrect! Try again.
Enter password: test
Incorrect! Try again.
Enter password: python123
Access granted!
```

**Hints:**
- Use `while True:` loop
- Compare password to correct value
- Use `break` when correct

---

## Task 4: Average Calculator 
**Difficulty: Medium**

Absolutely — that’s a great catch. The term **“sentinel value”** can sound technical to beginners. Here’s a clearer, student-friendly rewrite of your task:

---

### 🧮 Task 4: Average Calculator

**Difficulty:** Medium

Create a program that calculates the average of numbers entered by the user.
The program should keep asking for numbers **until the user types `-1`**, which means *they’re done entering numbers*.

> 🔹 Don’t include `-1` in the average — it’s just the **stop signal**.

---

**Sample Run:**

```python
Enter a number (-1 to finish): 10
Enter a number (-1 to finish): 20
Enter a number (-1 to finish): 30
Enter a number (-1 to finish): -1
Average: 20.0
```

---

**Hints:**

* The answer is at the end of this document :) 
* Keep track of both the `total` of the values entered which you can call `num` and the `count`, which is the number of times a `num` was entered.
* When the user types `-1`, stop the loop.
* Then calculate:

```python
average = total / count
```

**Key Idea:**
`-1` isn’t part of the data collected for the average calculation — it’s just a special value that tells the program to **stop collecting input**.

---

## Task 5: Number Guessing Game 
**Difficulty: Medium**

Write a guessing game where the computer picks a random number between 1 and 50, and the user tries to guess it.
Give hints ("too high" or "too low") after each guess.

**Sample Run:**
```
I'm thinking of a number between 1 and 50...
Your guess: 25
Too low!
Your guess: 40
Too high!
Your guess: 35
Correct! You got it in 3 guesses!
```

**Hints:**
- `import random`
- `secret = random.randint(1, 50)`
- Keep count of guesses
- Use while True with break

---

## Task 6: Input Validation 
**Difficulty: Medium**

Create a program that asks for a grade and keeps asking until a valid grade (0-100) is entered.

**Sample Run:**
```
Enter a grade (0-100): 150
Invalid! Must be between 0 and 100.
Enter a grade (0-100): -5
Invalid! Must be between 0 and 100.
Enter a grade (0-100): 95
Valid grade accepted: 95
```

**Hints:**
- Use while True loop
- Check if `grade >= 0 and grade <= 100`
- Break when valid

---

## Task 7: Factorial Calculator 
**Difficulty: Medium**

Write a program that calculates the factorial of a number using a while loop.

**Sample Run:**
```
Enter a number: 5
5! = 120
```

**Hints:**
- Start with `product = 1` and `count = 1`
- Multiply product by count each time
- Continue while `count <= number`
- Remember to increment count!

---

## Task 8: ATM Simulator 
**Difficulty: Hard**

Create a simple ATM program with these features:
- Starting balance: $1000
- Menu options: Check Balance, Deposit, Withdraw, Exit
- Validate withdrawals (can't withdraw more than balance)
- Keep running until user chooses Exit

**Sample Run:**
```
ATM Menu:
1. Check Balance
2. Deposit
3. Withdraw
4. Exit
Choice: 1
Your balance: $1000.00

ATM Menu:
1. Check Balance
2. Deposit
3. Withdraw
4. Exit
Choice: 2
Deposit amount: $500
New balance: $1500.00

ATM Menu:
1. Check Balance
2. Deposit
3. Withdraw
4. Exit
Choice: 4
Thank you for using our ATM!
```

**Hints:**
- Use while True loop
- Use if-elif-else for menu choices
- Break when choice is "4"


## Submission Checklist

- [ ] No infinite loops (tested thoroughly!)
- [ ] Loop control variables properly updated
- [ ] Used appropriate loop type (while vs for)
- [ ] Input validation where needed
- [ ] Comments explain loop logic

## Debugging Infinite Loops

If your program hangs:
1. Press `Ctrl + C` to stop it
2. Check your loop control variable
3. Make sure you're updating it INSIDE the loop
4. Add print statements to see what's happening:
   ```python
   while count < 10:
       print(f"DEBUG: count = {count}")
       count += 1
   ```

## Common Mistakes to Avoid

1. **Never updating the control variable**
   ```python
   # WRONG - infinite loop
   x = 0
   while x < 5:
       print(x)  # Forgot to increment!
   ```

2. **Updating after using it wrong**
   ```python
   # WRONG - off by one
   count = 0
   while count < 5:
       count += 1
       print(count)  # Prints 1-5 instead of 0-4
   ```

3. **Wrong condition**
   ```python
   # WRONG - never runs
   count = 10
   while count < 5:  # Already false!
       print(count)
   ```

--- 

### 🧮 Task 4 Answer: 

# Average Calculator Program

```python
total = 0      # keeps track of the sum of all numbers
count = 0      # keeps track of how many numbers were entered

while True:
    num = int(input("Enter any number (-1 to stop): "))
    if num == -1:
        print("You're done!")
        break  # exit the loop when -1 is entered
    
    total += num   # add the number to the running total
    count += 1     # count how many valid numbers were entered

print(f"Average = {total / count}")

```