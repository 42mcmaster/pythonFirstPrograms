# Lesson 3c Tasks: String Traversal and Formatting Practice

## Setup
Complete these tasks in IDLE or VS Code. Test with various inputs!

---

## Task 1: Character Printer ⭐
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

**Hints:**
- Use a for loop to iterate through the string
- Print each character

---

## Task 2: Letter Counter ⭐
**Difficulty: Easy**

Create a program that counts how many letters 'a' (lowercase) appear in a user-entered text.

**Sample Run:**
```
Enter some text: banana
The letter 'a' appears 3 times
```

**Hints:**
- Use a counter variable starting at 0
- Check if each character equals 'a'
- Increment the counter when found

---

## Task 3: Vowel and Consonant Counter ⭐⭐
**Difficulty: Medium**

Write a program that counts both vowels and consonants in a user-entered text.
Ignore spaces and other characters.

**Sample Run:**
```
Enter text: Hello World!
Vowels: 3
Consonants: 7
```

**Hints:**
- Keep two separate counters
- Check if character is in "aeiouAEIOU" for vowels
- Check if character.isalpha() for letters
- Consonants = letters that aren't vowels

---

## Task 4: Powers Table ⭐⭐
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

**Hints:**
- Use a for loop with range(11)
- Calculate 2**exponent for each value
- Use format string: `"%4d %8d"`
- Print header and separator first

---

## Task 5: Price List Formatter ⭐⭐
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

**Hints:**
- Store items in a list
- Store prices in a list
- Use format string: `"%-12s $%7.2f $%7.2f"`
- Calculate tax: `price * 0.06`

---

## Task 6: Reverse String Builder ⭐⭐
**Difficulty: Medium**

Create a program that reverses a string using a for loop.

**Sample Run:**
```
Enter a word: Python
nohtyP
```

**Hints:**
- Start with an empty string: `reversed_str = ""`
- Loop through the original string
- Add each character to the FRONT: `reversed_str = char + reversed_str`

---

## Task 7: Character Frequency ⭐⭐⭐
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

**Hints:**
- Keep track of characters you've already counted
- For each unique character, count how many times it appears
- Skip spaces
- Use nested loops or create a list of seen characters

---

## Task 8: Report Card Generator ⭐⭐⭐
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

(... continue for 5 subjects ...)

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

**Hints:**
- Use lists to store subjects and grades
- Calculate average after collecting all grades
- Use if-elif statements for letter grade
- Format with `"%-18s %7.0f"`

---

## Task 9: Caesar Cipher Encoder ⭐⭐⭐
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

**Hints:**
- Use `ord()` to get ASCII value: `ord('A')` = 65
- Use `chr()` to convert back: `chr(65)` = 'A'
- Shift formula: `new_value = ((old_value - 65 + shift) % 26) + 65`
- Handle uppercase and lowercase separately

---

## Challenge Task: Paycheck Formatter 🌟
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

**Hints:**
- Calculate overtime hours: `max(0, hours - 40)`
- Use format strings for alignment
- All money should show 2 decimal places
- Build it step by step - test each section

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

---

## Submission Guidelines

- [ ] Test all programs with different inputs
- [ ] Check that formatting aligns properly
- [ ] Verify calculations are correct
- [ ] Use meaningful variable names
- [ ] Add comments explaining complex sections
- [ ] Save each task as a separate .py file

## Common Formatting Mistakes to Avoid

1. Forgetting the `%` operator: `"Value: %d" (number)` ❌
2. Wrong number of values: `"%d %d" % (5)` ❌ Should be `% (5, 6)`
3. Type mismatch: `"%d" % 3.14` ❌ Use `%f` for floats
4. Negative width on wrong side: `%5-d` ❌ Should be `%-5d`