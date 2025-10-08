# Lesson 3b_1: Count-Controlled Loops, Range, and Formatted Output

## Learning Objectives
- Use loops to count through a range of numbers
- Specify explicit lower and upper bounds with range()
- Use a step value to skip numbers
- Create loops that count down
- Use the loop variable in calculations
- Format output into aligned tables and reports

## Understanding Range

The `range()` function creates a sequence of numbers. It can take 1, 2, or 3 arguments.

### One Argument: range(stop)
```python
range(4)  # Creates: 0, 1, 2, 3
```
- Starts at 0
- Stops BEFORE the number given
- Goes up by 1

### Two Arguments: range(start, stop)
```python
range(1, 5)  # Creates: 1, 2, 3, 4
```
- Starts at the first number
- Stops BEFORE the second number
- Goes up by 1

### Three Arguments: range(start, stop, step)
```python
range(1, 10, 2)  # Creates: 1, 3, 5, 7, 9
```
- Starts at the first number
- Stops BEFORE the second number
- Goes up (or down) by the step value

## Count-Controlled Loops

A **count-controlled loop** uses the loop variable as a counter.

### Example 1: Using the Counter

```python
product = 1
for count in range(1, 5):
    product = product * count
print(product)  # Output: 24 (which is 1 * 2 * 3 * 4)
```

### Example 2: Summation with Bounds

```python
lower = int(input("Enter the lower bound: "))
upper = int(input("Enter the upper bound: "))

theSum = 0
for number in range(lower, upper + 1):
    theSum = theSum + number

print("The sum is", theSum)
```

**Sample Run:**
```
Enter the lower bound: 1
Enter the upper bound: 10
The sum is 55
```

**Important:** We use `upper + 1` because range stops BEFORE the last number!

## Using Steps

### Counting by 2s
```python
for count in range(2, 11, 2):
    print(count, end=" ")
# Output: 2 4 6 8 10
```

### Counting by 3s
```python
for count in range(1, 10, 3):
    print(count, end=" ")
# Output: 1 4 7
```

### Visualizing Range
```python
# See what range creates
print(list(range(1, 6, 1)))    # [1, 2, 3, 4, 5]
print(list(range(1, 6, 2)))    # [1, 3, 5]
print(list(range(1, 6, 3)))    # [1, 4]
```

## Counting Down

Use a **negative step** to count backwards!

```python
for count in range(10, 0, -1):
    print(count, end=" ")
# Output: 10 9 8 7 6 5 4 3 2 1
```

### Example: Countdown Timer
```python
import time

print("Rocket launch countdown!")
for seconds in range(10, 0, -1):
    print(seconds)
    time.sleep(1)  # Wait 1 second
print("BLAST OFF!")
```
To be continued with formatting output... in lesson 3b_2