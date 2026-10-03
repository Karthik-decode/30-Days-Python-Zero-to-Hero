# Practical Example – Student Marks

```python
try:
    marks = int(input("Enter marks: "))

    if marks < 0 or marks > 100:
        raise ValueError("Marks must be between 0 and 100.")

    print("Valid marks:", marks)

except ValueError as error:
    print("Error:", error)
```

---

# Practical Example – Age Validation

```python
try:
    age = int(input("Enter age: "))

    if age < 0:
        raise ValueError("Age cannot be negative.")

    print("Valid age:", age)

except ValueError as error:
    print("Error:", error)
```

---

# Practical Example – Login System

```python
correct_username = "admin"
correct_password = "1234"

try:
    username = input("Username: ")
    password = input("Password: ")

    if username != correct_username:
        raise ValueError("Invalid username.")

    if password != correct_password:
        raise ValueError("Invalid password.")

    print("Login successful.")

except ValueError as error:
    print("Login failed:", error)
```

---

# Practical Example – Division Function

```python
def safe_divide(a, b):

    try:
        return a / b

    except ZeroDivisionError:
        return "Cannot divide by zero."

    except TypeError:
        return "Both values must be numbers."

print(safe_divide(10, 2))
print(safe_divide(10, 0))
print(safe_divide(10, "5"))
```

---

# Practice Exercises

## Exercise 1
Write a program that handles invalid integer input.

## Exercise 2
Write a program that handles division by zero.

## Exercise 3
Write a program that handles invalid list indexes.

## Exercise 4
Write a program that handles missing dictionary keys.

## Exercise 5
Write a program that handles a missing file.

## Exercise 6
Write a calculator using exception handling.

## Exercise 7
Create a function that safely converts a string into an integer.

## Exercise 8
Create an age validator using `raise`.

## Exercise 9
Create a custom exception called `InvalidMarksError`.

## Exercise 10
Create an ATM program using exception handling.

---

# Mini Project 1: Robust Calculator

Build a calculator that:

- Accepts two numbers
- Accepts an operator
- Handles invalid input
- Handles division by zero
- Handles invalid operators

Add `%`, `**`, and `//` as a challenge.

---

# Mini Project 2: Student Marks Validator

Create a program that:

1. Accepts student name
2. Accepts marks
3. Checks whether marks are between 0 and 100
4. Handles invalid input
5. Displays the result

```python
try:
    name = input("Enter student name: ")
    marks = int(input("Enter marks: "))

    if marks < 0 or marks > 100:
        raise ValueError("Marks must be between 0 and 100.")

    print("Student:", name)
    print("Marks:", marks)

except ValueError as error:
    print("Error:", error)
```

---

# Mini Project 3: ATM Withdrawal

```python
balance = 5000

try:
    amount = float(input("Enter withdrawal amount: "))

    if amount <= 0:
        raise ValueError("Amount must be greater than zero.")

    if amount > balance:
        raise ValueError("Insufficient balance.")

    balance -= amount

    print("Withdrawal successful.")
    print("Remaining balance:", balance)

except ValueError as error:
    print("Transaction failed:", error)
```

---