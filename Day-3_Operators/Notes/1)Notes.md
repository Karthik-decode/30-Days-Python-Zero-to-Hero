# Day 3: Operators in Python

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

* What operators are
* Arithmetic Operators
* Comparison Operators
* Assignment Operators
* Logical Operators
* Operator Precedence
* Building a Simple Calculator

---

# 1. What are Operators?

Operators are special symbols used to perform operations on variables and values.

Example:

```python
a = 10
b = 5

print(a + b)
```

Output:

```text
15
```

Here, `+` is an operator.

---

# Types of Operators in Python

| Operator Type | Purpose                   |
| ------------- | ------------------------- |
| Arithmetic    | Mathematical calculations |
| Comparison    | Compare values            |
| Assignment    | Assign values             |
| Logical       | Combine conditions        |

---

# 2. Arithmetic Operators

Arithmetic operators perform mathematical operations.

| Operator | Meaning        | Example |
| -------- | -------------- | ------- |
| +        | Addition       | 10 + 5  |
| -        | Subtraction    | 10 - 5  |
| *        | Multiplication | 10 * 5  |
| /        | Division       | 10 / 5  |
| //       | Floor Division | 10 // 3 |
| %        | Modulus        | 10 % 3  |
| **       | Exponent       | 2 ** 3  |

---

## Addition

```python
a = 10
b = 5

print(a + b)
```

Output:

```text
15
```

---

## Subtraction

```python
print(10 - 5)
```

Output:

```text
5
```

---

## Multiplication

```python
print(10 * 5)
```

Output:

```text
50
```

---

## Division

```python
print(10 / 5)
```

Output:

```text
2.0
```

Division always returns a float.

---

## Floor Division

Returns only the whole number part.

```python
print(10 // 3)
```

Output:

```text
3
```

---

## Modulus

Returns the remainder.

```python
print(10 % 3)
```

Output:

```text
1
```

Useful for:

* Checking even/odd numbers
* Cyclic operations
* Time calculations

Example:

```python
print(20 % 2)
```

Output:

```text
0
```

Since remainder is 0, 20 is even.

---

## Exponent

Raises a number to a power.

```python
print(2 ** 3)
```

Output:

```text
8
```

Because:

```text
2 × 2 × 2 = 8
```

---

# 3. Comparison Operators

Comparison operators compare values and return:

```python
True
False
```

| Operator | Meaning               |
| -------- | --------------------- |
| ==       | Equal to              |
| !=       | Not equal to          |
| >        | Greater than          |
| <        | Less than             |
| >=       | Greater than or equal |
| <=       | Less than or equal    |

---

## Equal To

```python
print(10 == 10)
```

Output:

```text
True
```

---

## Not Equal To

```python
print(10 != 5)
```

Output:

```text
True
```

---

## Greater Than

```python
print(20 > 10)
```

Output:

```text
True
```

---

## Less Than

```python
print(5 < 10)
```

Output:

```text
True
```

---

## Greater Than or Equal To

```python
print(10 >= 10)
```

Output:

```text
True
```

---

## Less Than or Equal To

```python
print(5 <= 10)
```

Output:

```text
True
```

---

# 4. Assignment Operators

Used to assign values.

---

## Basic Assignment

```python
x = 10
```

---

## Add and Assign

```python
x = 10

x += 5

print(x)
```

Output:

```text
15
```

Equivalent to:

```python
x = x + 5
```

---

## Subtract and Assign

```python
x = 10

x -= 3

print(x)
```

Output:

```text
7
```

---

## Multiply and Assign

```python
x = 10

x *= 2

print(x)
```

Output:

```text
20
```

---

## Divide and Assign

```python
x = 20

x /= 2

print(x)
```

Output:

```text
10.0
```

---

# 5. Logical Operators

Logical operators combine multiple conditions.

| Operator | Meaning                             |
| -------- | ----------------------------------- |
| and      | Both conditions must be True        |
| or       | At least one condition must be True |
| not      | Reverse the result                  |

---

## AND Operator

```python
age = 20
citizen = True

print(age >= 18 and citizen)
```

Output:

```text
True
```

