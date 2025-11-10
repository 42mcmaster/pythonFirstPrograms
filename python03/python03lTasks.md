# Lesson 3l Tasks: Built-in Modules and Tools

## Setup
Practice using Python's built-in modules to solve real problems!

---

## Task 1: Math Operations Menu
**Difficulty: Easy**

Create a calculator menu that uses the math module:
```
1. Square root
2. Power
3. Circle area
4. Quit
```

For circle area, use `math.pi` and the formula: π × r²

**Expected Run:**
```
1. Square root
2. Power
3. Circle area
4. Quit
Choice: 1
Number: 25
Result: 5.0

Choice: 3
Radius: 7
Area: 153.94
```

**Hints:**
- Import math
- Use math.sqrt(), math.pow(), math.pi
- Format output to 2 decimal places

---

## Task 2: Age Calculator
**Difficulty: Medium**

Write a program that calculates someone's exact age in years and days.

**Expected Run:**
```
Birth Year: 2000
Birth Month: 6
Birth Day: 15

You are 25 years old
You have lived for 9147 days
```

**Hints:**
- Import datetime
- Use datetime.date(year, month, day)
- Subtract dates to get difference
- Use .days to get total days

---

## Task 3: File Explorer
**Difficulty: Medium**

Create a program that:
- Lists all files in current directory
- Shows file sizes in bytes
- Indicates if each item is a file or directory

**Expected Output:**
```
=== FILE EXPLORER ===

data.txt (482 bytes) [FILE]
images (DIR)
script.py (1024 bytes) [FILE]
notes.txt (256 bytes) [FILE]

Total: 4 items
```

**Hints:**
- Import os and os.path
- Use os.listdir() to get files
- Use os.path.getsize() for size
- Use os.path.isfile() and os.path.isdir()

---

## Task 4: Log System
**Difficulty: Medium**

Create a simple logging system that saves events with timestamps:
- Ask user for log message
- Save to `app.log` with current date/time
- Display all previous logs

**Expected Run:**
```
=== LOGGING SYSTEM ===
1. Add log entry
2. View log
3. Quit

Choice: 1
Message: User logged in
Saved!

Choice: 2
--- Log File ---
2025-11-09 14:30:25 - User logged in
2025-11-09 14:31:10 - Data updated
---------------
```

**Hints:**
- Import datetime
- Use datetime.datetime.now()
- Use .strftime() to format
- Append to file with "a" mode

---

## Task 5: Geometry Calculator
**Difficulty: Medium**

Create a comprehensive geometry calculator using math module:

```
=== GEOMETRY CALCULATOR ===
1. Circle (area and circumference)
2. Square (area and perimeter)  
3. Triangle (area using Heron's formula)
4. Quit
```

For triangle, use Heron's formula:
- s = (a + b + c) / 2
- area = √(s(s-a)(s-b)(s-c))

**Expected Run:**
```
Choice: 1
Radius: 5
Area: 78.54
Circumference: 31.42

Choice: 3
Side a: 3
Side b: 4
Side c: 5
Area: 6.00
```

**Hints:**
- Import math
- Use math.pi for circle
- Use math.sqrt() for triangle
- Calculate each formula correctly

---

## Testing Checklist

- [ ] Verify math calculations are accurate
- [ ] Check that dates display correctly
- [ ] Ensure file operations work in your directory
- [ ] Test with different inputs
- [ ] Verify logs are saved with proper timestamps
