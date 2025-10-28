# String Manipulation by Building a Cipher

## Step 1: Variables

**Definition:**  
A variable is a name that references or points to an object. You assign a value to something, pointing it out.

**Example:**
```python
age = 25
name = "Alex"
```

**Key Points:**
- Variables assign a name to a value
- Use the `=` operator to assign
- Variable names are case-sensitive
- Choose clear, descriptive names

---

## Step 2: Strings

**Definition:**  
A string is a sequence of characters used to represent text. It must be enclosed in matching quotation marks.

**Example:**
```python
text = "Hello World"
```

**Key Points:**
- Strings must start and end with the same quote type
- Use either single quotes ' ' or double quotes " "
- Mismatched quotes cause errors

---

## Step 3: print() Function

**Definition:**  
The `print()` function is used to display output in the terminal. It is a built-in function that you can call to show results.

**Example:**
```python
# Calling the print function
print()
```

**Key Points:**
- print() outputs text to the console
- Functions are called using parentheses ()
- An empty print() call displays a blank line

---

## Step 4: Function Arguments

**Definition:**  
An argument is the value or expression passed to a function when it is called. It goes inside the parentheses.

**Example:**
```python
greet = 'Hello!'
print(greet)  # 'greet' is the argument passed to print()
```

**Key Points:**
- Arguments are placed inside the function's parentheses ()
- You can pass variables (like greet) or direct values (like "Hello!")
- The function uses the argument to perform its task

---

## Step 5: String Indexing

**Definition:**  
Each character in a string has a numerical index starting from 0. You can access individual characters using these indexes.

**Example:**
```python
text = "Hello World"
print(text[0])  # Output: 'H'
print(text[1])  # Output: 'e'
print(text[6])  # Output: 'W'
```

**Key Points:**
- Indexing starts at 0 (not 1)
- Use square brackets [] with the index number inside
- Access any character by its position number
- Spaces and symbols also have indexes

---

## Step 6: Negative Indexing

**Definition:**  
You can access characters from the end of a string using negative indexes. The last character is -1, second last is -2, etc.

**Example:**
```python
text = "Hello World"
print(text[-1])  # Output: 'd'
print(text[-2])  # Output: 'l'
print(text[-5])  # Output: 'W'
```
**Key Points:**
- Negative indexes start from -1 (last character)
- Use the same square brackets [] with negative numbers
- Example: variable_name[-1] accesses the last character
- Useful for getting characters from the end without knowing the length

---

## Step 7: len() Function

**Definition:**  
The `len()` function returns the number of characters in a string, including spaces and punctuation.

**Example:**
```python
text = 'Hello World'
print(len(text))   # Output: 11
```
**Key Points:**
- Counts all characters (letters, spaces, symbols)
- Returns the total length as a number
- len() is a built-in function like print()
- Spaces count as characters

---

## Step 8: type() Function

**Definition:**  
The `type()` function returns the data type of a variable or value.

**Example:**
```python
text = 'Hello World'
print(type(text))   # Output: <class 'str'>
```
**Key Points:**
- Shows the data type (class) of the variable
- str means string (text)
- Useful for checking what kind of data you're working with
- Works with all data types, not just strings

---

## Step 9: Variable Assignment

**Definition:**  
Creating a new variable and giving it a value using the assignment operator `=`.

**Example:**
```python
text = 'Hello World'
shift = 3
```
---

## Step 10: Printing Variables

**Definition:**  
Using the `print()` function to display the value stored in a variable.

**Example:**
```python
text = 'Hello World'
shift = 3
print(shift)   # Output: 3
```
---

## Step 11: Checking Data Types

**Definition:**  
Using `type()` inside `print()` to display a variable's data type.

**Example:**
```python
text = 'Hello World'
print(type(text))    # Output: <class 'str'>
shift = 3
print(type(shift))   # Output: <class 'int'>
```
---

## Step 12: Variable Assignment & Naming Rules

**Definition:**  
Creating a variable to store the alphabet string, following Python's naming conventions.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
```
**Key Points:**
- Variable names cannot use reserved keywords (for, while, True, etc.)
- Cannot start with numbers (2alphabet ❌)
- Only alphanumeric characters and underscores allowed
- Case-sensitive (alphabet ≠ Alphabet)
- Use snake_case convention (user_name not userName)

---

## Step 13: .find() Method

**Definition:**  
The `.find()` method searches for a character in a string and returns its index position.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
position = alphabet.find('z')
print(position)   # Output: 25
```
**Key Points:**
- Called on a string object using dot notation (string.find())
- Returns the index of the first occurrence
- Returns -1 if character not found
- Similar to indexing but searches by value, not position

