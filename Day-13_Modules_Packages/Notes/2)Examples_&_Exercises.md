# Practical Example – Random Password Generator

```python
import random

characters = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789"

password = ""

for i in range(8):
    password += random.choice(characters)

print("Password:", password)
```

Possible output:

```text
Password: aK7pQ2xM
```

The output will be different each time.

---

# Practical Example – Circle Calculator

```python
import math

radius = float(input("Enter radius: "))

area = math.pi * radius ** 2
circumference = 2 * math.pi * radius

print("Area:", area)
print("Circumference:", circumference)
```

Example output:

```text
Enter radius: 5
Area: 78.53981633974483
Circumference: 31.41592653589793
```

---

# Practical Example – Dice Simulator

```python
import random

dice = random.randint(1, 6)

print("You rolled:", dice)
```

Possible output:

```text
You rolled: 4
```

---

# Practical Example – Current Date

```python
from datetime import date

today = date.today()

print("Today's date:", today)
```

Possible output:

```text
Today's date: 2026-09-30
```

---

# Exercises

## Exercise 1

Create a module called:

```text
numbers.py
```

Create functions:

```python
square()
cube()
```

Import them into `main.py`.

---

## Exercise 2

Use the `math` module to find:

- Square root of 144
- Factorial of 6
- Power of 2³
- Ceiling of 7.2
- Floor of 7.8

---

## Exercise 3

Use the `random` module to:

- Generate a number between 1 and 100
- Select a random name from a list
- Generate a random number between 1 and 6

---

## Exercise 4

Use `datetime` to display:

- Current date
- Current year
- Current month
- Current day

---

## Exercise 5

Create a module called:

```text
student.py
```

Create functions:

```python
calculate_total()
calculate_average()
```

Import them into `main.py`.

---

## Exercise 6

Create a package:

```text
utilities/
```

Inside it create:

```text
calculator.py
string_tools.py
```

Add useful functions to both modules and import them into `main.py`.

---
