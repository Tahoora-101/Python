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

## Step 56: Multiple Function Calls

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
- ROT13 (Rotate by 13 places) is a special case where encryption = decryption

---

## Step 57: Preparing for Vigenère Cipher

**Definition:**  
Removing function calls to prepare for upgrading from Caesar cipher to Vigenère cipher.

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

## Function calls removed - ready for Vigenère upgrade
```
**Key Points:**
- Caesar cipher: Same shift for every letter (less secure)
- Vigenère cipher: Different shift for each letter (more secure)
- Key: Determines the shifting pattern
- Preparing to implement more complex encryption
- Function remains defined but not called

---

## Step 58: Transitioning to Vigenère Cipher

**Definition:**  
Renaming the function and parameters to reflect the shift from Caesar cipher to Vigenère cipher.

**Example:**
```python
text = 'Hello Zaira'
shift = 3

def vigenere(message, key):
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
```
**Key Points:**
- Function name changed: caesar → vigenere
- Parameter changed: offset → key
- Key difference: Caesar uses number, Vigenère uses text key
- Current code still Caesar logic - needs Vigenère implementation
- Bug: offset variable not defined (should be using key)

---

## Step 59: Setting Up Vigenère Key

**Definition:**  
Replacing the numeric shift with a text key for Vigenère cipher implementation.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
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
```
**Key Points:**
- Deleted: shift = 3 (Caesar-style fixed shift)
- Added: custom_key = 'python' (Vigenère text key)
- Key purpose: Determines variable shifts for each letter
- Current state: Still using Caesar logic with undefined offset

---

## Step 60: Initializing Key Index for Vigenère

**Definition:**  
Setting up a key index to track position in the key for Vigenère cipher's polyalphabetic substitution.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
    key_index = 0
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
```
**Key Points:**
Key Points:
- key_index = 0 - tracks current position in the key
- Purpose: Key repeats for long messages ("pythonpythonpython...")
- Vigenère logic: Each letter uses different shift based on key character
- Still using old logic - will replace offset with key-based shifting
- Key index will increment for each character (except spaces)
- Next step: Will implement Vigenère shifting using the key

---

## Step 61: Adding Code Comments

**Definition:**  
Using comments to document code logic and improve readability.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', message)
    print('encrypted text:', encrypted_text)
```

---

## Step 62: Accessing Key Characters

**Definition:**  
Getting the current key character for Vigenère encryption using modulo to handle key repetition.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            key_char = key[key_index % len(key)]
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', message)
    print('encrypted text:', encrypted_text)
```
**Key Points:**
- **key_char = key[key_index % len(key)]** - gets current key character
- **Modulo ensures key repeats**: "pythonpythonpython..."
- **Example**: For key="python", positions cycle: 0→p, 1→y, 2→t, 3→h, 4→o, 5→n, 6→p, 7→y, etc.
- **Still using old logic** - will replace offset with key_char-based shift
- **Key index not incrementing yet** - next step

---

## Step 63: Incrementing Key Index

**Definition:**  
Increasing the key index to move to the next key character for each letter in the message.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            key_char = key[key_index % len(key)]
            key_index += 1
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', message)
    print('encrypted text:', encrypted_text)
```
**Key Points:**
- **key_index += 1** - moves to next key character
- **Ensures each letter** gets a different shift amount
- **Key cycles**: p→y→t→h→o→n→p→y→t→h...
- **Still using old Caesar logic** - offset not defined
- **Next step**: Replace offset with key-based shifting

---

## Step 64: Adding Encryption Comment

**Definition:**  
Documenting the key character selection process for Vigenère encryption.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            # Find the right key character to encode
            key_char = key[key_index % len(key)]
            key_index += 1
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', message)
    print('encrypted text:', encrypted_text)
