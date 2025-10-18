# Python Basics

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
shift = 3
```
---

## Step 10: Printing Variables

**Definition:**  
Using the `print()` function to display the value stored in a variable.

**Example:**
```python
shift = 3
print(shift)   # Output: 3
```
---

## Checking Data Types

**Definition:**  
Using `type()` inside `print()` to display a variable's data type.

**Example:**
```python
shift = 3
print(type(shift))   # Output: <class 'int'>
```
---

## Step 12: Variable Assignment & Naming Rules

**Definition:**  
Creating a variable to store the alphabet string, following Python's naming conventions.

**Example:**
```python
alphabet = 'abcdefghijklmnopqrstuvwxyz'
```
**Key Points:**
- Variable names cannot use reserved keywords (for, while, True, etc.)
- Cannot start with numbers (2alphabet ❌)
- Only alphanumeric characters and underscores allowed
- Case-sensitive (alphabet ≠ Alphabet)
- Use snake_case convention (user_name not userName)
