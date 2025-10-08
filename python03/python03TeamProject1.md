# Chapter 3 Team Project: Paired Programs

## Overview
Work with **one partner** to create **two related Python programs** that demonstrate your mastery of conditional statements and loops. Both programs should work together as a connected system.

## Project Timeline
- **Day 1**: Choose theme, plan features, create pseudocode
- **Day 2-3**: Code Program 1 (easier program)
- **Day 4-5**: Code Program 2 (more complex program)
- **Day 6**: Testing, documentation, presentation prep
- **Day 7**: Present to class

## Team Requirements
- [ ] Teams of exactly 2 students
- [ ] Both partners contribute to both programs
- [ ] Document who worked on what in comments
- [ ] Create a shared GitHub repo for the project
- [ ] Each program should be in a separate `.py` file

## Technical Requirements (MUST USE)

### Required in BOTH Programs:
- [ ] At least one `for` loop with `range()`
- [ ] At least one `if-elif-else` structure
- [ ] User input with `input()`
- [ ] Formatted output (tables, aligned text, or reports)
- [ ] At least one accumulator pattern
- [ ] Comments explaining complex sections

### Required in AT LEAST ONE Program:
- [ ] Logical operators (`and`, `or`, `not`)
- [ ] A loop that counts up or down by a step value
- [ ] String traversal (looping through characters)
- [ ] Nested conditionals (if inside if)
- [ ] Lists to store data

## Program Complexity

**Program 1 (Foundation Program)**: 
- 40-60 lines of code
- Focuses on data collection and basic processing
- Input-focused with simple validation

**Program 2 (Advanced Program)**:
- 60-100 lines of code  
- Processes data from Program 1 or generates complex output
- Must include formatted tables or detailed reports

---

## Theme Options

Choose ONE theme for your team. Both programs must fit your chosen theme.

---

## Theme 1: Grade Management System 📚

### Program 1: Grade Entry System
**Purpose**: Collect and validate student grades

**Features Required**:
- Ask how many students to enter
- For each student, collect:
  - Name
  - Number of assignments (3-5)
  - Grade for each assignment (0-100)
- Validate all grades are between 0-100
- Calculate and display each student's average
- Save summary to display (optional: write to file or just remember last run)

**Sample Output**:
```
=== GRADE ENTRY SYSTEM ===
How many students? 2

Student 1:
Name: Alice
How many assignments? 3
Assignment 1 grade: 95
Assignment 2 grade: 88
Assignment 3 grade: 92
Average: 91.7

Student 2:
Name: Bob
How many assignments? 3
Assignment 1 grade: 78
Assignment 2 grade: 85
Assignment 3 grade: 80
Average: 81.0

Data entry complete!
```

### Program 2: Class Statistics Report Generator
**Purpose**: Generate comprehensive statistics and formatted reports

**Features Required**:
- Ask for number of students and their grades
- Calculate:
  - Class average
  - Highest and lowest grades
  - Letter grade distribution (A, B, C, D, F counts)
  - Number of passing students (60+)
- Display formatted table with:
  - Student name
  - Average
  - Letter grade
- Show summary statistics

**Sample Output**:
```
=== CLASS STATISTICS REPORT ===

Student Name        Average    Letter
------------------  -------    ------
Alice                 91.7       A
Bob                   81.0       B
Charlie               76.5       C

==================================
CLASS SUMMARY
==================================
Class Average:              83.1
Highest Average:            91.7 (Alice)
Lowest Average:             76.5 (Charlie)

Grade Distribution:
  A grades: 1
  B grades: 1
  C grades: 1
  D grades: 0
  F grades: 0

Passing Rate: 100.0%
==================================
```

---

## Theme 2: Sports Team Manager ⚽

### Program 1: Game Score Tracker
**Purpose**: Track individual game results

**Features Required**:
- Ask for team name
- Ask how many games to enter
- For each game:
  - Opponent name
  - Your team's score
  - Opponent's score
  - Determine win/loss/tie
- Display game-by-game results
- Show running win-loss record