```
**Key Points:**
- Comment explains the purpose of key character selection
- Documents Vigenère logic: each letter uses different key character
- Improves code readability for complex algorithm
- Still has bug - offset not defined (should use key_char)

---

## Step 65: Converting Key Character to Shift Amount

**Definition:**  
Using `.index()` method to convert key characters into numeric shift values for Vigenère encryption.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            # Find the right key character to encode
            key_char = key[key_index % len(key)]
            key_index += 1
            index = alphabet.find(char)
            offset = alphabet.index(key_char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', message)
    print('encrypted text:', encrypted_text)
```
**Key Points:**
- offset = alphabet.index(key_char) - converts key character to shift amount
- .index() vs .find(): Both find positions, but .index() raises ValueError if not found
- Example: key_char='p' → offset=15, key_char='y' → offset=24
- Now using actual Vigenère logic - different shift for each letter
- fixed - offset now properly defined

---

## Step 66: Adding Documentation for Encryption Logic

**Definition:**  
Adding comments to document the offset calculation and encrypted letter generation process.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            # Find the right key character to encode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    print('plain text:', message)
    print('encrypted text:', encrypted_text)
```
**Key Points:**
- Comment documents the core Vigenère calculation steps
- Offset: Numeric value from key character position
- Encrypted letter: Result of shifting by offset
- Clear documentation of the polyalphabetic process
- Code is now fully functional Vigenère cipher

---

## Step 67: Returning Encrypted Text

**Definition:**  
Modifying the function to return the encrypted text instead of printing it, making the function reusable.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            # Find the right key character to encode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    
    return encrypted_text
```
**Key Points:**
- Removed print statements - no longer just displaying results
- Added return encrypted_text - function now returns the encrypted value
- Makes function reusable - output can be stored, processed, or used elsewhere
- Professional coding practice - functions should return values, not just print
- Vigenère cipher is now complete and reusable

---

## Step 68: Calling the Vigenère Function

**Definition:**  
Executing the Vigenère cipher function and storing the encrypted result in a variable.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            # Find the right key character to encode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    
    return encrypted_text

encryption = vigenere(text, custom_key)
```
**Key Points:**
- Function call: vigenere(text, custom_key) executes the encryption
- Store result: encryption = captures the returned value
- Reusable: Can now use encryption variable elsewhere in code
- Professional workflow: Define function → Call function → Use result
- Vigenère cipher is now fully operational ✅

---

## Step 69: Displaying Encrypted Output

**Definition:**  
Printing the encrypted result to see the Vigenère cipher in action.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            # Find the right key character to encode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    
    return encrypted_text

encryption = vigenere(text, custom_key)
print(encryption)
```
```
wcseg odfyp
```
**Key Points:**
- First visible output of Vigenère encryption
- "Hello Zaira" → "wcseg odfyp" (encrypted with key "python")
- Verifies cipher is working correctly
- Shows polyalphabetic nature - different letters transform differently
- Complete encryption pipeline: input → process → store → output ✅

---

## Step 70: Preparing for Encryption & Decryption

**Definition:**  
Adding a direction parameter to enable both encryption and decryption in the same function.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key, direction):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            # Find the right key character to encode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset) % len(alphabet)
            encrypted_text += alphabet[new_index]
    
    return encrypted_text

#encryption = vigenere(text, custom_key)
#print(encryption)
```
**Key Points:**
- Added direction parameter - will control encrypt vs decrypt
- Commented out function call - temporary to avoid errors
- Preparation for two-way cipher - same function handles both operations
- Next step: Implement direction logic (add vs subtract offset)
- Professional design - single function for related operations

---

## Step 71: Implementing Two-Way Encryption

**Definition:**  
Adding direction control to enable both encryption and decryption by multiplying offset by direction.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key, direction):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            # Find the right key character to encode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            encrypted_text += alphabet[new_index]
    
    return encrypted_text

#encryption = vigenere(text, custom_key)
#print(encryption)
```
**Key Points:**
- offset * direction - enables two-way operation
- direction = 1: index + offset (encryption)
- direction = -1: index - offset (decryption)
- Same function handles both encryption and decryption
- Mathematical elegance - simple multiplication changes operation
- Ready for testing with different direction values

---

## Step 72: Testing Encryption with Direction Parameter

**Definition:**  
Activating the encryption function with direction=1 to test the two-way Vigenère cipher.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key, direction):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            # Find the right key character to encode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            encrypted_text += alphabet[new_index]
    
    return encrypted_text

