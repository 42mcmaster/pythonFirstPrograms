# Lesson 3c: String Traversal

## Learning Objectives
- Understand that strings are sequences
- Traverse characters in a string using for loops
- Use basic string methods

##  Why This Lesson Matters: Real-World Applications

**String traversal** (looping through characters) is everywhere in programming:

- **Password validation**: Checking if passwords contain required characters (uppercase, numbers, symbols)
- **Data cleaning**: Removing unwanted characters from user input (like spaces in phone numbers)
- **Text analysis**: Counting letters, words, or patterns in documents
- **Game programming**: Processing player names, checking valid moves in word games
- **Form validation**: Verifying that email addresses, zip codes, or usernames are formatted correctly

Every time you type something into a website and it says "Password must contain a number" or "Please enter a valid email" - that's string traversal at work!

---

## Strings as Sequences

In Python, strings are **sequences of characters**. This means you can loop through them one character at a time!

### Basic String Traversal

```python
for character in "Hi there!":
    print(character)

# Output:
# H
# i
#  
# t
# h
# e
# r
# e
# !
```

Notice:
- Each character is processed one at a time
- Even the space is a character!
- We don't need `range()` - we can loop directly through the string

### Example: Counting Vowels

```python
text = input("Enter some text: ")
vowel_count = 0

for char in text:
    if char in "aeiouAEIOU":
        vowel_count += 1

print(f"Number of vowels: {vowel_count}")
```

**Sample Run:**
```
Enter some text: Hello World
Number of vowels: 3
```

### Example: Password Checker

```python
password = input("Enter a password: ")
has_digit = False

for char in password:
    if char.isdigit():
        has_digit = True

if has_digit:
    print("✓ Password contains a number")
else:
    print("✗ Password must contain at least one number")
```

## Useful String Methods

Python strings have built-in methods that help you check characters:

```python
char = "A"

# Check character type
char.isdigit()    # True if it's a number (0-9)
char.isalpha()    # True if it's a letter (a-z, A-Z)
char.isupper()    # True if it's uppercase
char.islower()    # True if it's lowercase
char.isspace()    # True if it's whitespace (space, tab, etc.)
```

### Example: Analyzing Text

```python
text = input("Enter some text: ")

letters = 0
digits = 0
spaces = 0

for char in text:
    if char.isalpha():
        letters += 1
    elif char.isdigit():
        digits += 1
    elif char.isspace():
        spaces += 1

print(f"Letters: {letters}")
print(f"Digits: {digits}")
print(f"Spaces: {spaces}")
```

**Sample Run:**
```
Enter some text: Python 3 is awesome!
Letters: 14
Digits: 1
Spaces: 3
```

## Building New Strings

You can build new strings by adding characters as you loop:

```python
text = "Hello World"
vowels_only = ""

for char in text:
    if char in "aeiouAEIOU":
        vowels_only += char

print(vowels_only)  # Output: eoo
```

### Example: Removing Spaces

```python
phone = input("Enter phone number: ")
clean_phone = ""

for char in phone:
    if not char.isspace() and char != "-":
        clean_phone += char

print(f"Cleaned: {clean_phone}")
```

**Sample Run:**
```
Enter phone number: 555-123-4567
Cleaned: 5551234567
```

## Quick Reference: String Character Methods

| Method | Returns True if... | Example |
|--------|-------------------|---------|
| `.isdigit()` | Character is 0-9 | `"5".isdigit()` → True |
| `.isalpha()` | Character is a letter | `"A".isalpha()` → True |
| `.isupper()` | Character is uppercase | `"A".isupper()` → True |
| `.islower()` | Character is lowercase | `"a".islower()` → True |
| `.isspace()` | Character is whitespace | `" ".isspace()` → True |

## Key Points

1. **Strings are sequences** - you can loop through them character by character
2. **Use `for char in string`** - no need for range() or indices
3. **String methods help** - use `.isdigit()`, `.isalpha()`, etc. to check characters
4. **Build new strings** - use `+=` to add characters to a new string