---

## Step 14: Implementing .find for cipher project

**Definition:**  
Begin implementing the Caesar cipher by finding the alphabet position of the first character in your message.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
position = alphabet.find(text[0])              # Finds position of 'H'
print(position)                                # Output: -1
```
**Key Points:**
- text[0] gets the first character of your message
- alphabet.find(text[0]) finds its position in alphabet
- This is the first step to shift letters for encryption

---

## Step 15: Storing Return Values

**Definition:**  
Store the position returned by `.find()` in a variable to use later in the cipher.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0])
```
**Key Points:**
- Methods like .find() return values you can store
- Stored values can be reused in later calculations
- Essential for building multi-step algorithms like ciphers

---

## Step 16: Printing Stored Values

**Definition:**  
Print the stored index value to verify the position found by the `.find()` method.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0])
print(index)  # Output: -1
```
---

## Step 17: Handling Case Sensitivity

**Definition:**  
Using `.lower()` method to convert text to lowercase since alphabet only contains lowercase letters.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0])
print(index)                              # -1
print(text.lower())                       # hello world
```
**Key Points:**
- .find() returns -1 when character not found
- Uppercase 'H' not found in lowercase alphabet
- .lower() converts entire string to lowercase
- Essential for case-insensitive text processing

---

## Step 18: Converting Case for Search

**Definition:**  
Convert individual characters to lowercase before searching in the alphabet to handle uppercase letters.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0].lower())
print(index)                                # 7
```
**Key Points:**
- text[0].lower() converts 'H' to 'h' before searching
- Now finds position 7 instead of -1
- Handles mixed case input properly
- Only converts the character being searched, not the whole text

---

## Step 19: Accessing Shifted Character

**Definition:**  
Store the character from the alphabet at the found position using bracket notation.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0].lower())
print(index)
shifted = alphabet[index]
```
**Key Points:**
- alphabet[index] gets the character at position 7 ('h')
- shifted variable now stores the original character
- This is an intermediate step before applying the actual shift
- Uses string indexing to retrieve characters by position

---

## Step 20: Printing the Shifted Character

**Definition:**  
Print the character stored in the shifted variable to verify it matches the original character.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0].lower())
print(index)                                    # 7
shifted = alphabet[index]
print(shifted)                                  # h
```
**Key Points:**
- First print shows position (7)
- Second print shows character at that position ('h')
- Confirms we can retrieve original character from alphabet
- Verifies the indexing works correctly

---

## CURRENT STATUS:
We've built the first half: **Letter → Position → Letter**
Next up: **Actually shifting the position!**

## WHY THIS MATTERS:
Every encryption system needs reliable ways to:
1. Convert between letters and numbers
2. Handle different text cases
3. Process one step at a time

**You've built the foundation - now comes the encryption!**

---

## Step 21: Applying the Shift

**Definition:**  
Add the shift value to the position to get the encrypted character position.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0].lower())
print(index)                                     # 7
shifted = alphabet[index + shift]
print(shifted)                                   # k
```
**Key Points:**
- index + shift = 7 + 3 = 10
- alphabet[10] = 'k'
- First actual encryption: 'h' → 'k'
- This is the core of Caesar cipher - shifting positions

---

## Step 22: Preparing for Loops

**Definition:**  
Clearing the code to prepare for implementing loops that will process all characters automatically.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
```

---

## Step 23: Implementing For Loop

**Definition:**  
Creating a for loop to iterate through each character in the text string.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
for i in text:
```
**Key Points:**
- Loop will execute for each character in text
- i contains the current character during each iteration
- The colon : indicates the start of the loop body
- Next steps will add indented code to process each character

---

## Step 24: Adding Loop Body

**Definition:**  
Adding indented code inside the loop to execute for each character.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for i in text:
    print(i)
```
```python
Output
H
e
l
l
o

W
o
r
l
d
```
**Key Points:**
- Indented code (4 spaces) runs for each character
- print(i) executes 11 times (once per character)
- Without proper indentation: IndentationError
- The space in "Hello World" is also processed as a character

---

## Step 25: Meaningful Variable Names

**Definition:**  
Renaming the loop variable to something more descriptive than `i`.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text:
    print(char)
```
```python
Output
H
e
l
l
o

W
o
r
l
d
```
**Key Points:**
- char is more meaningful than i (clearly means "character")
- Variable names should describe what they contain
- Better readability and understanding
- Same functionality, clearer code

---

## Step 26: Finding Character Positions in Loop

**Definition:**  
Inside the loop, find the alphabet position of each character before printing.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text:
    index = alphabet.find(char)
    print(char)