encryption = vigenere(text, custom_key, 1)
print(encryption)
```
```
wcseg odfyp
```
**Key Points:**
- Uncommented function call - reactivated the encryption pipeline
- Added direction=1 - specifies encryption mode
- Same output as before - confirms encryption works correctly with new parameter
- "Hello Zaira" → "wcseg odfyp" - Vigenère encryption with key "python"
- Ready for decryption test - next step will use direction=-1

---

## Step 73: Testing Decryption with Direction Parameter

**Definition:**  
Testing the decryption capability by using direction=-1 to reverse the encryption process.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key, direction):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    encrypted_text = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            encrypted_text += char
        else:
            # Find the right key character to encode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            encrypted_text += alphabet[new_index]
    
    return encrypted_text

encryption = vigenere(text, custom_key, 1)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption
```
```
wcseg odfyp
hello zaira
```
**Key Points:**
- decryption = vigenere(encryption, custom_key, -1) - uses direction=-1 for decryption
- Full cycle: "Hello Zaira" → "wcseg odfyp" → "hello zaira"
- Proves two-way functionality - same function handles both operations
- Mathematical verification - encryption and decryption are perfect inverses
- Complete Vigenère cipher system ✅

---

## Step 75-76: Complete Code Cleanup

**Definition:**  
Updating both variable names and comments to reflect the function's dual encryption/decryption capability.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key, direction):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

encryption = vigenere(text, custom_key, 1)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption)
```
```
wcseg odfyp
hello zaira
```
**Key Points:**
- Variable name: encrypted_text → final_message (works for both operations)
- Comment updates: "encode" → "encode/decode", "encrypted" → "encrypted/decrypted"
- Accurate documentation - reflects the function's true dual purpose
- Professional standards - clear, honest code documentation
- Maintains full functionality - encryption/decryption still works perfectly
  
---

## Step 77: Adding Default Parameter Value

**Definition:**  
Setting a default value for the direction parameter to make the function more user-friendly.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

encryption = vigenere(text, custom_key, 1)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption)
```
**Key Points:**
- direction=1 - sets default value for encryption
- Backward compatible - existing code still works
- User-friendly - can call vigenere(text, key) without specifying direction
- Professional API design - sensible defaults improve usability
- Default assumes encryption - most common use case

---

## Step 78: Testing Default Parameter

**Definition:**  
Verifying that the default direction parameter works by calling the function without the third argument.

**Example:**
```python
text = 'Hello Zaira'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

encryption = vigenere(text, custom_key)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption)
```
```
wcseg odfyp
hello zaira
```
**Key Points:**
- Removed direction argument from first call: vigenere(text, custom_key)
- Default value works - automatically uses direction=1 for encryption
- Same output - confirms default parameter functions correctly
- Cleaner API - simpler function calls for common use case
- Flexible design - can still specify direction when needed for decryption

---

## Step 79: Testing with Special Characters

**Definition:**  
Testing the Vigenère cipher with punctuation to identify handling of non-alphabet characters.

**Example:**
```python
text = 'Hello Zaira!'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append space to the message
        if char == ' ':
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

encryption = vigenere(text, custom_key)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption)
```
```
wcesc mpgkhn
hello zairaz
```
**Key Points:**
- Input: "Hello Zaira!" (with exclamation mark)
- Encrypted: "wcesc mpgkhn" (corrupted - should be "wcseg odfyp")
- Decrypted: "hello zairaz" (extra 'z' and missing '!')
- Problem: Non-alphabet characters break the encryption
- Root cause: alphabet.find('!') returns -1, causing incorrect shifts
- Key synchronization lost: Exclamation mark consumes a key character but isn't encrypted properly

---

## Step 80: Testing .isalpha() Method

**Definition:**  
Replacing space-specific checking with `.isalpha()` method to handle all letter characters.

**Example:**
```python
text = 'Hello Zaira!'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append space to the message
        if char.isalpha():
            final_message += char
        else:        
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

encryption = vigenere(text, custom_key)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption)
```
```
helloozairax
helloozairax
```
**Key Points:**
- Using .isalpha() instead of char == ' '
- Current logic: Letters copied directly, non-letters encrypted
- Result: Corruption observed - demonstrates importance of correct logic
- Learning opportunity: Shows how small logic errors break cryptography

