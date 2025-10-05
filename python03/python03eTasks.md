# Lesson 3.5 Tasks: Multi-Way Selection Practice

## Setup
Complete these tasks in IDLE or VS Code. Remember to test with various inputs!

---

## Task 1: Day of the Week ⭐
**Difficulty: Easy**

Write a program that takes a number (1-7) and prints the corresponding day of the week.
- 1 = Monday, 2 = Tuesday, etc.
- If the number is not 1-7, print "Invalid day"

**Sample Run:**
```
Enter day number (1-7): 4
Thursday
```

**Hints:**
- Use if-elif-elif... for each day
- Use else for invalid input
- Use == to check each number

---

## Task 2: Letter Grade with Plus/Minus ⭐⭐
**Difficulty: Medium**

Create a more detailed grade converter that includes + and - grades:
- A: 93-100
- A-: 90-92
- B+: 87-89
- B: 83-86
- B-: 80-82
- C+: 77-79
- C: 73-76
- C-: 70-72
- D: 60-69
- F: below 60

**Sample Run:**
```
Enter grade: 88
Your letter grade is: B+
```

**Hints:**
- Order from highest to lowest
- Use >= for boundaries
- Many elif statements needed!

---

## Task 3: Shipping Calculator ⭐⭐
**Difficulty: Medium**

Write a program that calculates shipping costs based on weight:
- Under 2 lbs: $5.00
- 2-10 lbs: $8.50
- 10-20 lbs: $12.00
- Over 20 lbs: $15.00 + $0.50 per pound over 20

**Sample Run 1:**
```
Enter package weight in lbs: 15
Shipping cost: $12.00
```

**Sample Run 2:**
```
Enter package weight in lbs: 25
Shipping cost: $17.50
```

**Hints:**
- For over 20 lbs: `15 + ((weight - 20) * 0.50)`
- Use .2f formatting for money

---

## Task 4: Season Identifier ⭐⭐
**Difficulty: Medium**

Create a program that identifies the season based on the month number (1-12):
- Winter: 12, 1, 2
- Spring: 3, 4, 5
- Summer: 6, 7, 8
- Fall: 9, 10, 11

**Sample Run:**
```
Enter month number (1-12): 7
Summer
```

**Hints:**
- You can check multiple values in one condition
- Or use separate if statements for each month

---

## Task 5: Triangle Type Classifier ⭐⭐⭐
**Difficulty: Hard**

Write a program that classifies a triangle based on side lengths:
- Equilateral: all three sides equal
- Isosceles: exactly two sides equal
- Scalene: all sides different
- Invalid: sides cannot form a triangle

Remember: For a valid triangle, the sum of any two sides must be greater than the third side.

**Sample Run:**
```
Enter side 1: 5
Enter side 2: 5
Enter side 3: 5
This is an equilateral triangle.
```

**Hints:**
- First check if it's a valid triangle
- Then check if all three equal (equilateral)
- Then check if any two equal (isosceles)
- Otherwise scalene

---

## Task 6: Tax Bracket Calculator ⭐⭐⭐
**Difficulty: Hard**

Create a tax calculator that uses these brackets:
- $0 - $10,000: 10% tax
- $10,001 - $40,000: 12% tax
- $40,001 - $85,000: 22% tax
- $85,001+: 24% tax

Display the income, tax rate, and amount owed.

**Sample Run:**
```
Enter annual income: $50000
Income: $50,000.00
Tax rate: 22%
Tax owed: $11,000.00
```

**Hints:**
- Convert income to float
- Calculate tax: `income * rate`
- Format all money to 2 decimal places

---

## Task 7: Water State Identifier ⭐⭐
**Difficulty: Medium**

Write a program that identifies the state of water based on temperature in Celsius:
- Below 0°C: Solid (Ice)
- Exactly 0°C: Freezing point
- 0°C - 100°C: Liquid (Water)
- Exactly 100°C: Boiling point
- Above 100°C: Gas (Steam)

**Sample Run:**
```
Enter temperature in °C: 25
Water is in a liquid state.
```

**Hints:**
- Check for exact values first (==)
- Then use ranges with < and >

---

## Task 8: Movie Ticket Pricer ⭐⭐⭐
**Difficulty: Hard**

