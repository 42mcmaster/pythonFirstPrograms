# Lesson 3j Tasks: File Input and Output

## Setup
Create a new Python file for each task. Test with different data!

---

## Task 1: Name Saver
**Difficulty: Easy**

Write a program that asks for 3 names and saves them to `names.txt`, then reads them back and displays them.

**Expected Flow:**
```
Enter name 1: Alice
Enter name 2: Bob
Enter name 3: Charlie

Saved to names.txt!

Reading names back:
1. Alice
2. Bob
3. Charlie
```

**Hints:**
- Use `with open("names.txt", "w")` to write
- Use `with open("names.txt", "r")` to read
- Don't forget `\n` when writing

---

## Task 2: Grade Calculator from File
**Difficulty: Easy**

Create a file called `grades.txt` with these grades (one per line):
```
85
92
78
95
88
```

Write a program that reads this file and calculates:
- Average grade
- Highest grade
- Lowest grade

**Expected Output:**
```
Average: 87.6
Highest: 95
Lowest: 78
```

**Hints:**
- Read line by line
- Convert strings to integers: `int(line.strip())`
- Use variables to track min/max

---

## Task 3: Daily Log
**Difficulty: Medium**

Create a simple journal program that:
- Asks for a log entry
- Saves it to `journal.txt` with a timestamp
- Appends (doesn't overwrite)
- Shows all previous entries

**Expected Run:**
```
=== DAILY LOG ===
1. Write entry
2. View all entries
3. Quit

Choice: 1
Entry: Had a great day at school!
Saved!

Choice: 2
--- Log Entries ---
Had a great day at school!
Learned about file I/O today.
---
```

**Hints:**
- Use `"a"` mode to append
- Keep entries short and simple
- Read entire file to display

---

## Task 4: Word Counter
**Difficulty: Medium**

Write a program that:
1. Reads a text file
2. Counts total words
3. Counts total lines
4. Finds the longest word

Create a file called `story.txt`:
```
The quick brown fox
jumps over the lazy dog
programming is fun
```

**Expected Output:**
```
File: story.txt
Lines: 3
Words: 11
Longest word: programming
```

**Hints:**
- Use `.split()` to get words from a line
- Track max length word as you read
- Count lines with a counter

---

## Task 5: High Score Keeper
**Difficulty: Medium**

Create a game score tracker that:
- Reads the current high score from `highscore.txt`
- If file doesn't exist, starts at 0
- Asks for new score
- Updates file if new score is higher
- Shows all-time high

**Sample Run 1 (first time):**
```
Current high score: 0
Enter your score: 150
NEW HIGH SCORE!
```

**Sample Run 2 (later):**
```
Current high score: 150
Enter your score: 200
NEW HIGH SCORE!
```

**Sample Run 3:**
```
Current high score: 200
Enter your score: 175
Not quite! Try again!
```

**Hints:**
- Use try/except for FileNotFoundError
- Read score as integer
- Write only if new score is higher
- Use `"w"` mode when updating

---

## Testing Checklist

- [ ] Test file creation - does the file actually appear?
- [ ] Test reading - does program read correctly?
- [ ] Test appending - does data get added without erasing?
- [ ] Test missing file - does program handle gracefully?
- [ ] Verify file contents manually (open in Notepad/TextEdit)
