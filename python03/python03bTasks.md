# Lesson 3b Tasks: String Traversal and Formatting Practice

## Setup
Complete these tasks in IDLE or VS Code. Test with various inputs!

---

## Task 1: Character Printer 
**Difficulty: Easy**

Write a program that asks the user for a word and prints each character on a separate line.

**Sample Run:**
```
Enter a word: Python
P
y
t
h
o
n
```

**Starter Code:**
```python
# Get input from user
word = input("Enter a word: ")

# Loop through each character
for ____ in ____:  # TODO: fill in the blanks, print the output
    
```

---

## Task 2: Letter Counter 
**Difficulty: Easy**

Create a program that counts how many letters 'a' (lowercase) appear in a user-entered text.

**Sample Run:**
```
Enter some text: banana
The letter 'a' appears 3 times
```

**Starter Code:**
```python
# Get text from user
text = _____("Enter some text: ") # TODO: fill in the blanks

# Initialize counter
count = 0

# Loop through each character
for char in text:
    # TODO: Check if character is 'a'
    # TODO: If yes, increment count

# Print result
print("The letter 'a' appears", count, "times")
```

---

## Task 3: Vowel and Consonant Counter 
**Difficulty: Medium**

Write a program that counts both vowels and consonants in a user-entered text.
Ignore spaces and other characters.

**Sample Run:**
```
Enter text: Hello World!
Vowels: 3
Consonants: 7
```

**Starter Code:**
```python
# Get text from user
text = input("Enter text: ")

# Initialize counters
vowel_count = 0
consonant_count = 0

# Define vowels
vowels = "aeiouAEIOU"

# Loop through each character
for char in text:
    # TODO: Check if character is a letter using char.isalpha()
    if char.isalpha():
        # TODO: Check if it's a vowel (if char in vowels)
        if ___________:
            vowel_count += 1
        else:
            # TODO: It's a consonant
            ___________

# Print results
print("Vowels:", vowel_count)
print("Consonants:", consonant_count)
```

---

## Task 4: Powers Table 
**Difficulty: Medium**

Create a formatted table showing powers of 2 from 2⁰ to 2¹⁰.

**Expected Output:**
```
Exponent    Value
--------    -----
   0            1
   1            2
   2            4
   3            8
   4           16
   5           32
   6           64
   7          128
   8          256
   9          512
  10         1024
```

**Starter Code:**
```python
# Print header
print("Exponent    Value")
print("--------    -----")

# Loop through exponents 0 to 10
for exponent in range(___):
    value = 2 ** exponent
    # TODO: Print with format string "%4d %8d"
    print("__________" % (exponent, value))
```

---

## Task 5: Price List Formatter 
**Difficulty: Medium**

Write a program that displays a formatted price list.

Ask the user for 3 items and 3 prices, then display them in a table with tax calculated at 6%.

**Sample Run:**
```
Enter item 1: Pen
Enter price 1: 1.50
Enter item 2: Notebook
Enter price 2: 3.25
Enter item 3: Eraser
Enter price 3: 0.75

Item          Price    Tax
------------ -------- --------
Pen          $   1.50 $   0.09
Notebook     $   3.25 $   0.20
Eraser       $   0.75 $   0.05
```

**Starter Code:**
```python
# Initialize lists
items = []
prices = []

# Collect 3 items and prices
for i in range(1, 4):
    item = input("Enter item %d: " % i)
    price = float(input("Enter price %d: " % i))
    items.append(item)
    prices.append(price)

# Print header
print("\nItem          Price    Tax")
print("------------ -------- --------")

# Print each item with price and tax
for i in range(3):
    tax = prices[i] * 0.06
    # TODO: Use format "%-12s $%7.2f $%7.2f"
    print("__________" % (items[i], prices[i], tax))
```

---

## Task 6: Reverse String Builder 
**Difficulty: Medium**

Create a program that reverses a string using a for loop.

**Sample Run:**
```
Enter a word: Python
nohtyP
```

**Starter Code:**
```python
# Get word from user
word = input("Enter a word: ")

# Start with empty string
reversed_word = ""

# Loop through each character
for char in word:
    # TODO: Add character to FRONT of reversed_word
    reversed_word = ___________

# Print result
print(reversed_word)
```

---

## Task 7: Character Frequency 
**Difficulty: Hard**

Write a program that counts the frequency of each unique character in a text (ignoring spaces).

**Sample Run:**
```
Enter text: hello world
Character frequencies:
h: 1
e: 1
l: 3
o: 2
w: 1
r: 1
d: 1
```

**Starter Code:**
```python
# Get text from user
text = input("Enter text: ")

# Keep track of characters we've counted
counted_chars = ""

print("Character frequencies:")

# Loop through each character in text
for char in text:
    # Skip spaces
    if char == " ":
        continue
    
    # Skip if we've already counted this character
    if char in counted_chars:
        continue
    
    # Count how many times this character appears
    count = 0
    for c in text:
        if c == char:
            count += 1
    
    # Print the frequency
    print("%s: %d" % (char, count))
    
    # Remember we've counted this character
    counted_chars += char
```

