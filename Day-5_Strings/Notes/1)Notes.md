# Day 5: Strings in Python

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

* What strings are
* Creating strings
* String Indexing
* String Slicing
* Common String Methods
* String Formatting
* Real-world string examples

---

# 1. What is a String?

A string is a sequence of characters enclosed in quotes.

Examples:

```python
name = "Karthik"
course = 'Python'
message = "Hello World"
```

---

# Why Strings Matter

Strings are used everywhere:

* Names
* Emails
* Passwords
* Messages
* File names
* URLs

Example:

```python
name = "Karthik"

print("Welcome", name)
```

Output:

```text
Welcome Karthik
```

---

# 2. Creating Strings

Using double quotes:

```python
language = "Python"
```

Using single quotes:

```python
language = 'Python'
```

Both are valid.

---

# Multi-Line Strings

```python
message = """
Welcome to
30 Days of Python
"""
```

Output:

```text
Welcome to
30 Days of Python
```

---

# 3. String Length

Use `len()` to find the number of characters.

```python
word = "Python"

print(len(word))
```

Output:

```text
6
```

---

# 4. String Indexing

Each character has a position called an index.

```text
P  y  t  h  o  n
0  1  2  3  4  5
```

---

## Accessing Characters

```python
word = "Python"

print(word[0])
print(word[1])
print(word[5])
```

Output:

```text
P
y
n
```

---

# Negative Indexing

Python can count from the end.

```text
P  y  t  h  o  n
-6 -5 -4 -3 -2 -1
```

Example:

```python
word = "Python"

print(word[-1])
print(word[-2])
```

Output:

```text
n
o
```

---

# 5. String Slicing

Slicing extracts part of a string.

## Syntax

```python
string[start:end]
```

* Start is included
* End is excluded

---

## Example

```python
word = "Python"

print(word[0:3])
```

Output:

```text
Pyt
```

---

## More Examples

```python
word = "Python"

print(word[0:2])
print(word[2:5])
print(word[1:4])
```

Output:

```text
Py
tho
yth
```

---

## Omitting Start

```python
word = "Python"

print(word[:4])
```

Output:

```text
Pyth
```

---

## Omitting End

```python
word = "Python"

print(word[2:])
```

Output:

```text
thon
```

---

## Copy Entire String

```python
word = "Python"

print(word[:])
```

Output:

```text
Python
```

---

# Step Slicing

Syntax:

```python
string[start:end:step]
```

---

## Every Second Character

```python
word = "Python"

print(word[::2])
```

Output:

```text
Pto
```

---

## Reverse a String

```python
word = "Python"

print(word[::-1])
```

Output:

```text
nohtyP
```

---

# 6. String Methods

Methods are built-in functions that work on strings.

---

## upper()

Converts to uppercase.

```python
name = "karthik"

print(name.upper())
```

Output:

```text
KARTHIK
```

---

## lower()

Converts to lowercase.

```python
name = "KARTHIK"

print(name.lower())
```

Output:

```text
karthik
```

---

## capitalize()

Capitalizes first character.

```python
name = "python"

print(name.capitalize())
```

Output:

```text
Python
```

---

## title()

Capitalizes every word.

```python
text = "python programming"

print(text.title())
```

Output:

```text
Python Programming
```

---

## strip()

Removes leading and trailing spaces.

```python
name = "   Python   "

print(name.strip())
```

Output:

```text
Python
```

---

## replace()

Replaces characters or words.

```python
text = "I love Java"

print(text.replace("Java", "Python"))
```

Output:

```text
I love Python
```

---

## find()

Returns position of first occurrence.

```python
word = "Python"

print(word.find("t"))
```

Output:

```text
2
```

---

## count()

Counts occurrences.

```python
word = "banana"

print(word.count("a"))
```

Output:

```text
3
```

---

## startswith()

Checks beginning of string.

```python
filename = "notes.pdf"

print(filename.startswith("notes"))
```

Output:

```text
True
```

---

## endswith()

Checks ending of string.

```python
filename = "notes.pdf"

print(filename.endswith(".pdf"))
```

Output:

```text
True
```

---

# 7. String Formatting

Formatting helps create readable output.

---

## Method 1: Using Comma

```python
name = "Karthik"

print("Hello", name)
```

Output:

```text
Hello Karthik
```

---

## Method 2: Using + Operator

```python
name = "Karthik"

print("Hello " + name)
```

Output:

```text
Hello Karthik
```

---

## Method 3: f-Strings (Recommended)

```python
name = "Karthik"
age = 20

print(f"My name is {name} and I am {age} years old.")
```

Output:

```text
My name is Karthik and I am 20 years old.
```

---

# Why f-Strings?

Cleaner and easier to read.

Instead of:

```python
name = "Karthik"
age = 20

print("My name is " + name + " and I am " + str(age))
```

Use:

```python
print(f"My name is {name} and I am {age}")
```

---

### Key Takeaways

✅ Strings are sequences of characters enclosed in quotes.

✅ Indexing is used to access individual characters.

✅ Negative indexing accesses characters from the end.

✅ Slicing extracts portions of a string.

✅ Step slicing can skip characters or reverse strings.

✅ String methods simplify common text operations.

✅ `len()` returns the length of a string.

✅ `upper()`, `lower()`, `replace()`, `find()`, and `count()` are frequently used methods.

✅ f-Strings provide the most readable way to format strings.

✅ String manipulation is one of the most important skills in Python programming.

---