```
```python
H
e
l
l
o

W
o
r
l
d
```
**Key Points:**
- index = alphabet.find(char) finds position of current character
- Runs for each character in the loop
- Currently not using the index value yet
- index will be -1 for spaces and uppercase letters

---

## Step 27: Printing Character and Position

**Definition:**  
Using `print()` with multiple arguments to display both the character and its alphabet position.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text:
    index = alphabet.find(char)
    print(char, index)
```
```python
Output
H -1
e 4
l 11
l 11
o 14
  -1
W -1
o 14
r 17
l 11
d 3
```
**Key Points:**
- print() can take multiple arguments separated by commas
- Shows character and its position together
- -1 means character not found in alphabet (uppercase, spaces)
- Confirms we need to handle case sensitivity

---

## Step 28: Handling Uppercase Letters

**Definition:**  
Converting the entire text to lowercase before processing to handle uppercase letters.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text.lower():
    index = alphabet.find(char)
    print(char, index)
```
```python
h 7
e 4
l 11
l 11
o 14
  -1
w 22
o 14
r 17
l 11
d 3
```
**Key Points:**
- text.lower() converts entire string to lowercase first
- Now 'h'=7, 'w'=22 (no more -1 for uppercase)
- Space still returns -1 (will handle later)
- All letters now found in alphabet correctly

---

## Step 29: Calculating Shifted Position

**Definition:**  
Creating a new variable to store the shifted position (current position + shift value).

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text.lower():
    index = alphabet.find(char)
    print(char, index)
    new_index = index + shift
```
**Key Points:**
- new_index = index + shift calculates the encrypted position
- For 'h' (index 7): 7 + 3 = 10
- For 'e' (index 4): 4 + 3 = 7
- Not printing new_index yet - just calculating it
- This is the core encryption step

---

## Step 30: String Immutability

**Definition:**  
Strings cannot be modified once created - they are immutable.

**Example:**
```python
text = 'Hello World'
text[0] = 'r'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text.lower():
    index = alphabet.find(char)
    print(char, index)
    new_index = index + shift
```
```python
TypeError: 'str' object does not support item assignment
```
**Key Points:**
- Strings are immutable (cannot change characters directly)
- text[0] = 'r' causes TypeError
- To "change" a string, you must create a new one
- This is why we build encrypted text piece by piece rather than modifying original

---

## Step 31: Fixing the Code & New Text

**Definition:**  
Removing the invalid string modification and assigning a new string value to the text variable.

**Example:**
```python
text = 'Albatross'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text.lower():
    index = alphabet.find(char)
    print(char, index)
    new_index = index + shift# Step 31: Fixing the Code & New Text
```
```python
a 0
l 11
b 1
a 0
t 19
r 17
o 14
s 18
s 18
```
**Key Points:**
- Removed text[0] = 'r' (invalid string modification)
- Assigned new string 'Albatross' to text variable
- All characters now found in alphabet (no -1 values)
- new_index calculated but not used yet

---

## Step 32: Returning to Original Text

**Definition:**  
Reverting back to the original 'Hello World' text by removing the 'Albatross' assignment.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text.lower():
    index = alphabet.find(char)
    print(char, index)
    new_index = index + shift
```
```python
h 7
e 4
l 11
l 11
o 14
  -1
w 22
o 14
r 17
l 11
d 3
```
**Key Points:**
- Back to original 'Hello World' text
- Space character still returns -1 (not in alphabet)
- All other characters found successfully
- new_index calculated for each character

---

## Step 33: Getting Encrypted Character

**Definition:**  
Converting the shifted position back into an actual character from the alphabet.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text.lower():
    index = alphabet.find(char)
    print(char, index)
    new_index = index + shift
    new_char = alphabet[new_index]
```
**Key Points:**
- new_index = position number (e.g., 10)
- new_char = actual letter at that position (e.g., 'k')
- Essential for building encrypted message
- Converts numbers back to readable text

---

## Step 34: Printing Encrypted Characters

**Definition:**  
Displaying the encrypted characters generated by shifting each letter's position.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text.lower():
    index = alphabet.find(char)
    print(char, index)
    new_index = index + shift
    new_char = alphabet[new_index]
    print(new_char)
```
```
h 7
k
e 4  
h
l 11
o
l 11
o
o 14
r
  -1
w 22
z
o 14
r
r 17
u
l 11
o
d 3
g
```
**Key Points:**
- Successfully encrypts letters: h→k, e→h, l→o, o→r,....etc.
- ERROR on space character (index = -1, alphabet[-1] doesn't exist)
- We need to handle non-alphabet characters
- Shows the encryption is working for valid letters

---











