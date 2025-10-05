# Lesson 3.4 Tasks: If Statements Practice

## Setup
Complete these tasks in IDLE or VS Code. Test thoroughly with different inputs!

---

## Task 1: Positive Number Checker ⭐
**Difficulty: Easy**

Write a program that asks for a number and prints "That's positive!" only if the number is greater than 0.

**Sample Run 1:**
```
Enter a number: 5
That's positive!
```

**Sample Run 2:**
```
Enter a number: -3
(nothing prints)
```

**Hints:**
- Use a simple `if` statement
- Check if `number > 0`

---

## Task 2: Even or Odd ⭐
**Difficulty: Easy**

Create a program that determines if a number is even or odd.

**Sample Run:**
```
Enter a number: 7
7 is odd
```

**Hints:**
- Use the modulus operator: `number % 2`
- If result is 0, it's even
- Otherwise, it's odd

---

## Task 3: Voting Eligibility ⭐
**Difficulty: Easy**

Write a program that checks if someone can vote (must be 18 or older).

**Sample Run 1:**
```
Enter your age: 16
Sorry, you cannot vote yet.
```

**Sample Run 2:**
```
Enter your age: 21
You are eligible to vote!
```

**Hints:**
- Use `if-else`
- Check if `age >= 18`

---

## Task 4: Temperature Advisory ⭐⭐
**Difficulty: Medium**

Create a program that gives different advice based on temperature:
- If temp >= 90: "It's hot! Stay hydrated."
- Otherwise: "Temperature is comfortable."

**Sample Run:**
```
Enter temperature in °F: 95
It's hot! Stay hydrated.
```

**Hints:**
- Use `if-else`
- Convert input to integer

---

## Task 5: Grade Pass/Fail with Comments ⭐⭐
**Difficulty: Medium**

Write a program that:
- Takes a grade (0-100)
- Prints whether the student passed (>= 60)
- If failed, tells them how many more points needed

**Sample Run 1:**
```
Enter your grade: 75
You passed!
```

**Sample Run 2:**
```
Enter your grade: 55
You did not pass.
You needed 5 more points.
```

**Hints:**
- Use `if-else`
- Calculate: `points_needed = 60 - grade`

---

## Task 6: Shopping Discount ⭐⭐
**Difficulty: Medium**

Create a discount calculator:
- If purchase is $100 or more: 10% discount
- Otherwise: no discount
- Show the discount amount and final price

**Sample Run 1:**
```
Enter purchase amount: $125
Discount: $12.50
Final price: $112.50
```

**Sample Run 2:**
```
Enter purchase amount: $75
No discount applied.
Final price: $75.00
```

**Hints:**
- Check if `amount >= 100`
- Calculate discount: `amount * 0.10`
- Calculate final: `amount - discount`
- Use `.2f` formatting for money

---

## Task 7: Number Comparator ⭐⭐
**Difficulty: Medium**

Write a program that compares two numbers and tells which is larger, or if they're equal.

**Sample Run:**
```
Enter first number: 15
Enter second number: 23
23 is larger than 15
```

**Hints:**
- Need to check three conditions:
  - `num1 > num2`
  - `num1 < num2`
  - `num1 == num2`
