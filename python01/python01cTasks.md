# Tasks 1c: Interactive Shell Basics

## Task 1: Variable Practice (15 minutes)

Open IDLE and create these variables. After creating each set, use `print()` to display them.

**Part A: About You**
```python
>>> name = "Your Name"
>>> age = Your Age
>>> grade = Your Grade
>>> favorite_color = "Your Favorite Color"
>>> print("My name is", name, "and I am", age, "years old")
```

Record what prints: ___________________________________

**Part B: Math Variables**
```python
>>> length = 10
>>> width = 5
>>> area = length * width
>>> print("The area is", area)
```

Record the result: ___________________________________

**Part C: String Variables**
```python
>>> first_name = "John"
>>> last_name = "Doe"
>>> full_name = first_name + " " + last_name
>>> print(full_name)
```

Record the result: ___________________________________

## Task 2: Data Type Detective (15 minutes)

For each variable, predict the type, then check using `type()`:

| Variable | Your Prediction | Actual Type (use type()) |
|----------|----------------|-------------------------|
| `x = 42` | | |
| `y = 3.14` | | |
| `z = "100"` | | |
| `a = "3.14"` | | |
| `b = 7.0` | | |

**Questions:**
1. What's the difference between `100` and `"100"`?
2. What's the difference between `7` and `7.0`?

## Task 3: Error Investigation (10 minutes)

Try each of these in IDLE and record what happens:

```python
# Example 1
>>> print(student_name)
```
Error message: ___________________________________
How to fix it: ___________________________________

```python
# Example 2
>>> my-age = 16
```
Error message: ___________________________________
Why doesn't this work? ___________________________________

```python
# Example 3
>>> print("Hello + "World")
```
Error message: ___________________________________
What's wrong? ___________________________________

```python
# Example 4
>>> result = 5 + "3"
```
Error message: ___________________________________
How could you fix this? ___________________________________

## Task 4: String Operations (15 minutes)

Use IDLE to complete these challenges:

**Challenge 1:** Create a variable with your first name and another with your last name. Combine them with a space to create your full name.

```python
>>> first = 
>>> last = 
>>> full = 
>>> print(full)
```

**Challenge 2:** Create a line of 30 equal signs (=) using string repetition.

```python
>>> line = 
>>> print(line)
```

**Challenge 3:** Create this pattern using string operations:
```
***
***
***
```

```python
>>> pattern = 
>>> print(pattern)
```

**Challenge 4:** Make your name appear 3 times:
```
Alex Alex Alex
```

```python
>>> name = "Alex"
>>> repeated = 
>>> print(repeated)
```

## Task 5: Variable Reassignment (10 minutes)

Type this code sequence and record what happens after each line:

```python
>>> score = 0
>>> print("Score:", score)

>>> score = score + 10
>>> print("Score:", score)

>>> score = score + 5
>>> print("Score:", score)

>>> score = score * 2
>>> print("Score:", score)
```

**Questions:**
1. What is the final value of `score`? _________
2. Explain in your own words what `score = score + 10` does:
   ___________________________________
3. Why doesn't `score = score + 10` cause an error?
   ___________________________________

## Task 6: Using help() (10 minutes)

Use the `help()` function to answer these questions:

```python
>>> help(print)
```

1. Can the `print()` function take more than one value?
2. What does the `sep` parameter do?
3. What does the `end` parameter do?

Try this:
```python
>>> print("Hello", "World", sep="-")
>>> print("Python", end="!")
>>> print("Rocks")
```

What's different about the output?

## Extension Challenge (Optional)

### Mad Libs Generator

Create variables for different parts of speech, then combine them into a silly sentence:

```python
>>> adjective1 = "sparkly"
>>> noun1 = "unicorn"
>>> verb = "dancing"
>>> adjective2 = "purple"
>>> noun2 = "banana"

>>> sentence = "The " + adjective1 + " " + noun1 + " was " + verb + " with a " + adjective2 + " " + noun2
>>> print(sentence)
```

Create your own mad lib with at least 5 variables!

## Reflection Questions

1. What's the difference between typing `age` and typing `"age"` in Python?
2. Why are variables useful instead of just typing values directly?
3. What's one thing you found confusing about variables?