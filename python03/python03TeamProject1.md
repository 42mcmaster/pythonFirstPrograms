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
- [ ] At least one loop (`for` with `range()` OR `while`)
- [ ] At least one `if-elif-else` structure
- [ ] User input with `input()`
- [ ] Clear, organized output
- [ ] At least one accumulator pattern
- [ ] Comments explaining complex sections

### Required in AT LEAST ONE Program:
- [ ] A `while` loop (for input validation, menu systems, or repeated actions)
- [ ] A `for` loop with `range()` (for counting or iterating a specific number of times)
- [ ] Logical operators (`and`, `or`, `not`)
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
- Must include summary statistics or detailed reports

---

## Theme Options

Choose ONE theme for your team. Both programs must fit your chosen theme.

---

## Theme 1: Grade Management System 📚

### Program 1: Grade Entry System
**Purpose**: Collect and validate student grades

**Features Required**:
- Use a `while` loop to keep asking if user wants to enter another student
- For each student, collect:
  - Name
  - Number of assignments (3-5)
  - Grade for each assignment (0-100) using a `for` loop
- Validate all grades are between 0-100 (use `while` loop to re-prompt if invalid)
- Calculate and display each student's average
- Keep track of total students entered

**Sample Output**:
```
=== GRADE ENTRY SYSTEM ===

Student Name: Alice
How many assignments? 3
Assignment 1 grade: 95
Assignment 2 grade: 88
Assignment 3 grade: 92
Alice's Average: 91.7

Enter another student? (yes/no): yes

Student Name: Bob
How many assignments? 3
Assignment 1 grade: 78
Assignment 2 grade: 85
Assignment 3 grade: 80
Bob's Average: 81.0

Enter another student? (yes/no): no

Total students entered: 2
Data entry complete!
```

### Program 2: Class Statistics Report Generator
**Purpose**: Generate comprehensive statistics

**Features Required**:
- Ask for number of students
- Use `for` loop to collect student names and their averages
- Calculate:
  - Class average
  - Highest and lowest grades
  - Letter grade distribution (A, B, C, D, F counts)
  - Number of passing students (60+)
- Display summary with clear labels

**Sample Output**:
```
=== CLASS STATISTICS REPORT ===

Enter number of students: 3

Student 1:
Name: Alice
Average: 91.7
Letter Grade: A

Student 2:
Name: Bob
Average: 81.0
Letter Grade: B

Student 3:
Name: Charlie
Average: 76.5
Letter Grade: C

CLASS SUMMARY
Class Average: 83.1
Highest Average: 91.7 (Alice)
Lowest Average: 76.5 (Charlie)

Grade Distribution:
A grades: 1
B grades: 1
C grades: 1
D grades: 0
F grades: 0

Passing Rate: 100.0%
```

---

## Theme 2: Sports Team Manager ⚽

### Program 1: Game Score Tracker
**Purpose**: Track individual game results

**Features Required**:
- Ask for team name
- Use `while` loop to keep entering games until user is done
- For each game:
  - Opponent name
  - Your team's score
  - Opponent's score
  - Determine win/loss/tie
- Display game-by-game results
- Show running win-loss record after each game

**Sample Output**:
```
=== GAME SCORE TRACKER ===
Enter team name: Eagles

Game 1
Opponent: Hawks
Eagles score: 21
Hawks score: 14
Result: WIN
Current Record: 1-0-0

Enter another game? (yes/no): yes

Game 2
Opponent: Lions
Eagles score: 17
Lions score: 17
Result: TIE
Current Record: 1-0-1

Enter another game? (yes/no): no

Final Record: 1-0-1
```

### Program 2: Season Statistics Report
**Purpose**: Generate season summary with player stats

**Features Required**:
- Ask for team name and number of games
- Use `for` loop to collect scores for each game
- Ask for number of players
- Use `for` loop to collect player data:
  - Name
  - Points scored this season
  - Games played
- Calculate:
  - Overall win-loss-tie record
  - Total points scored/allowed
  - Points per game average
  - Player statistics (points per game)

**Sample Output**:
```
=== SEASON STATISTICS REPORT ===
Team: Eagles

SEASON SUMMARY
Games Played: 10
Record: 7-2-1
Points Scored: 234
Points Allowed: 198
Points Per Game: 23.4

PLAYER STATISTICS
Mike Johnson - 85 points (8.5 PPG)
Sarah Lee - 72 points (7.2 PPG)
Tom Wilson - 77 points (7.7 PPG)

Top Scorer: Mike Johnson (85 points)
```

---

## Theme 3: Restaurant Order System 🍕

### Program 1: Menu Builder & Pricer
**Purpose**: Create menu and calculate individual orders

**Features Required**:
- Display restaurant menu (at least 6 items with prices)
- Use `while` loop to let customers keep adding items until done
- For each item:
  - Show menu
  - Let them pick by number
  - Ask for quantity
  - Validate input (use `while` loop for bad inputs)
