# Lesson 3i Tasks: Team Functions Project

## Team Project Setup
**Team Size:** 2 students per team  
**Goal:** Build TWO complete programs using functions

---

## Project Requirements

Your team must complete:
1. **ONE Fun Project** (choose from Options 1-2)
2. **ONE Real-World Project** (choose from Options 3-4)

### Grading Criteria

Each project will be graded on:
- [ ] Code runs without errors
- [ ] At least 4 different functions defined
- [ ] Functions have clear, descriptive names
- [ ] Functions use parameters and return values appropriately
- [ ] Code is well-commented
- [ ] Program handles invalid input gracefully
- [ ] Code is organized and easy to read
- [ ] Both team members contributed

---

### AI Rules: 
You can use AI only to help you understand how to build out the logic if you are struggling with the program(s).  You can't use it for code development, just how to set up the structure.  I want your team to figure out how to write the functions, but because this is a complex project, you can use AI to help you think through how to structure the code such as a flowchart, pseudocode, etc.  

---

## Fun Project Option 1: Magic 8-Ball Fortune Teller

Create an interactive Magic 8-Ball program that gives random answers to yes/no questions.

### What It Should Do:
- Display a welcome message
- Let user ask multiple questions
- Give random fortunes/answers
- Keep track of how many questions asked
- Have at least 10 different possible answers

### Starter Code:



```python
import random

def display_welcome():
    """Display a welcome banner for the Magic 8-Ball."""
    # YOUR CODE HERE
    pass

def get_question():
    """Get a question from the user. Return the question."""
    # YOUR CODE HERE
    pass

def get_fortune():
    """Return a random fortune from a list of possible answers."""
    # Hint: Create a list of at least 10 different answers
    # Use random.choice() or random.randint()
    # YOUR CODE HERE
    pass

def display_fortune(fortune):
    """Display the fortune in a fancy way."""
    # YOUR CODE HERE
    pass

def play_again():
    """Ask user if they want to ask another question. Return True or False."""
    # YOUR CODE HERE
    pass

# Main program
display_welcome()
question_count = 0

# YOUR CODE HERE - Write the main game loop
# Use the functions above to create the complete program
```

### Example Output:
```
═══════════════════════════
MAGIC 8-BALL FORTUNE TELLER 
═══════════════════════════

Ask a yes/no question: Will I get an A in this class?
🔮 The Magic 8-Ball says: "Without a doubt!"

Ask another question? (yes/no): yes
Ask a yes/no question: Will it rain tomorrow?
🔮 The Magic 8-Ball says: "Outlook not so good"

Ask another question? (yes/no): no
You asked 2 questions. Thanks for playing!
```

### Suggested Additional Functions:
- `shake_ball()` - Display animation/delay before showing answer
- `validate_question(question)` - Check if question ends with "?"
- `display_stats(count)` - Show final statistics

---

## Fun Project Option 2: Text Adventure Game

Create a simple text-based adventure game with multiple rooms/locations.

### What It Should Do:
- Player can move between at least 3 locations
- Each location has a description
- Player can collect items
- Game has a win condition
- Player can see inventory

### Starter Code:

```python
def display_title():
    """Display the game title and intro."""
    # YOUR CODE HERE
    pass

def display_location(location_name):
    """Display description of current location."""
    # Hint: Use if/elif statements or a dictionary
    # to store location descriptions
    # YOUR CODE HERE
    pass

def get_command():
    """Get a command from the player. Return the command."""
    # Commands might be: north, south, east, west, take, inventory, quit
    # YOUR CODE HERE
    pass

def move_player(current_location, direction):
    """
    Move the player in the given direction.
    Return the new location, or current location if can't move that way.
    """
    # YOUR CODE HERE
    pass

def show_inventory(items):
    """Display the player's inventory."""
    # YOUR CODE HERE
    pass

def check_win_condition(items):
    """Check if player has won. Return True or False."""
    # YOUR CODE HERE
    pass

# Main program
display_title()
current_room = "start"
inventory = []
playing = True

# YOUR CODE HERE - Write the main game loop
# Use the functions above to create the complete program
```

### Example Output:
```
═══════════════════════
 THE MYSTERIOUS MANSION 
═══════════════════════

You wake up in a dark entrance hall...

> north
You enter the library. Dusty books line the walls.
There is a KEY on the table.

> take key
You picked up the key!

> south
You are back in the entrance hall.

> inventory
You are carrying: key

> east
You use the key to unlock the treasure room!
You found the treasure! YOU WIN!
```

