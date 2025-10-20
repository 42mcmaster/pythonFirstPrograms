# Lesson 3h Tasks: Random Numbers and Final Projects

## Setup
These tasks combine everything from Chapter 3. Test thoroughly!

---

## Task 1: Dice Roller 
**Difficulty: Easy**

Write a program that simulates rolling a six-sided die 10 times and displays the results.

**Expected Output:**
```
Rolling a die 10 times:
3 6 2 4 1 5 6 3 2 4
```

**Hints:**
- `import random`
- Use `random.randint(1, 6)`
- Use a for loop with `range(10)`

---

## Task 2: Coin Flip Simulator 
**Difficulty: Easy**

Create a program that simulates flipping a coin 20 times and counts heads and tails.

**Sample Output:**
```
Flipping a coin 20 times...
H T H H T T H T H H T H T T H H H T T H
Heads: 11
Tails: 9
```

**Hints:**
- Use `random.randint(0, 1)` (0=heads, 1=tails)
- Keep two counters
- Print "H" or "T" based on result

---

## Task 3: Random Number Guesser 
**Difficulty: Medium**

Write a program where the computer guesses YOUR number!
- You think of a number between 1-100
- Computer makes guesses
- You tell it "higher", "lower", or "correct"

**Sample Run:**
```
Think of a number between 1 and 100...
My guess is 50. (higher/lower/correct): higher
My guess is 75. (higher/lower/correct): lower
My guess is 62. (higher/lower/correct): correct
I got it in 3 guesses!
```

**Hints:**
- Computer picks random numbers
- Keep trying until correct
- Count guesses

---

## Task 4: Lottery Number Generator 
**Difficulty: Medium**

Create a program that generates 6 unique lottery numbers between 1 and 49.
Make sure no number appears twice.

**Sample Output:**
```
Your lottery numbers: 7 23 15 42 8 31
```

**Hints:**
- Use a list to store numbers
- Before adding a number, check if it's already in the list
- Keep generating until you have 6 unique numbers
- Use `in` operator: `if num not in numbers:`

---

## Task 5: Higher or Lower Game 
**Difficulty: Medium**

Create a game where:
- Computer shows a random number (1-100)
- Player guesses if next number will be higher or lower
- Computer generates next number
- Track wins and losses

**Sample Run:**
```
Current number: 45
Will the next number be (h)igher or (l)ower? h
Next number: 67
You win!

Current number: 67
Will the next number be (h)igher or (l)ower? l
Next number: 89
You lose!

Score: 1 wins, 1 loss
```

**Hints:**
- Generate two numbers
- Compare them based on guess
- Keep track of score

---

## Task 6: Random Math Quiz 
**Difficulty: Hard**

Write a program that:
- Generates 10 random addition problems
- Numbers between 1-50
- Keeps track of correct/incorrect answers
- Shows final score

**Sample Run:**
```
Question 1: 23 + 17 = 40
Correct!

Question 2: 45 + 8 = 50
Incorrect! The answer is 53.

...

Quiz complete!
Score: 8 out of 10 (80%)
```

**Hints:**
- Use a for loop for 10 questions
- `num1 = random.randint(1, 50)`
- `num2 = random.randint(1, 50)`
- Calculate `correct_answer = num1 + num2`
- Compare to user's answer

---

## Task 7: Random Walk Simulation 
**Difficulty: Hard**

Simulate a "random walk" where you:
- Start at position 0
- Each step: randomly move +1 or -1
- Take 100 steps
- Show final position

**Sample Output:**
```
Starting random walk...
Final position after 100 steps: -12
```

Then extend it to show a simple visualization:
```
Final position: -12
|----*----0----+----+----+----+----+---|
```

**Hints:**
- `position = 0`
- Loop 100 times
- `step = random.randint(0, 1)` (0 for -1, 1 for +1)
- Or use: `step = random.choice([-1, 1])`

---

## Task 8: Rock-Paper-Scissors Tournament 
**Difficulty: Hard**

Create an enhanced rock-paper-scissors game:
- Best of 5 rounds
- Keep score for player and computer
- Show results after each round
- Declare overall winner

**Sample Run:**
```
ROUND 1
Your choice (rock/paper/scissors): rock
Computer chose: scissors
You win this round!
Score - You: 1, Computer: 0

ROUND 2
...

FINAL SCORE
You: 3
Computer: 2
You win the tournament!
```

**Hints:**
- Use a for loop for 5 rounds
- Use `random.choice(['rock', 'paper', 'scissors'])`
- Track two scores
- Determine winner after all rounds

---

## Task 9: Password Generator 
**Difficulty: Hard**

Create a random password generator that:
- Asks for desired password length
- Generates random password with:
  - Uppercase letters
  - Lowercase letters
  - Numbers
  - Special characters
- Ensures at least one of each type

**Sample Run:**
```
Password length: 12
Generated password: aB7#xK2$mP9!
```

**Hints:**
- Create strings with each character type
- Use `random.choice()` to pick characters
- Ensure you pick at least one from each category

---

## Task 10: Number Statistics Analyzer 
**Difficulty: Hard**

Write a program that:
- Generates 100 random numbers (1-50)
- Calculates and displays:
  - Highest number
  - Lowest number
  - Average
  - Most common number
  - How many even vs odd

**Sample Output:**
```
Generated 100 random numbers between 1 and 50.

Statistics:
Highest: 50
Lowest: 1
Average: 25.3
Most common: 17 (appeared 5 times)
Even numbers: 52
Odd numbers: 48
```

**Hints:**
- Store all numbers in a list
- Use max() and min() functions
- Count occurrences with a loop
- Use % 2 to check even/odd

---

## Testing Checklist for Random Programs

When testing programs with random elements:

- [ ] Run multiple times to see different outcomes
- [ ] Check that random ranges are correct
- [ ] Verify randomness looks distributed (not always same number)
- [ ] Test edge cases (what if random number is minimum? maximum?)
- [ ] Ensure program handles all possible random outcomes

## Chapter 3 Mastery Checklist

By completing these tasks, you should be able to:

- [ ] Write for loops for definite iteration
- [ ] Use range() with 1, 2, and 3 arguments
- [ ] Traverse strings with loops
- [ ] Format output with field widths
- [ ] Write if/elif/else statements
- [ ] Use comparison operators
- [ ] Use logical operators (and, or, not)
- [ ] Write while loops for indefinite iteration
- [ ] Use break to exit loops
- [ ] Generate random numbers
- [ ] Debug loop errors
- [ ] Combine loops, selection, and random for complete programs

## Congratulations!

You've completed Chapter 3! You now have powerful programming tools:
- **Loops** to repeat actions
- **Selection** to make choices
- **Random** to add unpredictability

These are the building blocks of most programs. Great job! 