# Lesson 3b Tasks: Range and Counting Practice

## Setup
Complete these tasks in IDLE or VS Code. Save each as a separate `.py` file.

---

## Task 1: Number Printer 
**Difficulty: Easy**

Write a program that prints the numbers 5 through 15 (inclusive), each on a new line.

**Expected Output:**
```
5
6
7
8
9
10
11
12
13
14
15
```
---

## Task 2: Even Numbers 
**Difficulty: Easy**

Create a program that prints all even numbers from 0 to 20 on one line, separated by spaces.

**Expected Output:**
```
0 2 4 6 8 10 12 14 16 18 20
```

**Hints:**
- Use `range()` with a step of 2
- Use `end=" "` in your print statement

---

## Task 3: Countdown Display 
**Difficulty: Medium**

Write a countdown program that:
1. Asks the user for a starting number
2. Counts down from that number to 1
3. Prints "Liftoff!" at the end

**Sample Run:**
```
Enter starting number: 5
5
4
3
2
1
Liftoff!
```

**Hints:**
- Use a negative step in range: `range(start, 0, -1)`
- The "Liftoff!" print should be AFTER the loop (not indented)

---

## Task 4: Sum Calculator 
**Difficulty: Medium**

Create a program that calculates the sum of all numbers from 1 to a user-specified number.

**Sample Run:**
```
Enter a number: 100
The sum of numbers 1 to 100 is 5050
```

**Hints:**
- Start with `total = 0`
- Use a for loop to add each number to the total
- Use `range(1, number + 1)` to include the last number

---

## Task 5: Multiplication Table 
**Difficulty: Medium**

Write a program that prints a multiplication table for a number entered by the user.
Show the number multiplied by 1 through 10.

**Sample Run:**
```
Enter a number: 7
7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
7 x 4 = 28
7 x 5 = 35
7 x 6 = 42
7 x 7 = 49
7 x 8 = 56
7 x 9 = 63
7 x 10 = 70
```

**Hints:**
- Use `range(1, 11)` to get numbers 1-10
- Calculate: `result = number * i`
- Use an f-string or format string to display nicely

---

## Task 6: Range Calculator 
**Difficulty: Medium**

Create a program that:
1. Asks for a lower bound
2. Asks for an upper bound  
3. Calculates and prints the sum of all numbers in that range (inclusive)

**Sample Run:**
```
Enter lower bound: 5
Enter upper bound: 10
The sum of numbers from 5 to 10 is 45
```

**Verification:** 5+6+7+8+9+10 = 45 ✓

---

## Task 7: Odd Sum 
**Difficulty: Hard**

Write a program that calculates the sum of all ODD numbers between 1 and a user-specified number.

**Sample Run:**
```
Enter a number: 10
The sum of odd numbers from 1 to 10 is 25
```

**Verification:** 1+3+5+7+9 = 25 ✓

**Hints:**
- Use `range(1, number + 1, 2)` to get odd numbers
- Or use `if num % 2 == 1:` to check if odd

---

## Task 8: Number Pattern 
**Difficulty: Hard**

Create a program that prints numbers in this pattern:
```
1 2 3 4 5 6 7 8 9 10
10 9 8 7 6 5 4 3 2 1
```

**Requirements:**
- First line counts up from 1 to 10
- Second line counts down from 10 to 1
- Numbers on each line separated by spaces

**Hints:**
- Use two separate for loops
- First loop: `range(1, 11)`
- Second loop: `range(10, 0, -1)`

---

## Task 9: Average Calculator 
**Difficulty: Hard**

Write a program that:
1. Asks how many numbers to process
2. For each number:
   - Asks the user to enter a number
   - Adds it to a running total
3. Calculates and prints the average

**Sample Run:**
```
How many numbers? 4
Enter number 1: 10
Enter number 2: 20
Enter number 3: 30
Enter number 4: 40
The average is 25.0
```

**Hints:**
- Use `range(1, count + 1)` to get the right number of iterations
- Keep track of the sum
- Calculate average: `average = total / count`
- The answer is at the end!

---

## Challenge Task: Fibonacci Sequence 
**Difficulty: Challenge**

The Fibonacci sequence starts with 0 and 1. Each following number is the sum of the previous two numbers: 0, 1, 1, 2, 3, 5, 8, 13, 21...

Write a program that:
1. Asks the user how many Fibonacci numbers to generate
2. Prints that many numbers in the sequence

**Sample Run:**
```
How many Fibonacci numbers? 10
0 1 1 2 3 5 8 13 21 34
```

**Hints:**
- Start with `a = 0` and `b = 1`
- In each loop iteration:
  - Print the current number
  - Calculate the next number: `next_num = a + b`
  - Update: `a = b` and `b = next_num`

---

## Bonus Challenge: Prime Number Checker 
**Difficulty: Very Hard**

Write a program that checks if a number is prime.

A prime number is only divisible by 1 and itself (like 2, 3, 5, 7, 11, 13...)

**Sample Run 1:**
```
Enter a number: 17
17 is prime!
```

**Sample Run 2:**
```
Enter a number: 15
15 is not prime.
```

**Hints:**
- A number is prime if it has no divisors from 2 to (number-1)
- Use a loop to check each possible divisor
- Use the modulus operator (%) to check divisibility
- Think about when to print "is prime" vs "is not prime"

```python
# Ask how many numbers to process
count = int(input("How many numbers? "))

# Initialize a variable to keep track of the total
total = 0

# Loop through the specified number of times
for i in range(1, count + 1):
    number = float(input(f"Enter number {i}: "))
    total += number  # Add each number to the running total

# Calculate the average
average = total / count

# Display the result
print(f"The average is {average}")

```

---

## Submission Checklist

- [ ] All programs run without errors
- [ ] Code is properly indented
- [ ] Variables have meaningful names
- [ ] Comments explain what the code does
- [ ] Each task saved as separate file
- [ ] Tested with different inputs