---

## Step 81: Using NOT Operator for Character Handling

**Definition:**  
Using the `not` operator to properly handle non-alphabetic characters by negating the `.isalpha()` condition.

**Example:**
```python
text = 'Hello Zaira!'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append space to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

encryption = vigenere(text, custom_key)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption)
```
wcseg odfyp!
hello zaira!
```
**Key Points:**
- not char.isalpha() - correctly identifies non-letter characters
- Proper logic: Non-letters copied directly, letters encrypted
- Clean output: "Hello Zaira!" → "wcseg odfyp!" → "hello zaira!"
- Exclamation preserved: Special characters handled correctly
- Full cycle working: Encryption and decryption complete successfully

----

## Step 82: Updating Comment for Accuracy

**Definition:**  
Correcting the comment to accurately describe the handling of non-letter characters in the cipher.

**Example:**
```python
text = 'Hello Zaira!'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

encryption = vigenere(text, custom_key)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption)
```
```
wcseg odfyp!
hello zaira!
```
**Key Points**:
- Updated comment: "Append any non-letter character to the message"
- Accurate documentation: Reflects the actual logic using .isalpha()
- Comprehensive handling: Spaces, punctuation, numbers, symbols all preserved
- Professional code quality: Clear, honest comments that match the code
- Maintains full functionality: Encryption/decryption still works perfectly

---

## Step 83: Creating Encryption Wrapper Function

**Definition:**  
Creating a dedicated `encrypt` function as a wrapper for the Vigenère cipher to provide a cleaner interface.

**Example:**
```python
text = 'Hello Zaira!'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    pass

encryption = vigenere(text, custom_key)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption)
```
**Key Points:**
- Created encrypt() function - dedicated wrapper for encryption
- Used pass keyword - placeholder for future implementation
- Cleaner API design - separates encryption from core Vigenère logic
- User-friendly interface - encrypt(message, key) is more intuitive
- Preparation for decryption function - sets pattern for symmetric design

---

## Step 84: Implementing Encryption Wrapper Function

**Definition:**  
Completing the `encrypt` wrapper function by calling the main Vigenère function with the correct parameters.

**Example:**
```python
text = 'Hello Zaira!'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)

encryption = vigenere(text, custom_key)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption)
```
**Key Points:**
- Replaced pass with implementation - function now actually works
- encrypt() calls vigenere() - wrapper function with direction=1 (default)
- Cleaner user interface - encrypt(message, key) vs vigenere(message, key, 1)
- Professional library design - separation of core logic and user API
- Maintains functionality - same output as before

---

## Step 85: Creating Decryption Wrapper Function

**Definition:**  
Creating a dedicated `decrypt` function as a symmetric counterpart to the `encrypt` function for a complete API.

**Example:**
```python
text = 'Hello Zaira!'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)

def decrypt(message, key):
    return vigenere(message, key, -1)

encryption = vigenere(text, custom_key)
print(encryption)

decryption = vigenere(encryption, custom_key, -1)
print(decryption)
```
**Key Points:**
- Created decrypt() function - symmetric counterpart to encrypt()
- Calls vigenere with direction=-1 - specifies decryption mode
- Complete API - both encrypt and decrypt functions available
- Clean user interface - intuitive function names, no magic numbers
- Professional library structure - core function + user-friendly wrappers

---

## Step 86: Using the Clean API

**Definition:**  
Testing the new user-friendly API by calling the wrapper functions instead of the core Vigenère function directly.

**Example:**
```python
text = 'Hello Zaira!'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)
    
def decrypt(message, key):
    return vigenere(message, key, -1)
    
encryption = encrypt(text, custom_key)
print(encryption)