**Sample Output**:
```
=== GAME SCORE TRACKER ===
Enter team name: Eagles

How many games to enter? 3

Game 1:
Opponent: Hawks
Eagles score: 21
Hawks score: 14
Result: WIN

Current Record: 1-0-0

Game 2:
Opponent: Lions
Eagles score: 17
Hawks score: 17
Result: TIE

Current Record: 1-0-1

...
```

### Program 2: Season Statistics Report
**Purpose**: Generate season summary with player stats

**Features Required**:
- Ask for team name and number of games
- For each game collect scores (team and opponent)
- Ask for number of players
- For each player collect:
  - Name
  - Points scored this season
  - Games played
- Calculate:
  - Overall win-loss-tie record
  - Total points scored/allowed
  - Points per game average
  - Player statistics (points per game)
- Display formatted tables and rankings

**Sample Output**:
```
=== SEASON STATISTICS REPORT ===
Team: Eagles

SEASON SUMMARY
==================================
Games Played:               10
Record:                     7-2-1
Points Scored:              234
Points Allowed:             198
Points Per Game:           23.4
==================================

PLAYER STATISTICS
Player Name         Points    PPG
------------------  ------    ----
Mike Johnson          85      8.5
Sarah Lee             72      7.2
Tom Wilson            77      7.7

Top Scorer: Mike Johnson (85 points)
```

---

## Theme 3: Restaurant Order System 🍕

### Program 1: Menu Builder & Pricer
**Purpose**: Create menu and calculate individual orders

**Features Required**:
- Display restaurant menu (at least 6 items with prices)
- Ask how many items customer wants
- For each item:
  - Show menu with numbers
  - Let them pick by number
  - Ask for quantity
- Calculate:
  - Subtotal
  - Tax (7%)
  - Tip (ask for percentage or use default 15%)
  - Total
- Display itemized receipt with formatting

**Sample Output**:
```
=== JOE'S PIZZA - ORDER SYSTEM ===

MENU:
1. Cheese Pizza      $12.99
2. Pepperoni Pizza   $14.99
3. Salad             $ 6.99
4. Breadsticks       $ 4.99
5. Soda              $ 2.49
6. Dessert           $ 5.99

How many different items? 2

Item 1:
Enter item number: 2
Quantity: 2

Item 2:
Enter item number: 5
Quantity: 3

=== RECEIPT ===
2x Pepperoni Pizza  $29.98
3x Soda             $ 7.47
                    ------
Subtotal:           $37.45
Tax (7%):           $ 2.62
Tip (15%):          $ 5.62
                    ------
TOTAL:              $45.69
=================
```

### Program 2: Daily Sales Report Generator
**Purpose**: Analyze multiple orders and generate end-of-day report

**Features Required**:
- Ask how many orders were placed today
- For each order collect:
  - Number of items
  - Order total
- Track which menu items were most popular (ask user or simulate)
- Calculate:
  - Total revenue
  - Average order size
  - Number of orders in ranges (under $20, $20-40, over $40)
  - Busiest hour (optional - or just ask for time periods)
- Display formatted daily report

**Sample Output**:
```
=== DAILY SALES REPORT ===
Date: [Today's Date]

SALES SUMMARY
==================================
Total Orders:               45
Total Revenue:          $1,247.80
Average Order:            $27.73
Highest Order:            $67.45
Lowest Order:             $12.38
==================================

ORDER SIZE DISTRIBUTION
Under $20:       12 orders (26.7%)
$20-$40:         25 orders (55.6%)
Over $40:         8 orders (17.8%)

POPULAR ITEMS (by orders)
1. Pepperoni Pizza    23 orders
2. Soda               34 orders
3. Cheese Pizza       18 orders

BUSIEST TIME PERIOD
Lunch (11am-2pm):    28 orders
Dinner (5pm-8pm):    17 orders
==================================
```

---

## Theme 4: Fitness Challenge Tracker 💪

### Program 1: Daily Workout Logger
**Purpose**: Log daily workouts and calculate totals

**Features Required**:
- Ask for user name and fitness goal
- Ask how many days to log
- For each day:
  - Exercise type (run, bike, swim, weights, etc.)
  - Duration in minutes
  - Difficulty (1-5 scale)
- Calculate daily totals
- Determine if they met goals (30+ min = met daily goal)
- Show daily summaries

### Program 2: Weekly Fitness Report
**Purpose**: Analyze week of workouts with statistics

