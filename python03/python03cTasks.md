# Lesson 3c Tasks: String Traversal and More Practice

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

**Hints:**
- Use a for loop to iterate through the string
- Print each character

---

## Task 2: Letter Counter 
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

**Pseudocode:**
```python
SET vowels = 0
SET consonants = 0

INPUT text

FOR each character IN text:
    IF character is a letter THEN (use char.isalpha)
        CONVERT character to lowercase
        IF character is in "aeiou" THEN
            ADD 1 to vowels
        ELSE
            ADD 1 to consonants
        ENDIF
    ENDIF
ENDFOR

DISPLAY "Vowels:", vowels
DISPLAY "Consonants:", consonants
```

---

## Task 4: Price List Formatter 
**Difficulty: Medium**

Write a program that asks the user for 3 items and their prices, then displays each item’s price and tax (at 6%).

## Hints
1. Ask the user to enter the **name** of 3 items.  
2. Ask for the **price** of each item.  
3. Calculate the **tax** for each item (`price * 0.06`).  
4. Display each item’s name, price, and tax using normal print statements.  
5. Store the user’s answers in separate variables like `item1`, `price1`, etc.  
6. Use `float()` when asking for prices so you can do math with them.  
7. Use `round(value, 2)` to limit your decimals to 2 places.  

- Example of displaying a result:
  ```python
  print(item1, "costs $", round(price1, 2), "with tax $", round(tax1, 2))
**Sample Run:**
```
Enter item 1: Pen
Enter price 1: 1.50
Enter item 2: Notebook
Enter price 2: 3.25
Enter item 3: Eraser
Enter price 3: 0.75

Pen costs $ 1.5 with tax $ 0.09
Notebook costs $ 3.25 with tax $ 0.19
Eraser costs $ 0.75 with tax $ 0.05

```

---

## Task 5: Reverse String Builder 
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

## Task 6: Report Card Generator 
**Difficulty: Hard**

Write a program that generates a simple **report card** for a student.

## Hints
1. Ask the user for the **student’s name**.  
2. Ask for **5 subject names**.  
3. Ask for **5 grades** (out of 100).  
4. After all grades are entered, display:  
   - Each subject and its grade  
   - The **average grade**  
   - The **letter grade**, based on:  
     - A: 90+  
     - B: 80–89  
     - C: 70–79  
     - D: 60–69  
     - F: below 60  
     
5. Use two lists:  
  ```python
  subjects = []
  grades = []
```

6. Use a loop to collect the 5 subjects and grades.
7. Use sum(grades) / len(grades) to find the average.
8. Use if-elif statements to assign the letter grade.
9. When printing, you can keep it simple:

```python
print(subjects[i], "grade is", grades[i])
```
**Example Output**
 ```python
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
Student: Alex Smith

Math grade is 95
Science grade is 88
English grade is 92
History grade is 85
PE grade is 90

Average grade: 90.0
Letter grade: A

 ```

---

## Submission Guidelines

- [ ] Test all programs with different inputs
- [ ] Check that formatting aligns properly
- [ ] Verify calculations are correct
- [ ] Use meaningful variable names
- [ ] Add comments explaining complex sections
- [ ] Save each task as a separate .py file
- [ ] Submit to your GitHub Rep just like previous assignments