- Calculate:
  - Subtotal
  - Tax (7%)
  - Tip (ask for percentage or use default 15%)
  - Total
- Display itemized receipt

**Sample Output**:
```
=== JOE'S PIZZA - ORDER SYSTEM ===

MENU:
1. Cheese Pizza - $12.99
2. Pepperoni Pizza - $14.99
3. Salad - $6.99
4. Breadsticks - $4.99
5. Soda - $2.49
6. Dessert - $5.99

Enter item number (or 0 to finish): 2
Quantity: 2
Added: 2x Pepperoni Pizza

Enter item number (or 0 to finish): 5
Quantity: 3
Added: 3x Soda

Enter item number (or 0 to finish): 0

RECEIPT
2x Pepperoni Pizza - $29.98
3x Soda - $7.47
Subtotal: $37.45
Tax (7%): $2.62
Tip (15%): $5.62
TOTAL: $45.69
```

### Program 2: Daily Sales Report Generator
**Purpose**: Analyze multiple orders and generate end-of-day report

**Features Required**:
- Ask how many orders were placed today
- Use `for` loop to collect order totals
- Track which menu items were most popular
- Calculate:
  - Total revenue
  - Average order size
  - Number of orders in ranges (under $20, $20-40, over $40)
  - Highest and lowest order

**Sample Output**:
```
=== DAILY SALES REPORT ===

SALES SUMMARY
Total Orders: 45
Total Revenue: $1,247.80
Average Order: $27.73
Highest Order: $67.45
Lowest Order: $12.38

ORDER SIZE DISTRIBUTION
Under $20: 12 orders (26.7%)
$20-$40: 25 orders (55.6%)
Over $40: 8 orders (17.8%)

POPULAR ITEMS
1. Pepperoni Pizza - 23 orders
2. Soda - 34 orders
3. Cheese Pizza - 18 orders
```

---

## Theme 4: Fitness Challenge Tracker 💪

### Program 1: Daily Workout Logger
**Purpose**: Log daily workouts and calculate totals

**Features Required**:
- Ask for user name and fitness goal
- Use `while` loop to keep logging workouts until user is done
- For each workout:
  - Exercise type (run, bike, swim, weights, etc.)
  - Duration in minutes
  - Difficulty (1-5 scale)
- Calculate daily totals
- Determine if they met goals (30+ min = met daily goal)


**Sample Output**:
```
=== DAILY WORKOUT LOGGER ===

Welcome! What's your name? Sarah
What's your daily fitness goal (minutes)? 30

Workout 1
Exercise type: run
Duration (minutes): 25
Difficulty (1-5): 3
Logged: 25 minutes of run

Log another workout? (yes/no): yes

Workout 2
Exercise type: weights
Duration (minutes): 20
Difficulty (1-5): 4
Logged: 20 minutes of weights

Log another workout? (yes/no): no

DAILY SUMMARY
Total workouts: 2
Total time: 45 minutes
Average difficulty: 3.5
Daily goal (30 min): ACHIEVED!
Great job, Sarah!
```

### Program 2: Weekly Fitness Report
**Purpose**: Analyze week of workouts with statistics

**Features Required**:
- Ask how many days to analyze
- Use `for` loop to collect workout data for each day
- Collect exercise type, duration, calories burned
- Calculate:
  - Total workout time
  - Average workout length
  - Most common exercise
  - Total calories burned
  - Days goal was met (30+ minutes)
  - Streak of consecutive days
- Give motivational message based on performance

**Sample Output**:
```
=== WEEKLY FITNESS REPORT ===

How many days to analyze? 5

Day 1
Exercise type: run
Duration (minutes): 30
Calories burned: 250

Day 2
Exercise type: bike
Duration (minutes): 45
Calories burned: 320

Day 3
Exercise type: run
Duration (minutes): 25
Calories burned: 200

Day 4
Exercise type: weights
Duration (minutes): 35
Calories burned: 180

Day 5
Exercise type: run
Duration (minutes): 40
Calories burned: 310

WEEKLY SUMMARY
Total workout time: 175 minutes
Average workout: 35 minutes
Total calories burned: 1,260
Days goal met (30+ min): 4 out of 5 (80%)
Longest streak: 4 consecutive days

Most common exercise: run (3 times)

PERFORMANCE REVIEW
Excellent work! You're staying consistent with your fitness routine.
Your running is really strong - consider varying your workouts more.
Keep up the great work!

```

---

## Theme 5: Movie/Game Collection Manager 🎮

### Program 1: Collection Entry System
**Purpose**: Add items to personal collection

**Features Required**:
- Choose collection type (movies or games)
- Use `while` loop to keep adding items until done
- For each item collect:
  - Title
  - Genre
  - Rating (1-10 or G/PG/PG-13/R for movies)
  - Year
  - Owned or wishlist
- Display collection summary
- Count items by genre