**This one is complete! Study it to understand how it works.**

---

## Task 8: Report Card Generator 
**Difficulty: Hard**

Create a program that generates a formatted report card.

Ask for:
- Student name
- 5 subject names
- 5 grades (out of 100)

Display a formatted report with:
- Each subject and grade
- Average grade
- Letter grade (A: 90+, B: 80+, C: 70+, D: 60+, F: below 60)

**Sample Run:**
```
Student name: Alex Smith

Enter subject 1: Math
Enter grade 1: 95
Enter subject 2: Science
Enter grade 2: 88
Enter subject 3: English
Enter grade 3: 92
Enter subject 4: History
Enter grade 4: 85
Enter subject 5: PE
Enter grade 5: 90

REPORT CARD
==================================
Student: Alex Smith

Subject             Grade
-----------------  -------
Math                  95
Science               88
English               92
History               85
PE                    90
-----------------  -------
Average:              90.0
Letter Grade: A
```

**Starter Code:**
```python
# Get student name
student_name = input("Student name: ")
print()

# Initialize lists
subjects = []
grades = []

# Collect 5 subjects and grades
for i in range(1, 6):
    subject = input("Enter subject %d: " % i)
    grade = int(input("Enter grade %d: " % i))
    subjects.append(subject)
    grades.append(grade)

# Print report header
print("\nREPORT CARD")
print("=" * 34)
print("Student:", student_name)
print()
print("%-18s %7s" % ("Subject", "Grade"))
print("-" * 34)

# Print each subject and grade
for i in range(5):
    # TODO: Print subject and grade using "%-18s %7d"
    print("__________" % (subjects[i], grades[i]))

print("-" * 34)

# Calculate average
total = 0
for grade in grades:
    total += grade
average = total / len(grades)

# Print average
print("%-18s %7.1f" % ("Average:", average))

# Determine letter grade
# TODO: Use if-elif statements to determine letter grade
if average >= 90:
    letter = "A"
elif ___________:
    letter = "B"
elif ___________:
    letter = "C"
elif ___________:
    letter = "D"
else:
    letter = "F"

print("Letter Grade:", letter)
print("=" * 34)
```

---

## Task 9: Caesar Cipher Encoder
**Difficulty: Hard**

Write a program that encodes text using a simple Caesar cipher (shift each letter by a certain amount).

**Sample Run:**
```
Enter text: HELLO
Enter shift amount: 3
Encoded text: KHOOR
```

**Requirements:**
- Only shift letters (A-Z, a-z)
- Keep other characters unchanged
- Handle wrap-around (Z+1 = A)

**Starter Code:**
```python
# Get input
text = input("Enter text: ")
shift = int(input("Enter shift amount: "))

# Build encoded text
encoded = ""

for char in text:
    if char.isupper():
        # Handle uppercase letters (A-Z)
        # Get position (A=0, B=1, etc.)
        pos = ord(char) - ord('A')
        # Shift and wrap around using modulo
        new_pos = (pos + shift) % 26
        # Convert back to character
        new_char = chr(new_pos + ord('A'))
        encoded += new_char
    
    elif char.islower():
        # TODO: Handle lowercase letters (a-z)
        # Similar to uppercase but use ord('a')
        pos = ord(char) - ord('a')
        new_pos = ___________
        new_char = chr(new_pos + ord('a'))
        encoded += new_char
    
    else:
        # Keep non-letters unchanged
        encoded += char

print("Encoded text:", encoded)
```

---

## Challenge Task: Paycheck Formatter
**Difficulty: Challenge**

Create a paycheck stub generator that:
1. Asks for employee name
2. Asks for hours worked
3. Asks for hourly rate
4. Calculates gross pay (with overtime at 1.5x after 40 hours)
5. Calculates deductions:
   - Tax: 20% of gross
   - Insurance: $50
   - Retirement: 5% of gross
6. Displays formatted paycheck stub

**Sample Run:**
```
Employee name: Jane Doe
Hours worked: 45
Hourly rate: 20.00

================================
PAYCHECK STUB
================================
Employee: Jane Doe

Regular hours:    40.0 @ $20.00 = $  800.00
Overtime hours:    5.0 @ $30.00 = $  150.00
                                   ---------
Gross Pay:                         $  950.00

Deductions:
  Federal Tax (20%):               $  190.00
  Insurance:                       $   50.00
  Retirement (5%):                 $   47.50
                                   ---------
Total Deductions:                  $  287.50

NET PAY:                           $  662.50
================================
```

