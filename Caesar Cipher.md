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

## Step 35: Cleaning Output Format

**Definition:**  
Improving output readability by labeling the original and encrypted characters.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text.lower():
    index = alphabet.find(char)
    new_index = index + shift
    new_char = alphabet[new_index]
    print('char:', char, 'new char:', new_char)
```
```
char: h new char: k
char: e new char: h  
char: l new char: o
char: l new char: o
char: o new char: r
...
```
**Key Points:**
- Clear labels show transformation: 'char: h new char: k'
- Easier to understand the encryption process
- Still need to handle the space character error
- Better debugging and visualization

---

## Step 36: Initializing Encrypted Text

**Definition:**  
Creating an empty string variable to store the final encrypted message.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    index = alphabet.find(char)
    new_index = index + shift
    new_char = alphabet[new_index]
    print('char:', char, 'new char:', new_char)
```
**Key Points:**
- encrypted_text = '' creates an empty string container
- This variable will gradually build the encrypted message
- Empty string '' is like a blank canvas to paint on
- Essential for collecting all encrypted characters into one result

---

## Step 37: Building Encrypted Text

**Definition:**  
Storing each encrypted character in the encrypted_text variable and tracking the progress.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    index = alphabet.find(char)    
    new_index = index + shift
    encrypted_text = alphabet[new_index]
    print('char:', char, 'encrypted text:', encrypted_text)
```
```
char: h encrypted text: k
char: e encrypted text: h
char: l encrypted text: o
char: l encrypted text: o
char: o encrypted text: r
char:   encrypted text: c
char: w encrypted text: z
char: o encrypted text: r
char: r encrypted text: u
char: l encrypted text: o
char: d encrypted text: g
```
**Key Points:**
- encrypted_text now stores the current encrypted character
- BUT it's overwriting each time instead of building up
- Notice encrypted text: shows only one character at a time
- We need to append rather than replace (next step)
- Space character surprisingly worked (gave 'c') due to index calculation

---

## Step 38: Building the Encrypted String

**Definition:**  
Appending each encrypted character to build the complete encrypted message.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    index = alphabet.find(char)
    new_index = index + shift
    encrypted_text = encrypted_text + alphabet[new_index]
    print('char:', char, 'encrypted text:', encrypted_text)
```
```
char: h encrypted text: k
char: e encrypted text: kh
char: l encrypted text: kho
char: l encrypted text: khoo
char: o encrypted text: khoor
char:   encrypted text: khooc
char: w encrypted text: khoocz
char: o encrypted text: khooczr
char: r encrypted text: khooczru
char: l encrypted text: khooczruo
char: d encrypted text: khooczruog
```
**Key Points:**
- encrypted_text + alphabet[new_index] appends instead of replacing
- Now builds the complete encrypted string step by step
- Still has the space bug - space became 'c' in the output
- Can see the encryption growing: k → kh → kho → khoo → khoor → etc.

---

## Step 39: Using += Operator

**Definition:**  
Using the addition assignment operator `+=` to append characters more efficiently.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    index = alphabet.find(char)
    new_index = index + shift
    encrypted_text += alphabet[new_index]
    print('char:', char, 'encrypted text:', encrypted_text)
```
```
char: h encrypted text: k
char: e encrypted text: kh
char: l encrypted text: kho
char: l encrypted text: khoo
char: o encrypted text: khoor
char:   encrypted text: khoorc
char: w encrypted text: khoorcz
char: o encrypted text: khoorczr
char: r encrypted text: khoorczru
char: l encrypted text: khoorczruo
char: d encrypted text: khoorczruog
```
**Key Points:**
- encrypted_text += alphabet[new_index] is shorthand for encrypted_text = encrypted_text + alphabet[new_index]
- Same functionality, cleaner code
- Space bug still present: space → 'c' in "khoorc"
- Building encrypted string: k → kh → kho → khoo → khoor → khoorc → etc.

---

## Step 40: Using Comparison Operators

**Definition:**  
Using the equality operator `==` to identify space characters in the text.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    print(char == ' ')
    index = alphabet.find(char)
    new_index = index + shift
    encrypted_text += alphabet[new_index]
    print('char:', char, 'encrypted text:', encrypted_text)
```
```
False
char: h encrypted text: k
False
char: e encrypted text: kh
False
char: l encrypted text: kho
False
char: l encrypted text: khoo
False
char: o encrypted text: khoor
True
char:   encrypted text: khoorc
False
char: w encrypted text: khoorcz
False
char: o encrypted text: khoorczr
False
char: r encrypted text: khoorczru
False
char: l encrypted text: khoorczruo
False
char: d encrypted text: khoorczruog
```
**Key Points:**
- char == ' ' returns True only for space character
- False for all letters, True for space (6th character)
- This is the first step to fix the space bug
- We can now detect spaces and handle them differently