**Sample Output**:
```
=== COLLECTION ENTRY SYSTEM ===

Collection type (movies/games): games

Item 1
Title: The Legend of Zelda
Genre: Adventure
Rating (1-10): 10
Year: 2017
Status (owned/wishlist): owned
Added to collection!

Add another item? (yes/no): yes

Item 2
Title: Minecraft
Genre: Sandbox
Rating (1-10): 9
Year: 2011
Status (owned/wishlist): owned
Added to collection!

Add another item? (yes/no): yes

Item 3
Title: Elden Ring
Genre: Adventure
Rating (1-10): 9
Year: 2022
Status (owned/wishlist): wishlist
Added to collection!

Add another item? (yes/no): no

COLLECTION SUMMARY
Total items: 3
Owned: 2
Wishlist: 1

Items by Genre:
Adventure: 2
Sandbox: 1

Collection saved!
```

### Program 2: Collection Statistics & Recommender
**Purpose**: Analyze collection and make recommendations

**Features Required**:
- Ask how many items to analyze
- Use `for` loop to enter collection data (title, genre, rating, year)
- Calculate statistics:
  - Total items in collection
  - Average rating
  - Genre breakdown (count and percentage)
  - Oldest and newest items
  - Highest and lowest rated
- Find genre with most items
- Make recommendations based on favorite genres

**Sample Output**:
```
=== COLLECTION STATISTICS & RECOMMENDER ===

How many items to analyze? 5

Item 1
Title: The Legend of Zelda
Genre: Adventure
Rating (1-10): 10
Year: 2017

Item 2
Title: Minecraft
Genre: Sandbox
Rating (1-10): 9
Year: 2011

Item 3
Title: Elden Ring
Genre: Adventure
Rating (1-10): 9
Year: 2022

Item 4
Title: Mario Kart 8
Genre: Racing
Rating (1-10): 8
Year: 2014

Item 5
Title: Dark Souls 3
Genre: Adventure
Rating (1-10): 9
Year: 2016

COLLECTION STATISTICS
Total items: 5
Average rating: 9.0

Genre Breakdown:
Adventure: 3 items (60%)
Sandbox: 1 item (20%)
Racing: 1 item (20%)

Collection Highlights:
Oldest: Minecraft (2011)
Newest: Elden Ring (2022)
Highest rated: The Legend of Zelda (10/10)
Lowest rated: Mario Kart 8 (8/10)

RECOMMENDATIONS
Your favorite genre is Adventure!
Based on your collection, you might enjoy:
- More adventure games like Breath of the Wild or Skyrim
- Try RPG games since you enjoy story-driven adventures
- You rated everything highly - you have great taste!
```

---

## Grading Rubric (40 points)

### Functionality (15 points)
- [ ] Both programs run without errors 
- [ ] All required features work correctly 
- [ ] User input is validated appropriately 
- [ ] Programs produce correct output 

### Code Quality (10 points)
- [ ] Uses all required Python concepts 
- [ ] Code is organized and readable 
- [ ] Meaningful variable names 
- [ ] Includes helpful comments 

### Design & Output (10 points)
- [ ] Output is clear and organized
- [ ] User interface is intuitive 
- [ ] Creativity and extra features 

### Teamwork & Documentation (5 points)
- [ ] Both partners contributed 
- [ ] GitHub repo is organized 
- [ ] README file explains programs 

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
   - Show how your programs work together
   - Answer questions

## Planning Template

Use this checklist in your first planning session:

```
Required Python Concepts Checklist:
[ ] For loops with range()
[ ] While loops
[ ] If-elif-else statements
[ ] Logical operators
[ ] Accumulator pattern
[ ] Input validation
[ ] String traversal
[ ] Lists
```

## Tips for Success

1. **Start Simple**: Get a basic version working first, then add features
2. **Test Often**: Run your program after every few lines
3. **Use While Loops Wisely**: Great for menus, input validation, and "keep going?" prompts
4. **Use For Loops for Counting**: When you know how many times to loop, use `for` with `range()`
5. **Communicate**: Check in with your partner regularly
6. **Comment As You Go**: Don't wait until the end
7. **Handle Bad Input**: Use `while` loops to re-prompt for valid input
8. **Ask for Help**: Use your teacher and classmates as resources

## While Loop Examples

**Input Validation:**
```python
grade = -1
while grade < 0 or grade > 100:
    grade = int(input("Enter grade (0-100): "))
```

**Menu System:**
```python
choice = ""
while choice != "quit":
    print("1. Add item")
    print("2. View items")
    choice = input("Enter choice: ")
```

**Keep Going Pattern:**
```python
continue_program = "yes"
while continue_program == "yes":
    # do something
    continue_program = input("Continue? (yes/no): ")
```

---

Good luck! Remember: this project tests everything you've learned about loops, conditionals, and input validation. Make it interesting, make it work, and most importantly—work together!