### Suggested Additional Functions:
- `add_item(inventory, item)` - Add item to inventory
- `has_item(inventory, item)` - Check if player has specific item
- `display_help()` - Show available commands

---

## Real-World Project Option 3: Student Grade Calculator

Create a grade management system for tracking student scores.

### What It Should Do:
- Add multiple assignment scores
- Calculate average
- Determine letter grade
- Show statistics (highest, lowest, average)
- Handle at least 5 assignments

### Starter Code:

```python
def display_menu():
    """Display the main menu options."""
    # YOUR CODE HERE
    pass

def add_grade(grades):
    """
    Prompt for a new grade and add it to the list.
    Return the updated list.
    """
    # YOUR CODE HERE
    pass

def calculate_average(grades):
    """Calculate and return the average of grades."""
    # Hint: Watch for empty list!
    # YOUR CODE HERE
    pass

def get_letter_grade(average):
    """Convert numeric average to letter grade. Return the letter."""
    # YOUR CODE HERE
    pass

def find_highest(grades):
    """Find and return the highest grade."""
    # YOUR CODE HERE
    pass

def find_lowest(grades):
    """Find and return the lowest grade."""
    # YOUR CODE HERE
    pass

def display_report(grades):
    """Display complete grade report with statistics."""
    # YOUR CODE HERE
    # Should show: all grades, average, letter grade, highest, lowest
    pass

# Main program
print("=== STUDENT GRADE CALCULATOR ===")
student_grades = []

# YOUR CODE HERE - Write the main program loop
# Allow user to add grades, view report, and quit
```

### Example Output:
```
=== STUDENT GRADE CALCULATOR ===

1. Add a grade
2. View grade report
3. Quit

Choice: 1
Enter grade (0-100): 85
Grade added!

Choice: 1
Enter grade (0-100): 92
Grade added!

Choice: 1
Enter grade (0-100): 78
Grade added!

Choice: 2

═══════════════
 GRADE REPORT    
═══════════════

Grades: 85, 92, 78
Number of assignments: 3

Average: 85.0
Letter Grade: B

Highest: 92
Lowest: 78

Choice: 3
Goodbye!
```

### Suggested Additional Functions:
- `remove_grade(grades)` - Remove a specific grade
- `drop_lowest(grades)` - Calculate average dropping lowest score
- `validate_grade(grade)` - Check if grade is 0-100
- `save_grades(grades, filename)` - Save grades to a file (advanced)

---

## Real-World Project Option 4: Restaurant Bill Calculator

Create a bill calculator for a restaurant with tip and split options.

### What It Should Do:
- Allow adding multiple menu items with prices
- Calculate subtotal
- Add tax
- Calculate tip (user chooses percentage)
- Split bill among multiple people
- Display formatted receipt

### Starter Code:

```python
def display_menu():
    """Display restaurant menu with prices."""
    # Create a menu with at least 6 items
    # YOUR CODE HERE
    pass

def get_order():
    """
    Let user order items. Return a list of items ordered
    and a list of their prices.
    """
    # YOUR CODE HERE
    pass

def calculate_subtotal(prices):
    """Calculate and return the subtotal of all prices."""
    # YOUR CODE HERE
    pass

def calculate_tax(subtotal, tax_rate):
    """Calculate and return the tax amount."""
    # YOUR CODE HERE
    pass

def calculate_tip(subtotal, tip_percent):
    """Calculate and return the tip amount."""
    # YOUR CODE HERE
    pass

def calculate_total(subtotal, tax, tip):
    """Calculate and return the final total."""
    # YOUR CODE HERE
    pass

def split_bill(total, num_people):
    """Calculate how much each person pays. Return amount per person."""
    # YOUR CODE HERE
    pass

def display_receipt(items, prices, subtotal, tax, tip, total, per_person=None):
    """Display a formatted receipt."""
    # YOUR CODE HERE
    pass

# Main program
print("════════════════════════════")
print("RESTAURANT BILL CALCULATOR")
print("════════════════════════════")

TAX_RATE = 0.08  # 8% tax

# YOUR CODE HERE - Write the main program
# 1. Display menu
# 2. Take order
# 3. Calculate all amounts
# 4. Ask for tip percentage
# 5. Ask if splitting bill
# 6. Display receipt
```