---

## Step 41: Conditional Logic with if Statement

**Definition:**  
Using an if statement to detect space characters and take specific action when they are found.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    if char == ' ':
        print('space!')
    index = alphabet.find(char)
    new_index = index + shift
    encrypted_text += alphabet[new_index]
    print('char:', char, 'encrypted text:', encrypted_text)
```
```
char: h encrypted text: k
char: e encrypted text: kh
char: l encrypted text: kho
char: l encrypted text: khoo
char: o encrypted text: khoor
space!
char:   encrypted text: khoorc
char: w encrypted text: khoorcz
char: o encrypted text: khoorczr
char: r encrypted text: khoorczru
char: l encrypted text: khoorczruo
char: d encrypted text: khoorczruog
```
**Key Points:**
- if char == ' ': detects space characters
- print('space!') only executes when a space is found
- Space bug still present - space still becomes 'c' in encrypted text
- Next step will likely fix the space handling

---

## Step 42: Handling Spaces in Encryption

**Definition:**  
Adding space characters directly to the encrypted text instead of encrypting them as letters.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    if char == ' ':
        encrypted_text += char  
    index = alphabet.find(char)
    new_index = index + shift
    encrypted_text += alphabet[new_index]
    print('char:', char, 'encrypted text:', encrypted_text)
```
```
char: h encrypted text: k
char: e encrypted text: kh
char: l encrypted text: kho
char: l encrypted text: khoo
char: o encrypted text: khoor
char:   encrypted text: khoor c
char: w encrypted text: khoor cz
char: o encrypted text: khoor czr
char: r encrypted text: khoor czru
char: l encrypted text: khoor czruo
char: d encrypted text: khoor czruog
```
**Key Points:**
- encrypted_text += char adds the space character directly
- Should preserve spaces in the encrypted message
- But there's still a logic issue - both the if block AND the regular encryption run for spaces
- We need to skip the regular encryption for spaces (next step)

---

## Step 43: Fixing Space Handling with Else Clause

**Definition:**  
Using an else clause to ensure encryption logic only runs for alphabet characters, preserving spaces in the encrypted text.

**Example:**
```python
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    if char == ' ':
        encrypted_text += char
    else:
        index = alphabet.find(char)
        new_index = index + shift
        encrypted_text += alphabet[new_index]
    print('char:', char, 'encrypted text:', encrypted_text)
```
```
char: h encrypted text: k
char: e encrypted text: kh
char: l encrypted text: kho
char: l encrypted text: khoo
char: o encrypted text: khoor
char:   encrypted text: khoor 
char: w encrypted text: khoor z
char: o encrypted text: khoor zr
char: r encrypted text: khoor zru
char: l encrypted text: khoor zruo
char: d encrypted text: khoor zruog
```
**Key Points:**
- Space bug fixed! Spaces now remain as spaces in encrypted text
- Encryption logic only runs for alphabet characters (else clause)
- Final print() call remains outside if/else to track progress
- "khoor zruog" = "hello world" encrypted with shift 3

---

## Step 44: Discovering the Edge Case

**Definition:**  
Testing the cipher with text containing 'z' reveals an index out of range error when shifting beyond the alphabet.

**Example:**
```python
text = 'Hello Zaira'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    if char == ' ':
        encrypted_text += char
    else:
        index = alphabet.find(char)
        new_index = index + shift
        encrypted_text += alphabet[new_index]
    print('char:', char, 'encrypted text:', encrypted_text)
```
```char: h encrypted text: k
char: e encrypted text: kh
char: l encrypted text: kho
char: l encrypted text: khoo
char: o encrypted text: khoor
char:   encrypted text: khoor 
Traceback (most recent call last):
  File "main.py", line 12, in <module>
    encrypted_text += alphabet[new_index]
IndexError: string index out of range
```
**Key Points:**
- Error occurs at 'z' → position 25 → 25+3=28 → alphabet[28] doesn't exist
- Alphabet only has positions 0-25 (26 letters)
- We need wrap-around logic (z → c)

---

## Step 45: Implementing Wrap-Around with Modulo

**Definition:**  
Using modulo operator `%` to handle letters at the end of the alphabet by wrapping around to the beginning.