decryption = decrypt(encryption, custom_key)
print(decryption)
```
```
wcseg odfyp!
hello zaira!
```
**Key Points:**
- encryption = encrypt(text, custom_key) - clean encryption call
- decryption = decrypt(encryption, custom_key) - clean decryption call (no -1 needed!)
- Self-documenting code - function names clearly indicate purpose
- Professional API usage - hiding implementation details from users
- Same perfect results - full encryption/decryption cycle works flawlessly

---

## Step 87: Testing with Pre-Encrypted Message

**Definition:**  
Testing the decryption functionality with a pre-encrypted message to verify the cipher works with external data.

**Example:**
```python
text = 'mrttaqrhknsw ih puggrur'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)
    
def decrypt(message, key):
    return vigenere(message, key, -1)
    
encryption = encrypt(text, custom_key)
print(encryption)

decryption = decrypt(encryption, custom_key)
print(decryption)
```
```
bpmaodgfdugj xf ibutgsk
mrttaqrhknsw ih puggrur
```
**Key Points:**
- New encrypted input: 'mrttaqrhknsw ih puggrur'
- Double encryption: Input gets encrypted → 'bpmaodgfdugj xf ibutgsk'
- Successful decryption: Returns to original → 'mrttaqrhknsw ih puggrur'
- Verifies external data handling: Works with pre-encrypted messages
- Confirms algorithm correctness: Full cycle preserves original data

---

## Step 88: Cleaning Up for Final Decryption

**Definition:**  
Removing unnecessary code to focus on decrypting the pre-encrypted message and discovering its original content.

**Example:**
```python
text = 'mrttaqrhknsw ih puggrur'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)
    
def decrypt(message, key):
    return vigenere(message, key, -1)

#decryption = decrypt(encryption, custom_key)
#print(decryption)
```
**Key Points:**
- Removed encryption variable - not needed for decryption-only task
- Commented out last lines - temporary cleanup
- Focus on decryption - preparing to reveal the secret message
- Clean code structure - ready for the final reveal
- Mystery message: 'mrttaqrhknsw ih puggrur' awaits decryption

---

## Step 89: Displaying Encrypted Text with Label

**Definition:**  
Using string concatenation to display the encrypted text with a descriptive label for better output presentation.

**Example:**
```python
text = 'mrttaqrhknsw ih puggrur'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)
    
def decrypt(message, key):
    return vigenere(message, key, -1)

print('Encrypted text: ' + text)
#decryption = decrypt(encryption, custom_key)
#print(decryption)
```
```
Encrypted text: mrttaqrhknsw ih puggrur
```
**Key Points:**
- String concatenation: 'Encrypted text: ' + text
- Clear labeling: Identifies the encrypted message
- Professional output: Well-formatted display
- Preparation for reveal: Sets up the mystery before decryption
- Maintains suspense: Shows what we're about to decrypt

---

## Step 90: Displaying Encryption Key

**Definition:**  
Adding a second print statement to display the encryption key being used, providing complete context for the decryption process.

**Example:**
```python
text = 'mrttaqrhknsw ih puggrur'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)
    
def decrypt(message, key):
    return vigenere(message, key, -1)

print('Encrypted text: ' + text)
print('Key: ' + custom_key)
#decryption = decrypt(encryption, custom_key)
#print(decryption)
```
```
Encrypted text: mrttaqrhknsw ih puggrur
Key: python
```
**Key Points:**
- Complete context: Shows both encrypted text and decryption key
- String concatenation: 'Key: ' + custom_key
- Professional presentation: Clear, labeled output
- Cryptographic transparency: Important to know both ciphertext and key
- Sets stage for final reveal: All pieces are in place for decryption

---

## Step 91-92: Converting Both Prints to f-strings

**Definition:**  
Modernizing all string outputs by converting both print statements to use f-strings for consistent, clean code.

**Example:**
```python
text = 'mrttaqrhknsw ih puggrur'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)
    
def decrypt(message, key):
    return vigenere(message, key, -1)

print(f'Encrypted text: {text}')
print(f'Key: {custom_key}')
#decryption = decrypt(encryption, custom_key)
#print(decryption)
```
```
Encrypted text: mrttaqrhknsw ih puggrur
Key: python
```
**Key Points:**
- Both prints use f-strings - consistent modern formatting
- Clean, readable code - no string concatenation clutter
- Professional standards - using Python's preferred string method
- Same clear output - functionality unchanged
- Ready for final step - clean codebase for the big reveal

---

## Step 93: Adding Newline Character

**Definition:**  
Using the newline character `\n` to create better formatted output by adding blank lines.

**Example:**
```python
text = 'mrttaqrhknsw ih puggrur'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)
    
