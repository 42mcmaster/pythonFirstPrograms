# Lesson 3g: While Loops and Conditional Iteration

## Learning Objectives
- Understand conditional iteration vs definite iteration
- Write while loops with proper continuation conditions
- Use while loops for input validation
- Implement while True loops with break statements
- Avoid infinite loops
- Convert between for and while loops

## Conditional Iteration

**Definite iteration** (for loops): You know exactly how many times to repeat
- "Print 10 times"
- "Process each character in this string"

**Indefinite iteration** (while loops): You repeat UNTIL something happens
- "Keep asking for input until the user enters 'quit'"
- "Roll dice until you get a 6"
- "Keep guessing until the correct answer"

## The While Loop

### Syntax

```python
while condition:
    statement1
    statement2
    # ... more statements
```

### How It Works

1. **Check the condition** (at the top of the loop)
2. If True: execute the loop body, then go back to step 1
3. If False: skip the loop body and continue with the rest of the program

### Important Terms

- **Entry-control loop**: Condition is tested BEFORE the loop body
- **Continuation condition**: The condition that keeps the loop running
- **Loop control variable**: Variable used in the continuation condition

## Example 1: Simple Input Loop

```python
theSum = 0.0
data = input("Enter a number or just press Enter to quit: ")

while data != "":
    number = float(data)
    theSum += number
    data = input("Enter a number or just press Enter to quit: ")

print(f"The sum is {theSum}")
```

**Sample Run:**
```
Enter a number or just press Enter to quit: 3
Enter a number or just press Enter to quit: 4
Enter a number or just press Enter to quit: 5
Enter a number or just press Enter to quit: 
The sum is 12.0
```

### Key Points
- `data` is the loop control variable
- First input is BEFORE the loop (initialization)
- Last input is INSIDE the loop (update)
- Empty string ("") is the **sentinel value** that stops the loop

## Example 2: Count-Controlled While Loop

A for loop can be rewritten as a while loop:

```python
# Using for loop
theSum = 0
for count in range(1, 100001):
    theSum += count
print(theSum)

# Using while loop (equivalent)
theSum = 0
count = 1
while count <= 100000:
    theSum += count
    count += 1
print(theSum)
```

### Pattern for Count-Controlled While Loops

1. **Initialize** the counter before the loop
2. **Test** the counter in the condition
3. **Update** the counter inside the loop

```python
counter = start_value           # 1. Initialize
while counter <= end_value:     # 2. Test
    # do something
    counter += 1                # 3. Update
```

## The while True Loop

Sometimes the condition check needs to happen in the MIDDLE of the loop.

### Syntax

```python
while True:
    # Get some input or do some work
    if termination_condition:
        break
    # Process the data
```

The `break` statement immediately exits the loop.

### Example: Input Validation

```python
while True:
    number = int(input("Enter a number between 1 and 10: "))
    if number >= 1 and number <= 10:
        break
    else:
        print("Invalid! Try again.")

print(f"You entered {number}")
```

**Sample Run:**
```
Enter a number between 1 and 10: 15
Invalid! Try again.
Enter a number between 1 and 10: -3
Invalid! Try again.
Enter a number between 1 and 10: 7
You entered 7
```

### When to Use while True

Use `while True` when:
- You need to get input BEFORE checking the condition
- The loop should run at least once
- The termination check is in the middle of the loop body

## Example 3: Guessing Game

```python
import random

secret = random.randint(1, 100)
guesses = 0

print("I'm thinking of a number between 1 and 100...")

while True:
    guesses += 1
    guess = int(input("Your guess: "))
    
    if guess == secret:
        print(f"Correct! You got it in {guesses} guesses!")
        break
    elif guess < secret:
        print("Too low!")
    else:
        print("Too high!")
```

## Using Boolean Flags

Another way to control a while loop: use a Boolean variable.

```python
done = False

while not done:
    number = int(input("Enter grade (0-100): "))
    
    if number >= 0 and number <= 100:
        done = True
        print("Valid grade accepted!")
    else:
        print("Error: Grade must be between 0 and 100")

# Process the valid grade
```

This is clearer than `while True` for some situations.

## Infinite Loops

An **infinite loop** runs forever because the condition never becomes False.

### Common Causes

**Mistake 1: Never updating the loop control variable**
```python
# INFINITE LOOP!
count = 0
while count < 10:
    print(count)
    # Forgot to increment count!
```

**Mistake 2: Wrong condition**
```python
# INFINITE LOOP!
count = 0
while count >= 0:  # This will always be True!
    print(count)
    count += 1
```