**Example:**
```python
text = 'Hello Zaira'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    if char == ' ':
        encrypted_text += char
    else:
        index = alphabet.find(char)
        new_index = (index + shift) % 26
        encrypted_text += alphabet[new_index]
    print('char:', char, 'encrypted text:', encrypted_text)
```
```
char: h encrypted text: k
char: e encrypted text: kh
char: l encrypted text: kho
char: l encrypted text: khoo
char: o encrypted text: khoor
char:   encrypted text: khoor 
char: z encrypted text: khoor c
char: a encrypted text: khoor cd
char: i encrypted text: khoor cdl
char: r encrypted text: khoor cdlu
char: a encrypted text: khoor cdlud
```
**Key Points:**
- % 26 ensures result always stays between 0-25
- 'z' (25) → (25+3)%26 = 28%26 = 2 → 'c' ✅
- 'a' (0) → (0+3)%26 = 3%26 = 3 → 'd' ✅
- No more IndexError! Wrap-around working perfectly
- "Hello Zaira" → "khoor cdlud"

---

## Step 46: Dynamic Alphabet Length

**Definition:**  
Using `len(alphabet)` instead of hardcoded 26 to make the cipher flexible for different alphabet sizes.

**Example:**
```python
text = 'Hello Zaira'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    if char == ' ':
        encrypted_text += char
    else:
        index = alphabet.find(char)
        new_index = (index + shift) % len(alphabet)
        encrypted_text += alphabet[new_index]
    print('char:', char, 'encrypted text:', encrypted_text)
```
```
char: h encrypted text: k
char: e encrypted text: kh
char: l encrypted text: kho
char: l encrypted text: khoo
char: o encrypted text: khoor
char:   encrypted text: khoor 
char: z encrypted text: khoor c
char: a encrypted text: khoor cd
char: i encrypted text: khoor cdl
char: r encrypted text: khoor cdlu
char: a encrypted text: khoor cdlud
```
**Key Points:**
- % len(alphabet) instead of % 26
- More flexible - works if alphabet changes size
- Same output since len(alphabet) = 26
- Prepares for adding numbers/symbols later

---

## Step 47: Final Output Cleanup

**Definition:**  
Moving the print statement outside the loop to display only the final encrypted result.

**Example:**
```python
text = 'Hello Zaira'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    if char == ' ':
        encrypted_text += char
    else:
        index = alphabet.find(char)
        new_index = (index + shift) % len(alphabet)
        encrypted_text += alphabet[new_index]

print('encrypted text:', encrypted_text)
```
```
encrypted text: khoor cdlud
```
**Key Points:**
- Print statement now outside the for loop
- Shows only the final encrypted result
- Cleaner output without step-by-step debugging
- "Hello Zaira" → "khoor cdlud" (encrypted)

---

## Step 48: Displaying Original Text

**Definition:**  
Adding a print statement to show the original plain text alongside the encrypted result.

**Example:**
```python
text = 'Hello Zaira'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
encrypted_text = ''

for char in text.lower():
    if char == ' ':
        encrypted_text += char
    else:
        index = alphabet.find(char)
        new_index = (index + shift) % len(alphabet)
        encrypted_text += alphabet[new_index]

print('plain text:', text)
print('encrypted text:', encrypted_text)
```
```
plain text: Hello Zaira
encrypted text: khoor cdlud
```
**Key Points:**
- Shows both original and encrypted text for comparison
- Clear user interface - easy to see the transformation
- "Hello Zaira" → "khoor cdlud"
- Professional presentation of results

---

## Step 49: Function Definition

**Definition:**  
Wrapping the entire Caesar cipher logic inside a reusable function called `caesar()`.

**Example:**
```python
text = 'Hello Zaira'
shift = 3  

def caesar():
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in text.lower():
        if char == ' ':
            encrypted_text += char
        else:
            index = alphabet.find(char)
            new_index = (index + shift) % len(alphabet)
            encrypted_text += alphabet[new_index]
    
    print('plain text:', text)
    print('encrypted text:', encrypted_text)
```
**Key Points:**
- Entire encryption logic now inside caesar() function
- Function can be reused multiple times
- Not yet called - just defined
- All related code (variables, loops, prints) contained in function body
- Step toward modular, reusable code

---

## Step 50: Understanding Variable Scope

**Definition:**  
Learning about variable scope - where variables can be accessed in your code.

**Example:**
```python
text = 'Hello Zaira'
shift = 3

def caesar():
    alphabet = 'abcdefghijklmnopqrstuvwxyz'  # Local variable
    encrypted_text = ''                       # Local variable

    for char in text.lower():
        if char == ' ':
            encrypted_text += char
        else:
            index = alphabet.find(char)
            new_index = (index + shift) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', text)
    print('encrypted text:', encrypted_text)

print(alphabet)
```
```
Traceback (most recent call last):
  File "<main.py>", line 18, in <module>
NameError: name 'alphabet' is not defined
```
**Key Points:**
- Global variables: text, shift (defined outside functions)
- Local variables: alphabet, encrypted_text (defined inside function)
- Local variables cannot be accessed outside their function
- Global variables can be accessed anywhere
- This demonstrates function encapsulation

