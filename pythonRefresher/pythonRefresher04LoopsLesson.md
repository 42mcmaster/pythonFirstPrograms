---
marp: true
theme: default
paginate: true
---

# Python Refresher 04
## Loops (while and for)

**Medina County Career Center**
Instructor: Mr. McMaster

---

## Learning Objectives

By the end of this lesson, you will be able to:
- Use `while` loops to repeat code
- Use `for` loops to iterate through sequences
- Use `range()` to create number sequences
- Understand when to use each type of loop
- Avoid infinite loops

---

## What are Loops?

**Loops** let you repeat code multiple times without writing it over and over.

Instead of:
```python
print("Hello")
print("Hello")
print("Hello")
```

Use a loop:
```python
for i in range(3):
    print("Hello")
```

---

## The while Loop

A `while` loop repeats **as long as a condition is True**.

```python
count = 1

while count <= 5:
    print(count)
    count = count + 1
```

**Output:**
```
1
2
3
4
5
```

---

## How while Loops Work

1. Check the condition
2. If True → run the code inside
3. Go back to step 1
4. If False → exit the loop

```python
count = 1
while count <= 3:    # Is count <= 3? If yes, continue
    print(count)     # Print the number
    count += 1       # Increase count by 1
```

---

## Important: Updating the Counter

You **must** change the variable that the condition checks, or you'll get an **infinite loop**!

❌ **INFINITE LOOP:**
```python
count = 1
while count <= 5:
    print(count)
    # Forgot to increase count!
```

✅ **CORRECT:**
```python
count = 1
while count <= 5:
    print(count)
    count += 1
```

---

## Example: Countdown

```python
seconds = 10

while seconds > 0:
    print(seconds)
    seconds -= 1

print("Blastoff!")
```

---

## Example: Input Validation

```python
password = ""

while password != "python123":
    password = input("Enter the password: ")
    if password != "python123":
        print("Incorrect. Try again.")

print("Access granted!")
```

---

## The for Loop

A `for` loop repeats a **specific number of times** or goes through a **sequence**.

```python
for i in range(5):
    print(i)
```

**Output:**
```
0
1
2
3
4
```

---

## The range() Function

`range()` creates a sequence of numbers.

**Three ways to use range():**

1. `range(stop)` → 0 to stop-1
2. `range(start, stop)` → start to stop-1
3. `range(start, stop, step)` → start to stop-1, counting by step

---

## range() Examples

```python
# range(5) → 0, 1, 2, 3, 4
for i in range(5):
    print(i)

# range(1, 6) → 1, 2, 3, 4, 5
for i in range(1, 6):
    print(i)

# range(0, 10, 2) → 0, 2, 4, 6, 8
for i in range(0, 10, 2):
    print(i)
```

---

## Example: Print 1-10

```python
for num in range(1, 11):
    print(num)
```

Remember: `range(1, 11)` goes up to (but not including) 11.

---

## Example: Countdown with for Loop

```python
for num in range(10, 0, -1):
    print(num)

print("Blastoff!")
```

The third parameter is the step (here, -1 means count down).

---

## Looping Through Strings

You can loop through each character in a string:

```python
name = "Python"

for letter in name:
    print(letter)
```

**Output:**
```
P
y
t
h
o
n
```

---

## Example: Count Vowels

```python
word = input("Enter a word: ")
vowels = "aeiouAEIOU"
count = 0

for letter in word:
    if letter in vowels:
        count += 1

print("Number of vowels:", count)
```

---

## Accumulator Pattern

An **accumulator** builds up a value inside a loop:

```python
# Sum of numbers 1-10
total = 0

for num in range(1, 11):
    total += num

print("Sum:", total)  # 55
```

---

## Example: Calculate Average

```python
total = 0

for i in range(5):
    num = int(input("Enter a number: "))
    total += num

average = total / 5
print("Average:", average)
```

---

## Nested Loops

You can put loops inside other loops:

```python
for i in range(1, 4):
    for j in range(1, 4):
        print(f"{i} x {j} = {i*j}")
    print()  # Blank line between groups
```

---

## Example: Multiplication Table

```python
for row in range(1, 6):
    for col in range(1, 6):
        print(row * col, end=" ")
    print()  # New line after each row
```

**Output:**
```
1 2 3 4 5 
2 4 6 8 10 
3 6 9 12 15 
4 8 12 16 20 
5 10 15 20 25 
```

---

## while vs for Loops

**Use `for` when:**
- You know how many times to repeat
- You're going through a sequence (like a string or range)

**Use `while` when:**
- You repeat until a condition changes
- You don't know how many iterations you need

---

## Example: Guess the Number

```python
import random

secret = random.randint(1, 10)
guess = 0

while guess != secret:
    guess = int(input("Guess a number (1-10): "))
    
    if guess < secret:
        print("Too low!")
    elif guess > secret:
        print("Too high!")

print("You got it!")
```

---

## break Statement

`break` exits a loop immediately:

```python
for num in range(1, 11):
    if num == 5:
        break
    print(num)

print("Done!")
```

**Output:** `1 2 3 4 Done!`

---

## continue Statement

`continue` skips the rest of the current iteration:

```python
for num in range(1, 6):
    if num == 3:
        continue
    print(num)
```

**Output:** `1 2 4 5` (skips 3)

---

## Common Mistakes

**Mistake 1:** Off-by-one errors
```python
# Want to print 1-10, but this only prints 1-9
for i in range(1, 10):
    print(i)
```

**Fix:**
```python
for i in range(1, 11):  # Remember: stop is exclusive
    print(i)
```

---

## Common Mistakes

**Mistake 2:** Forgetting to update while loop counter
```python
count = 1
while count <= 5:
    print(count)
    # Missing: count += 1
```

Always make sure the condition can eventually become False!

---

## Common Mistakes

**Mistake 3:** Using the wrong loop type
```python
# Awkward way to do a fixed count
count = 0
while count < 5:
    print(count)
    count += 1
```

**Better:**
```python
for i in range(5):
    print(i)
```

---

## Loop Control Summary

| Statement | Effect |
|-----------|--------|
| `break` | Exit the loop immediately |
| `continue` | Skip to next iteration |
| Normal flow | Continue until condition is False |

---

## Practice: Sum of Even Numbers

```python
# Sum all even numbers from 1-20
total = 0

for num in range(2, 21, 2):  # Start at 2, count by 2
    total += num

print("Sum of even numbers:", total)
```

---

## Practice: User Input Loop

```python
# Keep asking until user enters "quit"
while True:
    command = input("Enter a command (or 'quit' to exit): ")
    
    if command == "quit":
        break
    
    print("You entered:", command)

print("Goodbye!")
```

---

## Lesson Summary

✓ `while` loops repeat while a condition is True
✓ `for` loops iterate through sequences or ranges
✓ `range()` creates number sequences
✓ Use accumulators to build values in loops
✓ `break` exits a loop, `continue` skips to next iteration
✓ Always make sure loops can end!

---

## Task Time!

Open **python_refresher_04_task.py**

Complete the practice problems to master loops.

**Remember:**
- Avoid infinite loops
- Test with different inputs
- Use the right loop for the job!
