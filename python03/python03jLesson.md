# Lesson 3j: File Input and Output

## Learning Objectives
- Open and close files in Python
- Read data from text files
- Write data to text files
- Append data to existing files
- Use the `with` statement for safe file handling
- Check if files exist

## Why File I/O?

Programs often need to:
- Save data permanently (not just while program runs)
- Read data from files (config files, data files)
- Log information
- Process large datasets

**Key Difference:**
- Variables disappear when program ends
- Files persist on disk

## Opening and Closing Files

### The Basic Pattern

```python
# Open a file
file = open("data.txt", "r")  # "r" = read mode

# Do something with the file
content = file.read()

# Close the file (IMPORTANT!)
file.close()
```

**File Modes:**
- `"r"` - Read (default) - file must exist
- `"w"` - Write - creates new file or **overwrites** existing
- `"a"` - Append - adds to end of existing file
- `"r+"` - Read and write

## The `with` Statement (BEST PRACTICE)

**Problem:** If you forget `file.close()`, you can lose data!

**Solution:** Use `with` statement - automatically closes file

```python
with open("data.txt", "r") as file:
    content = file.read()
    print(content)
# File automatically closed here!
```

**Always use `with` when possible!**

## Reading from Files

### Method 1: Read Entire File

```python
with open("story.txt", "r") as file:
    content = file.read()
    print(content)
```

### Method 2: Read Line by Line

```python
with open("names.txt", "r") as file:
    for line in file:
        print(line.strip())  # .strip() removes \n
```

### Method 3: Read All Lines into a List

```python
with open("scores.txt", "r") as file:
    lines = file.readlines()
    
for line in lines:
    print(line.strip())
```

## Example 1: Reading a File

Suppose `grades.txt` contains:
```
85
92
78
95
88
```

**Program:**
```python
with open("grades.txt", "r") as file:
    total = 0
    count = 0
    
    for line in file:
        grade = int(line.strip())
        total += grade
        count += 1
    
    average = total / count
    print(f"Average grade: {average:.1f}")
```

**Output:**
```
Average grade: 87.6
```

## Writing to Files

### Creating a New File

```python
with open("output.txt", "w") as file:
    file.write("Hello, World!\n")
    file.write("This is a new file.\n")
```

**Warning:** `"w"` mode **overwrites** existing files!

### Writing Multiple Lines

```python
names = ["Alice", "Bob", "Charlie"]

with open("names.txt", "w") as file:
    for name in names:
        file.write(name + "\n")
```

## Example 2: Saving User Input

```python
print("Enter student names (type 'done' to finish):")

with open("students.txt", "w") as file:
    while True:
        name = input("Name: ")
        if name.lower() == "done":
            break
        file.write(name + "\n")

print("Names saved to students.txt")
```

## Appending to Files

Use `"a"` mode to add to existing files without erasing:

```python
with open("log.txt", "a") as file:
    file.write("New log entry\n")
```

## Example 3: High Score Tracker

```python
# Read existing high score
try:
    with open("highscore.txt", "r") as file:
        high_score = int(file.read())
except FileNotFoundError:
    high_score = 0

print(f"Current high score: {high_score}")

# Play game (simulate)
score = int(input("Enter your score: "))

# Update if new high score
if score > high_score:
    print("New high score!")
    with open("highscore.txt", "w") as file:
        file.write(str(score))
else:
    print("Try again!")
```

## Checking if File Exists

### Using os.path

```python
import os.path

if os.path.exists("data.txt"):
    print("File exists!")
else:
    print("File not found!")
```

### Using try/except (Better for File I/O)

```python
try:
    with open("data.txt", "r") as file:
        content = file.read()
except FileNotFoundError:
    print("File not found!")
```

## Complete Example: Todo List

```python
def show_menu():
    print("\n=== TODO LIST ===")
    print("1. View tasks")
    print("2. Add task")
    print("3. Quit")

def view_tasks():
    """Display all tasks from file."""
    try:
        with open("tasks.txt", "r") as file:
            tasks = file.readlines()
            if tasks:
                print("\nYour tasks:")
                for i, task in enumerate(tasks, 1):
                    print(f"{i}. {task.strip()}")
            else:
                print("No tasks yet!")
    except FileNotFoundError:
        print("No tasks yet!")

def add_task():
    """Add a new task to file."""
    task = input("Enter task: ")
    with open("tasks.txt", "a") as file:
        file.write(task + "\n")
    print("Task added!")

# Main program
while True:
    show_menu()
    choice = input("Choice: ")
    
    if choice == "1":
        view_tasks()
    elif choice == "2":
        add_task()
    elif choice == "3":
        print("Goodbye!")
        break
    else:
        print("Invalid choice!")
```

## File Paths

### Same Directory as Program
```python
with open("data.txt", "r") as file:
    # Looks in same folder as your .py file
```

### Absolute Path
```python
with open("C:/Users/Ryan/Desktop/data.txt", "r") as file:
    # Full path to file
```

### Relative Path
```python
with open("data/students.txt", "r") as file:
    # Looks in "data" subfolder
```

## Common File Errors

### FileNotFoundError
```python
# File doesn't exist in read mode
with open("missing.txt", "r") as file:  # ERROR!
    content = file.read()
```

**Fix:** Check if file exists first, or use try/except

### PermissionError
```python
# Can't write to file (maybe it's open elsewhere)
with open("locked.txt", "w") as file:  # ERROR!
    file.write("data")
```

**Fix:** Close file in other programs

## Working with CSV-like Data

```python
# Write scores with names
with open("scores.txt", "w") as file:
    file.write("Alice,85\n")
    file.write("Bob,92\n")
    file.write("Charlie,78\n")

# Read and parse
with open("scores.txt", "r") as file:
    for line in file:
        name, score = line.strip().split(",")
        print(f"{name}: {score}")
```

**Output:**
```
Alice: 85
Bob: 92
Charlie: 78
```

## Key Takeaways

1. **Use `with` statement** - automatically closes files
2. **`"r"`** = read, **`"w"`** = write (overwrites), **`"a"`** = append
3. **`.read()`** reads entire file, **`.readlines()`** reads into list
4. **`.write()`** writes string to file (add `\n` for newlines)
5. **`.strip()`** removes whitespace/newlines when reading
6. **Check file existence** with try/except or os.path.exists()
7. **Files persist** - unlike variables that disappear

## Important Reminders

- **Always close files** (use `with` to do it automatically)
- **`"w"` mode deletes existing content** - be careful!
- **Convert data types** - files only store strings
- **Add `\n`** when writing lines
- **Use `.strip()`** when reading lines

## Practice

Try this exercise:

```python
# Create a file with 5 numbers
with open("numbers.txt", "w") as file:
    for i in range(1, 6):
        file.write(str(i * 10) + "\n")

# Read and calculate sum
with open("numbers.txt", "r") as file:
    total = 0
    for line in file:
        total += int(line.strip())
    print(f"Sum: {total}")
```

Should output: `Sum: 150` (10+20+30+40+50)