Both conditions are True.

---

## OR Operator

```python
print(True or False)
```

Output:

```text
True
```

At least one is True.

---

## NOT Operator

```python
print(not True)
```

Output:

```text
False
```

---

# Truth Table

| A     | B     | A and B | A or B |
| ----- | ----- | ------- | ------ |
| True  | True  | True    | True   |
| True  | False | False   | True   |
| False | True  | False   | True   |
| False | False | False   | False  |

---

# 6. Operator Precedence

Python follows BODMAS-like rules.

Example:

```python
print(5 + 2 * 3)
```

Output:

```text
11
```

Because multiplication happens first.

Equivalent to:

```text
5 + (2 × 3)
```

---

## Using Parentheses

```python
print((5 + 2) * 3)
```

Output:

```text
21
```

Parentheses have highest priority.

---

# Summary

## Arithmetic Operators

```python
+
-
*
/
//
%
**
```

## Comparison Operators

```python
==
!=
>
<
>=
<=
```

## Assignment Operators

```python
=
+=
-=
*=
/=
```

## Logical Operators

```python
and
or
not
```

---

# 7. Membership Operators

Membership operators are used to check whether a value exists in a sequence.

Python provides:

```python
in
not in
```

---

## in Operator

Returns True if the value exists.

```python
name = "Python"

print("P" in name)
```

Output:

```text
True
```

---

```python
numbers = [10, 20, 30, 40]

print(20 in numbers)
```

Output:

```text
True
```

---

## not in Operator

Returns True if the value does not exist.

```python
name = "Python"

print("Z" not in name)
```

Output:

```text
True
```

---

```python
numbers = [10, 20, 30]

print(50 not in numbers)
```

Output:

```text
True
```

---

# 8. Identity Operators

Identity operators compare whether two variables refer to the same object in memory.

Python provides:

```python
is
is not
```

---

## is Operator

```python
a = [1, 2, 3]
b = a

print(a is b)
```

Output:

```text
True
```

Both variables point to the same object.

---

## is not Operator

```python
a = [1, 2, 3]
b = [1, 2, 3]

print(a is not b)
```

Output:

```text
True
```

Even though values are identical, they are different objects.

---

# Difference Between == and is

Many beginners get confused here.

## Equality Operator (==)

Checks whether values are equal.

```python
a = [1, 2, 3]
b = [1, 2, 3]

print(a == b)
```

Output:

```text
True
```

Values are equal.

---

## Identity Operator (is)

Checks whether both variables refer to the same object in the memory.

```python
a = [1, 2, 3]
b = [1, 2, 3]

print(a is b)
```

Output:

```text
False
```

Different objects in memory.

---

# Visual Explanation

```text
a ───────► [1, 2, 3]
b ───────► [1, 2, 3]
```

Different memory locations:

```python
a == b      # True
a is b      # False
```

---

```text
a ──┐
    ├────► [1, 2, 3]
b ──┘
```

Same memory location:

```python
a == b      # True
a is b      # True
```

---

# Complete Operator Categories in Python

| Category   | Operators                                      |
| ---------- | ---------------------------------------------- |
| Arithmetic | +, -, *, /, %, //, **                          |
| Comparison | ==, !=, >, <, >=, <=                           |
| Assignment | =, +=, -=, *=, /=, %=                          |
| Logical    | and, or, not                                   |
| Membership | in, not in                                     |
| Identity   | is, is not                                     |

---

### Key Takeaways

### Key Takeaways

✅ Arithmetic operators perform mathematical calculations.

✅ Comparison operators compare values and return `True` or `False`.

✅ Assignment operators assign and update variable values efficiently.

✅ Logical operators combine multiple conditions.

✅ Ternary operators provide a concise one-line alternative to `if-else` statements.

✅ Membership operators check whether a value exists in a sequence.

✅ Identity operators determine whether two variables refer to the same object in memory.

✅ `==` checks value equality, while `is` checks object identity.

✅ Operator precedence determines the order in which expressions are evaluated.

✅ Parentheses `()` can be used to control evaluation order and improve readability.

✅ Operators are fundamental building blocks used in almost every Python program.