### Example Output:
```
═══════════════════════════
 RESTAURANT BILL CALCULATOR
═══════════════════════════

MENU:
1. Burger - $12.99
2. Pizza - $14.99
3. Salad - $8.99
4. Pasta - $13.99
5. Soda - $2.99
6. Done ordering

Enter item number: 1
Added Burger!

Enter item number: 3
Added Salad!

Enter item number: 5
Added Soda!

Enter item number: 6

Tip percentage (15, 18, 20): 18
Split bill? How many people? (1 for no split): 2

═══════
RECEIPT    
═══════

Burger                      $12.99
Salad                       $ 8.99
Soda                        $ 2.99
                          --------
Subtotal:                  $24.97
Tax (8%):                  $ 2.00
Tip (18%):                 $ 4.49
                          --------
TOTAL:                     $31.46

Split between 2 people
Each person pays:          $15.73

Thank you for dining with us!
```

### Suggested Additional Functions:
- `format_price(amount)` - Format number as price with $
- `get_tip_percentage()` - Get valid tip percentage from user
- `validate_menu_choice(choice, max_items)` - Validate menu selection
- `display_items_list(items, prices)` - Show what was ordered

---

## Team Work Guidelines

### None of this is mandatory, but some ideas on how to divide up the work: 

**Option A - By Function:**
- Partner 1: Write functions 1-4
- Partner 2: Write functions 5-8
- Together: Write main program and test

**Option B - By Feature:**
- Partner 1: Input and validation functions
- Partner 2: Calculation and display functions
- Together: Integration and testing

**Option C - Parallel Development:**
- Both: Outline all functions together
- Partner 1: Build Project 1
- Partner 2: Build Project 2
- Both: Review each other's code

### Tips for Success

1. **Plan together first** - Outline all functions before coding
2. **Define function signatures** - Agree on parameter names and return values
3. **Write docstrings** - Document what each function does
4. **Test as you go** - Don't wait until the end
5. **Communicate** - Ask questions, share ideas
6. **Comment your code** - Help your partner understand your logic
7. **Test edge cases** - What if user enters invalid input?

### Common Pitfalls to Avoid

- Don't split into "one person does everything" - both must code!
- Don't leave testing until the end
- Don't forget to handle invalid input
- Don't make functions too long (keep them under 15 lines)
- Don't forget docstrings
- Don't copy-paste code - use functions to avoid repetition!

---

## Submission Requirements

Push the following to GitHub Python Repo (both team members need to push so you'll have to share the files when done)

1. **Python file** (.py) with all code
2. **Comments** at the top with:
   - Both team members' names
   - Which project option you chose
   - Description of who did what
   - Any major problems you ran into 

---

## Testing Checklist

Before submitting, verify:

- [ ] All functions have docstrings
- [ ] Program runs without errors
- [ ] Invalid input is handled gracefully
- [ ] Functions are used (not all code in main program)
- [ ] Functions have descriptive names
- [ ] Code is commented where needed
- [ ] Both team members understand all the code
- [ ] Tested with various inputs
- [ ] Output is formatted nicely
- [ ] Follows Python style (proper indentation, spacing)

---

## Rubric (30 points per project)

| Category | Points | Description |
|----------|--------|-------------|
| Functionality | 9 | Program works correctly, handles all requirements |
| Functions | 7 | At least 4 functions, properly defined with parameters/returns |
| Code Quality | 6 | Clean, organized, follows Python conventions |
| Input Handling | 3 | Validates input, handles errors gracefully |
| Documentation | 3 | Comments, docstrings, clear variable names |
| Teamwork | 2 | Both members contributed, documented division of labor |


---

## Example Function Skeleton

Here's a template for any function you write:

```python
def function_name(parameter1, parameter2):
    """
    Brief description of what this function does.
    
    Parameters:
        parameter1: description
        parameter2: description
    
    Returns:
        description of return value
    """
    # Your code here
    
    return result
```

---

## Help Resources

- Lesson 3i notes on functions
- Python documentation: https://docs.python.org
- Ask Mr. M for help during work time
- Test each function individually before combining

---

## Good Luck!

Remember: 
- **Start simple** - Get basic version working first
- **Test often** - Don't write all code before testing
- **Help each other** - Explain your code to your partner
- **Have fun** - These projects show off what you've learned!