---

## Step 51: Fixing Scope Error

**Definition:**  
Removing the invalid print statement that tried to access a local variable from outside the function.

**Example:**
```python
text = 'Hello Zaira'
shift = 3

def caesar():
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in text.lower():
        if char == ' ':
            encrypted_text += char
        else:
            index = alphabet.find(char)
            new_index = (index + shift) % len(alphabet)
            encrypted_text += alphabet[new_index]
    
    print('plain text:', text)
    print('encrypted text:', encrypted_text)
```
**Key Points:**
- Removed print(alphabet) that caused NameError

---

## Step 52: Calling the Function

**Definition:**  
Executing the Caesar cipher function by calling it with parentheses `caesar()`.

**Example:**
```python
text = 'Hello Zaira'
shift = 3

def caesar():
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in text.lower():
        if char == ' ':
            encrypted_text += char
        else:
            index = alphabet.find(char)
            new_index = (index + shift) % len(alphabet)
            encrypted_text += alphabet[new_index]
    
    print('plain text:', text)
    print('encrypted text:', encrypted_text)
caesar()
```
```
plain text: Hello Zaira
encrypted text: khoor cdlud
```
**Key Points:**
- caesar() executes the function
- Function now actually runs and produces output
- Reusable - can call multiple times
- Encapsulated - all logic contained in function

---

## Step 53: Adding Function Parameters

**Definition:**  
Modifying the function to accept parameters, making it customizable and reusable for different inputs.

**Example:**
```python
text = 'Hello Zaira'
shift = 3

def caesar(message, offset):
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in text.lower():
        if char == ' ':
            encrypted_text += char
        else:
            index = alphabet.find(char)
            new_index = (index + shift) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', text)
    print('encrypted text:', encrypted_text)

caesar()
```
```
Traceback (most recent call last):
  File "<main.py>", line 17, in <module>
TypeError: caesar() missing 2 required positional arguments: 'message' and 'offset'
```
**Key Points:**
- Function now declares parameters (message, offset)
- Error occurs because function call doesn't provide arguments
- Parameters make function customizable
- Next step will fix the implementation

---

## Step 54: Renaming Variables to Match Parameters

**Definition:**  
Updating variable names inside the function to use the parameter names for consistency.

**Example:**
```python
message = 'Hello Zaira'
offset = 3

def caesar(message, offset):
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_message = ''

    for char in message.lower():
        if char == ' ':
            encrypted_message += char
        else:
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_message += alphabet[new_index]
    print('plain message:', message)
    print('encrypted message:', encrypted_message)

caesar()
```
```
Traceback (most recent call last):
  File "<main.py>", line 17, in <module>
TypeError: caesar() missing 2 required positional arguments: 'message' and 'offset'
```
**Key Points:**
- Renamed text → message and shift → offset inside function
- Still getting error - function call needs arguments
- Function now uses parameters internally
- External variables (message = 'Hello Zaira') are separate from parameters

---

## Step 55: Passing Arguments to Function

**Definition:**  
Calling the function with the required arguments to make it work properly.

**Example:**
```python
text = 'Hello Zaira'
shift = 3

def caesar(message, offset):
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        if char == ' ':
            encrypted_text += char
        else:
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', message)
    print('encrypted text:', encrypted_text)

caesar(text, shift)  # ← Added arguments
```
```
plain text: Hello Zaira
encrypted text: khoor cdlud
```
**Key Points:**
- Function call now includes arguments: caesar(text, shift)
- No more errors - function receives required parameters
- text variable passed as message parameter
- shift variable passed as offset parameter
- Fully reusable - can encrypt different texts with different shifts

---

# Step 56: Multiple Function Calls

**Definition:**  
Demonstrating function reusability by calling the Caesar cipher with different shift values.

**Example:**
```python
text = 'Hello Zaira'
shift = 3

def caesar(message, offset):
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        if char == ' ':
            encrypted_text += char
        else:
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', message)
    print('encrypted text:', encrypted_text)

caesar(text, shift)
caesar(text, 13)  # ← Second call with different shift
```
```
plain text: Hello Zaira
encrypted text: khoor cdlud
plain text: Hello Zaira
encrypted text: uryyb mnven
```
**Key Points:**
- Same function, different results: shift 3 vs shift 13
- Shift 3: "Hello Zaira" → "khoor cdlud"
- Shift 13: "Hello Zaira" → "uryyb mnven" (ROT13 cipher)
- Proves reusability - one function handles multiple encryption needs
- ROT13 is a special case where encryption = decryption

---


