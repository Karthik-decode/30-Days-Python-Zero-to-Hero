# 6. Real-World Examples

## Positive, Negative, or Zero

```python
number = -5

if number > 0:
    print("Positive")
elif number < 0:
    print("Negative")
else:
    print("Zero")
```

Output:

```text
Negative
```

---

## Largest of Two Numbers

```python
a = 20
b = 15

if a > b:
    print("A is larger")
else:
    print("B is larger")
```

Output:

```text
A is larger
```

---

## Password Checker

```python
password = "python123"

if password == "python123":
    print("Access Granted")
else:
    print("Access Denied")
```

Output:

```text
Access Granted
```

---

# Using User Input with Conditions

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("Eligible to vote")
else:
    print("Not eligible to vote")
```

---

# Practice Exercises

## Exercise 1

Write a program to check whether a number is:

* Positive
* Negative
* Zero

---

## Exercise 2

Write a program to check whether a number is:

* Even
* Odd

---

## Exercise 3

Take a student's marks and print:

```text
Pass
```

if marks are 35 or above, otherwise print:

```text
Fail
```

---

## Exercise 4

Take age as input and determine whether the user is eligible to vote.

---

## Exercise 5

Take two numbers and print the larger number.

---

## Exercise 6

Take a password as input and verify whether it matches:

```text
python123
```

---

## Exercise 7

Take marks as input and assign grades:

```text
90+  → A
75+  → B
50+  → C
35+  → D
Below 35 → F
```

---

## Exercise 8

Take:

* Marks
* Attendance

A student is eligible for a certificate only if:

* Marks ≥ 35
* Attendance ≥ 75

Use nested conditions.

---