**Features Required**:
- Ask for 7 days of workout data (or fewer)
- Collect exercise type, duration, calories burned
- Calculate:
  - Total workout time
  - Average workout length
  - Most common exercise
  - Total calories burned
  - Days goal was met (30+ minutes)
  - Streak of consecutive days
- Display formatted weekly report with progress bar
- Give motivational message based on performance

---

## Theme 5: Movie/Game Collection Manager 🎮

### Program 1: Collection Entry System
**Purpose**: Add items to personal collection

**Features Required**:
- Choose collection type (movies or games)
- Ask how many items to add
- For each item collect:
  - Title
  - Genre
  - Rating (1-10 or G/PG/PG-13/R for movies)
  - Year
  - Owned or wishlist
- Display collection summary
- Count items by genre

### Program 2: Collection Statistics & Recommender
**Purpose**: Analyze collection and make recommendations

**Features Required**:
- Enter collection data (title, genre, rating, year)
- Calculate statistics:
  - Total items in collection
  - Average rating
  - Genre breakdown (count and percentage)
  - Oldest and newest items
  - Highest and lowest rated
- Find genre with most items
- Display formatted tables
- Make recommendations based on favorite genres

---

## Grading Rubric (100 points)

### Functionality (40 points)
- [ ] Both programs run without errors (10 pts)
- [ ] All required features work correctly (15 pts)
- [ ] User input is validated appropriately (8 pts)
- [ ] Programs produce correct output (7 pts)

### Code Quality (30 points)
- [ ] Uses all required Python concepts (10 pts)
- [ ] Code is organized and readable (8 pts)
- [ ] Meaningful variable names (5 pts)
- [ ] Includes helpful comments (7 pts)

### Design & Output (20 points)
- [ ] Output is formatted and easy to read (10 pts)
- [ ] User interface is clear and friendly (5 pts)
- [ ] Creativity and extra features (5 pts)

### Teamwork & Documentation (10 points)
- [ ] Both partners contributed (3 pts)
- [ ] GitHub repo is organized (3 pts)
- [ ] README file explains programs (4 pts)

## Deliverables

1. **GitHub Repository** containing:
   - `program1.py` (descriptive name)
   - `program2.py` (descriptive name)
   - `README.md` with:
     - Team member names
     - Theme chosen
     - Description of each program
     - How to run the programs
     - Features implemented
     - Who did what

2. **Brief Presentation** (5 minutes):
   - Demonstrate both programs
   - Explain one interesting technical challenge
   - Show formatted output
   - Answer questions

## Planning Template

Use this in your first planning session:

```
TEAM PROJECT PLANNING

Team Members:
1. _______________
2. _______________

Theme Chosen: _______________

Program 1: _______________
Main Purpose: _______________
Key Features:
- 
-
-

Program 2: _______________
Main Purpose: _______________
Key Features:
-
-
-

Division of Work:
Partner 1 Focus: _______________
Partner 2 Focus: _______________
Shared Responsibilities: _______________

Required Python Concepts Checklist:
[ ] For loops with range()
[ ] If-elif-else statements
[ ] Logical operators
[ ] Accumulator pattern
[ ] Formatted output
[ ] String traversal
[ ] Lists
[ ] Input validation
```

## Tips for Success

1. **Start Simple**: Get a basic version working first, then add features
2. **Test Often**: Run your program after every few lines
3. **Communicate**: Check in with your partner regularly
4. **Comment As You Go**: Don't wait until the end
5. **Handle Bad Input**: Use if statements to validate user input
6. **Format Output**: Tables and reports should be neat and aligned
7. **Ask for Help**: Use your teacher and classmates as resources

## Extra Credit Opportunities (+10 points max)

- [ ] Write data to a file and read it back (+5 pts)
- [ ] Create a third bonus program that uses both programs together (+5 pts)
- [ ] Add color to output using ANSI codes (+3 pts)
- [ ] Create ASCII art for your program interface (+2 pts)
- [ ] Add data visualization (simple text-based charts) (+5 pts)

---

Good luck! Remember: this project tests everything you've learned about loops, conditionals, and formatted output. Make it interesting, make it work, and most importantly—work together!