# 🎲 The Great Dice Rolling Challenge 🎲

## Team Competition Rules
- Work in pairs (2 students per team)
- First **3 teams** to complete the challenge win!
- Help each other, but no copying code from other teams
- Test your program before calling me over to verify

---

## Part 1: Meet the Random Function

Before we start rolling dice, you need to learn about Python's `random` module. This module lets your program make random choices, just like rolling a real die!

### How to Use Random

First, you need to import the random module at the very top of your program:

```python
import random
```

### The random.randint() Function

The `randint()` function gives you a random integer between two numbers (including both endpoints).

**Syntax:**
```python
random.randint(start, end)
```

**Examples:**
```python
# Get a random number from 1 to 6 (like a die!)
die_roll = random.randint(1, 6)

# Get a random number from 1 to 100
score = random.randint(1, 100)

# Get a random number from 60 to 88
temperature = random.randint(60, 80)
```

### Try It Out!

Before starting the challenge, run this small test program:

```python
import random

for i in range(5):
    roll = random.randint(1, 6)
    print(f"Roll {i+1}: {roll}")
```

Run it a few times. Notice how the numbers change each time? That's randomness!

---

## Part 2: Your Challenge Mission 🎯

### The Goal
Create a program that simulates rolling a die multiple times and calculates the **average** result.

### What Your Program Must Do:

1. **Ask the user** how many times they want to roll the die
2. **Roll the die** that many times (using a for loop)
3. **Keep track** of the total of all rolls (using a counter)
4. **Print each roll** as it happens (so the user can see the results)
5. **Calculate the average** of all the rolls
6. **Print the average** at the end

### Example Output:

If the user enters 5 rolls, your output might look like:

```
How many rolls of the die?: 5
Die 1: 4
Die 2: 2
Die 3: 6
Die 4: 3
Die 5: 5
Average roll: 4.0
```

---

## Step-by-Step Guide 

Oops - this part isn't provided - this is the challenge... you need to develop the logic together!

---

## But... I'll give you some hints & tips 💡

**Hint 1:** Remember that `range(1, rolls + 1)` starts at 1 and goes up to (and including) the number of rolls.

**Hint 2:** To calculate an average, divide the total by the number of rolls: `counter / rolls`

**Hint 3:** Use an f-string to make your output look nice: `print(f"Die {i}: {die}")`

**Hint 4:** Make sure your counter variable is created BEFORE the for loop, not inside it!

**Hint 5:** The division for the average should happen AFTER the for loop is completely finished.

---

## Testing Your Program

Before you call me over, test your program with these inputs:

1. Try 10 rolls - does your average seem reasonable (between 1 and 6)?
2. Try 100 rolls - the average should be closer to 3.5
3. Try 1 roll - does it work correctly?

---

## When You're Done ✅

Raise your hand and I'll come verify your program. Be ready to:
- Explain how your code works
- Run it for me with different inputs
- Answer questions about what each part does

**Remember:** The first 3 teams to complete this successfully WIN! 