**Starter Code:**
```python
# Get input
name = input("Employee name: ")
hours = float(input("Hours worked: "))
rate = float(input("Hourly rate: "))

# Calculate regular and overtime hours
if hours <= 40:
    regular_hours = hours
    overtime_hours = 0
else:
    regular_hours = 40
    overtime_hours = hours - 40

# Calculate pay
regular_pay = regular_hours * rate
overtime_pay = overtime_hours * (rate * 1.5)
gross_pay = regular_pay + overtime_pay

# Calculate deductions
tax = gross_pay * 0.20
insurance = 50.00
retirement = gross_pay * 0.05
total_deductions = tax + insurance + retirement

# Calculate net pay
net_pay = gross_pay - total_deductions

# Print paycheck stub
print("\n" + "=" * 32)
print("PAYCHECK STUB")
print("=" * 32)
print("Employee:", name)
print()

# TODO: Print regular hours line using format below
# "Regular hours:  %6.1f @ $%.2f = $%9.2f"
print("__________" % (regular_hours, rate, regular_pay))

# TODO: Print overtime hours line (if any)
if overtime_hours > 0:
    print("__________" % (overtime_hours, rate * 1.5, overtime_pay))

print(" " * 35 + "---------")
# TODO: Print gross pay using "Gross Pay:" and format
print("%-35s $%9.2f" % ("Gross Pay:", gross_pay))

print()
print("Deductions:")
# TODO: Print each deduction with proper formatting
print("  %-31s $%9.2f" % ("Federal Tax (20%):", tax))
print("__________" % ("Insurance:", insurance))
print("__________" % ("Retirement (5%):", retirement))

print(" " * 35 + "---------")
print("%-35s $%9.2f" % ("Total Deductions:", total_deductions))
print()
# TODO: Print net pay
print("%-35s $%9.2f" % ("NET PAY:", net_pay))
print("=" * 32)
```

---

## Bonus Challenge: Text Statistics 🌟🌟
**Difficulty: Very Hard**

Create a comprehensive text analyzer that shows:
- Total characters (including spaces)
- Total characters (excluding spaces)
- Total words
- Total sentences (count periods, question marks, exclamation marks)
- Average word length
- Longest word
- Most common character (excluding spaces)

Display results in a nicely formatted report.

**Sample Run:**
```
Enter text: The quick brown fox jumps over the lazy dog!

TEXT ANALYSIS REPORT
========================================
Total characters (with spaces):     44
Total characters (no spaces):       35
Total words:                         9
Total sentences:                     1
Average word length:              3.9 letters
Longest word:                     quick

Most common character: o (appears 4 times)
========================================
```

**Starter Code:**
```python
# Get text
text = input("Enter text: ")

# Count characters with spaces
total_with_spaces = len(text)

# Count characters without spaces
total_no_spaces = 0
for char in text:
    if char != " ":
        total_no_spaces += 1

# Count words (split by spaces)
words = text.split()
word_count = len(words)

# Count sentences
sentence_count = 0
for char in text:
    if char in ".!?":
        sentence_count += 1

# Calculate average word length
total_word_length = 0
for word in words:
    # Count only letters in each word
    letter_count = 0
    for char in word:
        if char.isalpha():
            letter_count += 1
    total_word_length += letter_count

if word_count > 0:
    avg_word_length = total_word_length / word_count
else:
    avg_word_length = 0

# Find longest word
longest = ""
for word in words:
    # Remove punctuation from word
    clean_word = ""
    for char in word:
        if char.isalpha():
            clean_word += char
    
    if len(clean_word) > len(longest):
        longest = clean_word

# Find most common character (excluding spaces)
# TODO: Similar to Task 7, find character with highest count
most_common_char = ""
most_common_count = 0

# Your code here to find most common character
# Hint: Loop through unique characters and count each

# Print report
print("\nTEXT ANALYSIS REPORT")
print("=" * 40)
print("%-35s %5d" % ("Total characters (with spaces):", total_with_spaces))
print("%-35s %5d" % ("Total characters (no spaces):", total_no_spaces))
print("%-35s %5d" % ("Total words:", word_count))
print("%-35s %5d" % ("Total sentences:", sentence_count))
print("%-35s %5.1f letters" % ("Average word length:", avg_word_length))
print("%-35s %s" % ("Longest word:", longest))
print()
print("Most common character: %s (appears %d times)" % (most_common_char, most_common_count))
print("=" * 40)
```

---

## Submission Guidelines

- [ ] Test all programs with different inputs
- [ ] Check that formatting aligns properly
- [ ] Verify calculations are correct
- [ ] Use meaningful variable names
- [ ] Add comments explaining complex sections
- [ ] Save each task as a separate .py file

## Common Formatting Mistakes to Avoid

1. **Forgetting the `%` operator**: 
   - ❌ `"Value: %d" (number)` 
   - ✓ `"Value: %d" % (number)`

2. **Wrong number of values**: 
   - ❌ `"%d %d" % (5)` 
   - ✓ `"%d %d" % (5, 6)`

3. **Type mismatch**: 
   - ❌ `"%d" % 3.14` (truncates to 3)
   - ✓ `"%f" % 3.14` or `"%.2f" % 3.14`

4. **Negative sign placement**: 
   - ❌ `"%5-d"` 
   - ✓ `"%-5d"`

5. **Forgetting parentheses for multiple values**:
   - ❌ `"%s %d" % "Hi", 5`
   - ✓ `"%s %d" % ("Hi", 5)`