Create a movie ticket pricing system:
- Children (under 13): $7.00
- Teens (13-17): $9.00
- Adults (18-64): $12.00
- Seniors (65+): $8.00

Also ask if it's a matinee (before 5 PM) - if yes, subtract $2.00 from the price.

**Sample Run:**
```
Enter age: 25
Matinee showing? (yes/no): yes
Ticket price: $10.00
```

**Hints:**
- First determine base price by age
- Then check for matinee discount
- Use `.lower()` to handle "yes", "Yes", "YES", etc.

---

## Task 9: Grade Point Average ⭐⭐⭐
**Difficulty: Hard**

Write a program that converts letter grades to GPA points:
- A = 4.0
- B = 3.0
- C = 2.0
- D = 1.0
- F = 0.0

Then ask for 5 letter grades and calculate the GPA.

**Sample Run:**
```
Enter grade 1: A
Enter grade 2: B
Enter grade 3: A
Enter grade 4: B
Enter grade 5: A
Your GPA is: 3.6
```

**Hints:**
- Create a loop to get 5 grades
- For each grade, convert to points
- Add to a total
- Divide by 5 for average

---

## Task 10: Rock-Paper-Scissors Judge ⭐⭐⭐
**Difficulty: Hard**

Create a program that determines the winner of rock-paper-scissors:
- Rock beats scissors
- Scissors beats paper
- Paper beats rock
- Same choice = tie

**Sample Run:**
```
Player 1 choice (rock/paper/scissors): rock
Player 2 choice (rock/paper/scissors): scissors
Player 1 wins!
```

**Hints:**
- First check for a tie (both same)
- Then check all win conditions for player 1
- Else player 2 wins
- Use `.lower()` for input consistency

---

## Challenge Task: Leap Year Calculator 🌟
**Difficulty: Challenge**

Write a program that determines if a year is a leap year.

Rules:
- If divisible by 4: it's a leap year
- EXCEPT if divisible by 100: not a leap year
- EXCEPT if divisible by 400: it IS a leap year

Examples:
- 2020: leap year (divisible by 4)
- 1900: NOT a leap year (divisible by 100 but not 400)
- 2000: leap year (divisible by 400)

**Sample Run:**
```
Enter a year: 2024
2024 is a leap year.
```

**Hints:**
- Check conditions in order: 400, then 100, then 4
- Use modulus operator: `year % 400 == 0`

---

## Bonus Challenge: Roman Numeral Converter 🌟🌟
**Difficulty: Very Hard**

Create a program that converts numbers 1-10 to Roman numerals:
- 1 = I, 2 = II, 3 = III, 4 = IV, 5 = V
- 6 = VI, 7 = VII, 8 = VIII, 9 = IX, 10 = X

**Sample Run:**
```
Enter a number (1-10): 7
Roman numeral: VII
```

Then extend it to handle numbers 1-100!
- X = 10, XX = 20, XXX = 30, XL = 40, L = 50
- LX = 60, LXX = 70, LXXX = 80, XC = 90, C = 100

---

## Submission Checklist

- [ ] All programs use elif (not multiple ifs)
- [ ] Conditions ordered correctly (most restrictive first)
- [ ] else clause handles invalid/unexpected input
- [ ] Test with edge cases (boundaries between categories)
- [ ] Code properly indented
- [ ] Comments explain decision logic

## Testing Tips

For programs with ranges, test:
- The minimum value in each range
- The maximum value in each range
- Values just outside the range
- Invalid input

Example for grade converter:
- Test: 100, 90, 89, 80, 79, 70, 69, 60, 59, 0
- These hit all the boundaries!

## Common Mistakes

1. **Using separate ifs instead of elif**
   ```python
   # WRONG - all conditions check
   if grade >= 90:
       letter = 'A'
   if grade >= 80:  # Still checks!
       letter = 'B'  # Overwrites A!
   
   # CORRECT - stops after first match
   if grade >= 90:
       letter = 'A'
   elif grade >= 80:
       letter = 'B'
   ```

2. **Wrong order of conditions**
   ```python
   # WRONG - catches too much
   if grade >= 60:  # This catches 60-100!
       letter = 'D'
   elif grade >= 70:  # Never reached
       letter = 'C'
   ```

3. **Using wrong comparison operators**
   ```python
   # WRONG - 90 doesn't get an A
   if grade > 90:  # Should be >=
       letter = 'A'
   ```