**Mistake 3: Updating wrong variable**
```python
# INFINITE LOOP!
count = 0
total = 0
while count < 10:
    total += 1  # Incrementing wrong variable!
```

### How to Stop an Infinite Loop

If your program hangs:
- **In IDLE or Terminal**: Press `Ctrl + C`
- **In VS Code**: Click the stop/kill button in the terminal

## Loop Patterns

### Pattern 1: Sentinel-Controlled Loop

```python
total = 0
value = input("Enter value (or 'done'): ")

while value != 'done':
    total += float(value)
    value = input("Enter value (or 'done'): ")

print(f"Total: {total}")
```

### Pattern 2: Counter-Controlled Loop

```python
count = 1
while count <= 10:
    print(count)
    count += 1
```

### Pattern 3: Validation Loop

```python
while True:
    age = int(input("Enter age: "))
    if age >= 0 and age <= 120:
        break
    print("Invalid age!")
```

### Pattern 4: Menu Loop

```python
choice = ""

while choice != "quit":
    print("\n1. New Game")
    print("2. Load Game")
    print("3. Quit")
    choice = input("Choice: ")
    
    if choice == "1":
        print("Starting new game...")
    elif choice == "2":
        print("Loading game...")
    elif choice == "3" or choice.lower() == "quit":
        print("Goodbye!")
        choice = "quit"
    else:
        print("Invalid choice!")
```

## For vs While: When to Use Which?

**Use a for loop when:**
- You know how many iterations needed
- You're traversing a sequence (string, list, range)
- You're counting through numbers

**Use a while loop when:**
- You don't know how many iterations needed
- You're waiting for user input
- You're checking a condition that might change
- You need input validation

## Converting For to While

Any for loop can be converted to a while loop:

**For loop:**
```python
for i in range(1, 11):
    print(i)
```

**Equivalent while loop:**
```python
i = 1
while i <= 10:
    print(i)
    i += 1
```

## Common Mistakes

### Mistake 1: Forgetting to Update

```python
# WRONG - infinite loop
x = 0
while x < 5:
    print(x)
    # Forgot x += 1
```

### Mistake 2: Wrong Initial Value

```python
# WRONG - loop never runs
x = 10
while x < 5:  # Already False!
    print(x)
    x += 1
```

### Mistake 3: Off-by-One Error

```python
# Want to print 1-10, but this prints 1-11
count = 1
while count <= 10:
    count += 1
    print(count)  # Incremented before printing!
```

**Fix:**
```python
count = 1
while count <= 10:
    print(count)
    count += 1  # Increment after printing
```

## Debugging While Loops

**Add print statements to see what's happening:**

```python
count = 0
total = 0

while count < 5:
    print(f"Debug: count={count}, total={total}")  # Debug line
    count += 1
    total += count

print(f"Final total: {total}")
```

## Complete Example: Simple ATM

```python
balance = 1000.00
pin = "1234"

# Login
attempts = 0
logged_in = False

while attempts < 3 and not logged_in:
    entered_pin = input("Enter PIN: ")
    if entered_pin == pin:
        logged_in = True
    else:
        attempts += 1
        if attempts < 3:
            print(f"Incorrect. {3 - attempts} attempts remaining.")

if not logged_in:
    print("Account locked!")
else:
    # Main menu
    while True:
        print(f"\nBalance: ${balance:.2f}")
        print("1. Deposit")
        print("2. Withdraw")
        print("3. Exit")
        
        choice = input("Choice: ")
        
        if choice == "1":
            amount = float(input("Deposit amount: $"))
            balance += amount
            print(f"New balance: ${balance:.2f}")
            
        elif choice == "2":
            amount = float(input("Withdraw amount: $"))
            if amount <= balance:
                balance -= amount
                print(f"New balance: ${balance:.2f}")
            else:
                print("Insufficient funds!")
                
        elif choice == "3":
            print("Thank you!")
            break
            
        else:
            print("Invalid choice!")
```

## Key Takeaways

1. **While loops** are for indefinite iteration
2. **Condition is checked before** each iteration
3. **Must update** the loop control variable
4. **while True** with break is useful for mid-loop checks
5. **Boolean flags** can make code clearer
6. **Infinite loops** happen when condition never becomes False
7. **Always have a way** for the loop to end
8. **Test your loops** with different inputs

## Practice

Try this in IDLE or VS Code:

```python
# Experiment: What does this print?
x = 5
while x > 0:
    print(x)
    x -= 1
print("Done!")

# Experiment: Will this ever stop?
count = 0
while count < 10:
    print(count)
    count += 2  # What effect does this have?
```