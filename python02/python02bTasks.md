# Lesson 2b Tasks: Strings and Variables

## Task 1: String Basics

Create a file called `string_practice.py` and complete these exercises:

```python
# 1. Create a variable with your full name using double quotes


# 2. Create a variable with your favorite quote that contains an apostrophe


# 3. Create a variable with the empty string


# 4. Print all three variables
```

## Task 2: Escape Sequence Practice

Create a file called `escape_sequences.py` that uses escape sequences to print this EXACT output:

```
Line 1
	Line 2 (indented with a tab)
Line 3 has a "quote" in it
Line 4 shows a backslash: \
```

Your code should use `\n`, `\t`, `\"`, and `\\` escape sequences.

## Task 3: String Concatenation

Create a file called `name_builder.py` that:

1. Asks the user for their first name
2. Asks the user for their last name
3. Creates a variable called `full_name` by concatenating first name, a space, and last name
4. Prints a greeting using the full name

**Example run:**
```
Enter your first name: Alex
Enter your last name: Johnson
Hello, Alex Johnson! Welcome to Python!
```

## Task 4: ASCII Art

Create a file called `ascii_art.py` that uses string repetition and concatenation to create a simple picture. Here's a simple house example to get you started:

```python
# Create a house using string operations
roof = "   /\\   "
walls = "  |  |  "
base = "  ----  "

print(roof)
print(walls)
print(base)
```

Now create your own ASCII art! Ideas:
- A tree
- A smiley face
- A car
- Your initials
- Be creative!

Use the `*` operator to repeat characters and `+` to join strings.

## Task 5: Variable Naming Practice

Look at these variable names. Mark each one as ✅ VALID or ❌ INVALID according to Python's rules. If invalid, explain why:

1. `student_name` -
2. `2nd_place` -
3. `final-score` -
4. `_private` -
5. `myClass` -
6. `class` -
7. `first name` -
8. `TOTAL_POINTS` -
9. `score#1` -
10. `age` -

## Task 6: Fix the Variable Names

This code works, but the variable names are terrible! Rewrite it with good, descriptive variable names:

```python
x = "Sarah"
y = 16
z = "Soccer"

print(x)
print(y)
print(z)

a = x + " is " + str(y) + " years old."
print(a)
```

## Task 7: Personal Information Display

Create a file called `about_me_improved.py` that:

1. Creates variables for:
   - Your name
   - Your age
   - Your grade level
   - Your favorite class
   - Your favorite food

2. Uses string concatenation to create ONE long string variable that contains all this information with labels

3. Prints the result with a decorative border

**Example output:**
```
**********************************
* Name: Jordan Smith            *
* Age: 15                        *
* Grade: 10th                    *
* Favorite Class: Computer Sci   *
* Favorite Food: Pizza           *
**********************************
```

## Task 8: Mad Lib Generator

Create a file called `my_mad_lib.py` that:

1. Asks the user for at least 5 different words (nouns, verbs, adjectives, etc.)
2. Stores each word in a descriptively-named variable
3. Combines them into a short, silly story
4. Displays the story with a nice border or separator

Be creative with your story! Make it funny!

## Task 9: Receipt Builder

Create a file called `receipt.py` that simulates a store receipt:

1. Ask the user for:
   - Store name
   - Item name
   - Item price (as a string for now - we'll handle numbers next lesson)
   - Customer name

2. Build a receipt that looks like:

```
================================
       STORE NAME
================================
Item: ITEM_NAME
Price: $PRICE
================================
Thank you for shopping with us,
CUSTOMER_NAME!
================================
```

Use escape sequences and string operations to make it look nice!

## Task 10: Text Formatter

Create a file called `text_formatter.py` that:

1. Asks the user for a sentence
2. Displays that sentence:
   - In all uppercase (use `.upper()` method)
   - In all lowercase (use `.lower()` method)
   - Repeated 3 times
   - Centered with asterisks on both sides

**Example:**
```
Enter a sentence: Hello World

UPPERCASE: HELLO WORLD
lowercase: hello world
Repeated: Hello WorldHello WorldHello World
Centered: ***** Hello World *****
```

## Challenge Task: Pattern Maker

Create a file called `pattern.py` that asks the user for:
- A character to use
- A number of times to repeat it

Then create three different patterns using that character. For example, if they enter `*` and `5`:

```
Pattern 1:
*****

Pattern 2:
*
**
***
****
*****

Pattern 3:
*****
****
***
**
*
```

Hint: You'll need to use loops for patterns 2 and 3, OR you can build them manually for now using string repetition and `\n`.

## Debugging Challenge

This code has several problems. Find and fix ALL the errors:

```python
# Bug Hunt!
1student = "Alice"
score-total = 95
favorite class = "Math"

message = 'It's almost done!'
print(message)

border = "*" 5
print(border)

name = "Bob
print(name)
```

Save your fixed version as `debug_fixed.py`.

## Reflection Questions

Answer these in a text file called `lesson2_reflection.txt`:

1. Why do you think Python allows both single and double quotes for strings? When would you choose one over the other?

2. Explain the difference between these two statements:
   ```python
   print("5" + "3")
   print(5 + 3)
   ```

3. Why is it important to use descriptive variable names instead of short names like `x` or `y`?

4. Give an example of when you might use the empty string (`""` or `''`).

## Submission Checklist

Make sure all your files:
- [ ] Have a docstring at the top
- [ ] Have good variable names
- [ ] Run without errors
- [ ] Produce the expected output
- [ ] Are properly commented
- [ ] Use meaningful variable names

Files to submit:
- `string_practice.py`
- `escape_sequences.py`
- `name_builder.py`
- `ascii_art.py`
- `about_me_improved.py`
- `my_mad_lib.py`
- `receipt.py`
- `text_formatter.py`
- `debug_fixed.py`
- `lesson2_reflection.txt`
- (Optional) `pattern.py`

## Going Further (Optional)

Research and try out these string methods:
- `.upper()` and `.lower()`
- `.strip()`
- `.replace()`
- `.count()`

Create a file called `string_methods.py` that demonstrates each of these methods with comments explaining what they do.