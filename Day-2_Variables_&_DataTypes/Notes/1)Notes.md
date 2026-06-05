# Day 2: Variables and Data Types

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

* What variables are
* How to store data in variables
* Integer data type (`int`)
* Float data type (`float`)
* String data type (`str`)
* Boolean data type (`bool`)
* Type conversion between data types

---

# 1. Introduction to Variables

A variable is a named storage location used to store data in memory.

Think of a variable as a labeled box that contains information.

## Syntax

```python
variable_name = value
```

## Example

```python
name = "Karthik"
age = 20

print(name)
print(age)
```

### Output

```
Karthik
20
```

---

# Why Use Variables?

Without variables:

```python
print("Karthik")
print(20)
```

With variables:

```python
name = "Karthik"
age = 20

print(name)
print(age)
```

Variables make programs easier to read, modify, and maintain.

---

# Variable Naming Rules

## Valid Names

```python
name = "Karthik"
student_age = 20
age2 = 20
_marks = 95
```

## Invalid Names

```python
age = 20
student age = 20
class = "Python"
```

### Rules

* Must start with a letter or underscore
* Cannot start with a number
* Cannot contain spaces
* Cannot use Python keywords
* Case-sensitive

```python
age = 20
Age = 30

print(age)
print(Age)
```

Output:

```
20
30
```

---

# 2. Integer Data Type (int)

Integers are whole numbers without decimal points.

## Examples

```python
age = 20
marks = 95
temperature = -10
population = 1400000000
```

## Checking Data Type

```python
age = 20

print(type(age))
```

Output:

```python
<class 'int'>
```

---

# Integer Operations

```python
a = 10
b = 5

print(a + b)
print(a - b)
print(a * b)
print(a / b)
```

Output:

```
15
5
50
2.0
```

---

# 3. Float Data Type (float)

Floats are numbers containing decimal points.

## Examples

```python
height = 5.8
price = 99.99
pi = 3.14159
```

## Checking Data Type

```python
price = 99.99

print(type(price))
```

Output:

```python
<class 'float'>
```

---

# Float Operations

```python
a = 5.5
b = 2.5

print(a + b)
print(a - b)
print(a * b)
```

Output:

```
8.0
3.0
13.75
```

---

# Difference Between int and float

| Integer | Float |
| ------- | ----- |
| 10      | 10.0  |
| 25      | 25.75 |
| -5      | -5.5  |

---

# 4. String Data Type (str)

Strings are sequences of characters enclosed in quotes.

## Examples

```python
name = "Karthik"
college = 'ABC College'
course = "Python Programming"
```

## Checking Type

```python
name = "Python"

print(type(name))
```

Output:

```python
<class 'str'>
```

---

# String Concatenation

Combining two strings.

```python
first_name = "Karthik"
last_name = "N"

full_name = first_name + " " + last_name

print(full_name)
```

Output:

```
Karthik N
```

---

# String Repetition

```python
print("Python " * 3)
```

Output:

```
Python Python Python
```

---

# String Indexing

```python
word = "Python"

print(word[0])
print(word[1])
```

Output:

```
P
y
```

---

# String Length

```python
word = "Python"

print(len(word))
```

Output:

```
6
```

---

# 5. Boolean Data Type (bool)

Boolean values represent truth values.

There are only two values:

```python
True
False
```

## Examples

```python
is_student = True
is_logged_in = False
```

## Checking Type

```python
print(type(is_student))
```

Output:

```python
<class 'bool'>
```

---

# Boolean Expressions

```python
print(10 > 5)
print(10 < 5)
```

Output:

```
True
False
```

---

# Real-Life Boolean Example

```python
age = 20

is_eligible = age >= 18

print(is_eligible)
```

Output:

```
True
```

---

# 6. Type Conversion

Type conversion means changing one data type into another.

Python provides built-in conversion functions.

| Function | Purpose            |
| -------- | ------------------ |
| int()    | Convert to integer |
| float()  | Convert to float   |
| str()    | Convert to string  |
| bool()   | Convert to boolean |

---

# Integer to Float

```python
age = 20

new_age = float(age)

print(new_age)
print(type(new_age))
```

Output:

```
20.0
<class 'float'>
```

---

# Float to Integer

```python
price = 99.99

new_price = int(price)

print(new_price)
```

Output:

```
99
```

Note:

The decimal part is removed.

---

# Integer to String

```python
age = 20

text = str(age)

print(text)
print(type(text))
```

Output:

```
20
<class 'str'>
```

---

# String to Integer

```python
number = "100"

value = int(number)

print(value + 50)
```

Output:

```
150
```

---

# String to Float

```python
price = "99.99"

value = float(price)

print(value)
```

Output:

```
99.99
```

---

# Boolean Conversion

```python
print(bool(1))
print(bool(0))
```

Output:

```
True
False
```

---

# Common Beginner Mistakes

## Mistake 1

```python
age = 20

print("Age: " + age)
```

Output:

```
TypeError
```

Correct:

```python
print("Age: " + str(age))
```

---

## Mistake 2

```python
num = "10"

print(num + 5)
```

Output:

```
TypeError
```

Correct:

```python
print(int(num) + 5)
```

---

# Summary

## Data Types Learned

| Type  | Example  |
| ----- | -------- |
| int   | 20       |
| float | 5.8      |
| str   | "Python" |
| bool  | True     |

## Conversion Functions

```python
int()
float()
str()
bool()
```

## Key Concepts

✅ Variables store data

✅ Python is dynamically typed

✅ Four basic data types:

* Integer
* Float
* String
* Boolean

✅ Type conversion allows changing data types

✅ Variables make programs reusable and maintainable