- Use `if-elif-else` (we'll learn this more in next lesson)

---

## Task 8: Speed Limit Checker ⭐⭐⭐
**Difficulty: Hard**

Create a program that checks if a driver is speeding:
- Speed limit: 65 mph
- If going exactly 65 or under: "Legal speed"
- If going 1-10 mph over: "Warning ticket" and fine of $50
- If going more than 10 mph over: "Speeding ticket" and fine of $100 + $10 per mph over the limit

**Sample Run 1:**
```
Enter your speed: 70
Warning ticket
Fine: $50
```

**Sample Run 2:**
```
Enter your speed: 85
Speeding ticket!
Fine: $300
```

**Hints:**
- Calculate how much over: `over = speed - 65`
- Use nested if statements or multiple conditions
- For major speeding: `fine = 100 + (over * 10)`

---

## Task 9: BMI Calculator ⭐⭐⭐
**Difficulty: Hard**

Write a BMI (Body Mass Index) calculator that:
- Asks for weight in pounds
- Asks for height in inches
- Calculates BMI: (weight / height²) × 703
- Displays the BMI
- Tells if underweight (BMI < 18.5) or healthy weight (BMI >= 18.5)

**Sample Run:**
```
Enter weight in pounds: 150
Enter height in inches: 68
Your BMI is 22.8
You are at a healthy weight.
```

**Hints:**
- BMI formula: `bmi = (weight / (height ** 2)) * 703`
- Use `if-else` to check category
- Format BMI to 1 decimal place

---

## Task 10: Simple Password Checker ⭐⭐⭐
**Difficulty: Hard**

Create a basic password validation program:
- Ask user to create a password
- Check if it's at least 8 characters long
- If yes: "Password accepted"
- If no: "Password too short" and tell how many more characters needed

**Sample Run 1:**
```
Create a password: hello
Password too short. Need 3 more characters.
```

**Sample Run 2:**
```
Create a password: MySecure123
Password accepted!
```

**Hints:**
- Use `len(password)` to get length
- Check if `len(password) >= 8`
- Calculate needed: `8 - len(password)`

---

## Challenge Task: Quadratic Solver 🌟
**Difficulty: Challenge**

Write a program that solves a quadratic equation (ax² + bx + c = 0):
- Ask for a, b, and c
- Calculate discriminant: b² - 4ac
- If discriminant is negative: print "No real solutions"
- Otherwise: calculate and print the solutions using the quadratic formula

Quadratic formula: x = (-b ± √(b² - 4ac)) / (2a)

**Sample Run:**
```
Enter a: 1
Enter b: -5
Enter c: 6
Solution 1: 3.0
Solution 2: 2.0
```

**Hints:**
- Import math for sqrt
- Calculate discriminant first
- If discriminant >= 0, calculate both solutions:
  - `x1 = (-b + sqrt(discriminant)) / (2*a)`
  - `x2 = (-b - sqrt(discriminant)) / (2*a)`

---

## Bonus Challenge: Triangle Validator 🌟
**Difficulty: Challenge**

Create a program that checks if three sides can form a valid triangle.

**Triangle Rule:** The sum of any two sides must be greater than the third side.

**Sample Run 1:**
```
Enter side 1: 3
Enter side 2: 4
Enter side 3: 5
These sides can form a valid triangle!
```

**Sample Run 2:**
```
Enter side 1: 1
Enter side 2: 2
Enter side 3: 10
These sides cannot form a triangle.
```

**Hints:**
- Check three conditions:
  - `a + b > c`
  - `a + c > b`
  - `b + c > a`
- All three must be true
- Can use nested ifs or logical operators (next lesson)

---

## Submission Checklist

- [ ] All programs run without errors
- [ ] Tested with multiple inputs (including edge cases)
- [ ] Code properly indented
- [ ] Don't forget the colons after if/else
- [ ] Using == for comparison (not =)
- [ ] Comments explain your logic

## Common Mistakes to Watch For

1. **Using = instead of ==**
   ```python
   if x = 5:  # ERROR!
   if x == 5:  # CORRECT
   ```

2. **Forgetting the colon**
   ```python
   if x > 5  # ERROR!
   if x > 5:  # CORRECT
   ```

3. **Wrong indentation**
   ```python
   if x > 5:
   print("hi")  # ERROR - not indented
   
   if x > 5:
       print("hi")  # CORRECT
   ```

4. **Comparing strings and numbers**
   ```python
   age = input("Age: ")  # This is a STRING
   if age >= 18:  # ERROR - comparing string to number
   
   age = int(input("Age: "))  # CORRECT - convert to int first
   if age >= 18:
   ```