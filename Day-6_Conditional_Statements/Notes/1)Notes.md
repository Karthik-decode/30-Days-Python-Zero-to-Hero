# Day 6: Conditional Statements in Python

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

* Why conditional statements are needed
* The `if` statement
* The `if-else` statement
* The `if-elif-else` ladder
* Nested Conditions
* Real-world decision-making programs
* Grade Calculator Project

---

# 1. Introduction to Conditional Statements

In real life, we make decisions based on conditions.

Examples:

* If it rains, take an umbrella.
* If marks are above 35, pass.
* If age is 18 or above, eligible to vote.

Similarly, Python uses conditional statements to make decisions.

---

# 2. The if Statement

The `if` statement executes a block of code only when a condition is True.

## Syntax

```python
if condition:
    # code
```

---

## Example

```python
age = 20

if age >= 18:
    print("Eligible to vote")
```

Output:

```text
Eligible to vote
```

---

## Example 2

```python
number = 10

if number > 0:
    print("Positive Number")
```

Output:

```text
Positive Number
```

---

# Understanding Indentation

Python uses indentation (spaces) to define blocks of code.

Correct:

```python
if True:
    print("Hello")
```

Incorrect:

```python
if True:
print("Hello")
```

Output:

```text
IndentationError
```

---

# 3. The if-else Statement

Sometimes we want one action when the condition is True and another when it is False.

## Syntax

```python
if condition:
    # code if true
else:
    # code if false
```

---

## Example

```python
age = 16

if age >= 18:
    print("Eligible to vote")
else:
    print("Not eligible to vote")
```

Output:

```text
Not eligible to vote
```

---

## Example: Even or Odd

```python
number = 7

if number % 2 == 0:
    print("Even")
else:
    print("Odd")
```

Output:

```text
Odd
```

---

# 4. The if-elif-else Ladder

When multiple conditions need to be checked, use `elif`.

## Syntax

```python
if condition1:
    # code
elif condition2:
    # code
elif condition3:
    # code
else:
    # code
```

---

## Example

```python
marks = 75

if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
elif marks >= 50:
    print("Grade C")
else:
    print("Fail")
```

Output:

```text
Grade B
```

---

# How Python Evaluates Conditions

Python checks conditions from top to bottom.

Example:

```python
marks = 95

if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
```

Output:

```text
Grade A
```

Python stops after the first matching condition.

---

# 5. Nested Conditions

A conditional statement inside another conditional statement is called a nested condition.

## Syntax

```python
if condition1:
    if condition2:
        # code
```

---

# Ternary Operator (Conditional Expression)

The ternary operator is a shorthand way of writing an `if-else` statement in a single line.

## Syntax

```python
value_if_true if condition else value_if_false
```

---

## Example 1: Voting Eligibility

Using if-else:

```python
age = 20

if age >= 18:
    print("Eligible to Vote")
else:
    print("Not Eligible to Vote")
```

Using Ternary Operator:

```python
age = 20

result = "Eligible to Vote" if age >= 18 else "Not Eligible to Vote"

print(result)
```

Output:

```text
Eligible to Vote
```

---

## Example 2: Even or Odd

```python
number = 15

result = "Even" if number % 2 == 0 else "Odd"

print(result)
```

Output:

```text
Odd
```

---

## Example 3: Pass or Fail

```python
marks = 72

result = "Pass" if marks >= 35 else "Fail"

print(result)
```

Output:

```text
Pass
```

---

## Example 4: Largest of Two Numbers

```python
a = 20
b = 15

largest = a if a > b else b

print("Largest Number:", largest)
```

Output:

```text
Largest Number: 20
```

---

## Nested Ternary Operator

Multiple conditions can be checked using nested ternary operators.

```python
marks = 85

grade = "A" if marks >= 90 else \
        "B" if marks >= 75 else \
        "C" if marks >= 50 else \
        "F"

print(grade)
```

Output:

```text
B
```

---

### Key Takeaways

✅ Conditional statements allow programs to make decisions.

✅ `if` executes code only when a condition is True.

✅ `if-else` provides two possible execution paths.

✅ `elif` helps handle multiple conditions efficiently.

✅ Python evaluates conditions from top to bottom and stops at the first match.

✅ Nested conditions allow one condition to be checked inside another.

✅ Indentation is mandatory in Python and defines code blocks.

✅ Conditional statements are commonly used for validation, grading, authentication, and decision-making.

✅ Combining conditions with logical operators creates more powerful programs.

✅ Conditional statements are the foundation for building intelligent applications.

---