def decrypt(message, key):
    return vigenere(message, key, -1)

print(f'\nEncrypted text: {text}')
print(f'Key: {custom_key}')
#decryption = decrypt(encryption, custom_key)
#print(decryption)
```
```

Encrypted text: mrttaqrhknsw ih puggrur
Key: python
```
**Key Points:**
- \n at string start: Creates a blank line before the output
- Better formatting: Separates program output from command line
- Escape character: \n is interpreted as newline, not literal text
- Professional presentation: Clean, spaced output for better readability
- Common practice: Used to format multi-line console output

---

## Step 94: Preparing for Final Decryption

**Definition:**  
Uncommenting and modifying the decryption variable to decrypt the original encrypted text directly.

**Example:**
```python
text = 'mrttaqrhknsw ih puggrur'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)
    
def decrypt(message, key):
    return vigenere(message, key, -1)

print(f'\nEncrypted text: {text}')
print(f'Key: {custom_key}')
decryption = decrypt(text, custom_key)
#print(decryption)
```
**Key Points:**
- Uncommented decryption variable - reactivated the decryption process
- decrypt(text, custom_key) - decrypts the original encrypted message
- Direct decryption - no double encryption, goes straight to revealing the secret
- Final preparation - ready to display the decrypted message
- Mystery almost solved - the secret message is calculated and stored

---

## Step 95: Final Output with Actual Results

**Definition:**  
Displaying the complete encryption-decryption cycle with the actual decrypted output.

**Example:**
```python
text = 'mrttaqrhknsw ih puggrur'
custom_key = 'python'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)
    
def decrypt(message, key):
    return vigenere(message, key, -1)

print(f'\nEncrypted text: {text}')
print(f'Key: {custom_key}')
decryption = decrypt(text, custom_key)
print(f'\nDecrypted text: {decryption}\n')
```
```

Encrypted text: mrttaqrhknsw ih puggrur
Key: python

Decrypted text: xtammdcjrgej tj wnstcwy
```
**Key Points:**
- Mathematically consistent: Algorithm produces deterministic output
- Professional formatting: Clean, spaced output with labels
- Cryptographic verification: Demonstrates the cipher works end-to-end

---

## Step 96: Testing with Correct Key - PROJECT COMPLETE!

**Definition:**  
Using the correct decryption key 'happycoding' to successfully reveal the original secret message.

**Example:**
```python
text = 'mrttaqrhknsw ih puggrur'
custom_key = 'happycoding'

def vigenere(message, key, direction=1):
    key_index = 0
    alphabet = 'abcdefghijklmnopqrstuvwxyz'
    final_message = ''

    for char in message.lower():
        # Append any non-letter character to the message
        if not char.isalpha():
            final_message += char
        else:
            # Find the right key character to encode/decode
            key_char = key[key_index % len(key)]
            key_index += 1
            # Define the offset and the encrypted/decrypted letter
            offset = alphabet.index(key_char)
            index = alphabet.find(char)
            new_index = (index + offset * direction) % len(alphabet)
            final_message += alphabet[new_index]
    
    return final_message

def encrypt(message, key):
    return vigenere(message, key)
    
def decrypt(message, key):
    return vigenere(message, key, -1)

print(f'\nEncrypted text: {text}')
print(f'Key: {custom_key}')
decryption = decrypt(text, custom_key)
print(f'\nDecrypted text: {decryption}\n')
```
```
Encrypted text: mrttaqrhknsw ih puggrur
Key: happycoding

Decrypted text: freecodecamp is awesome
```
**Key Points:**
- Correct key: 'happycoding' instead of 'python'
- Successful decryption: "mrttaqrhknsw ih puggrur" → "freecodecamp is awesome"
- Key security demonstrated: Wrong key = gibberish, correct key = meaningful message
- Cryptographic principle proven: Encryption security depends entirely on key secrecy
- PROJECT COMPLETED: All 96 steps successfully implemented! 🎉

---
