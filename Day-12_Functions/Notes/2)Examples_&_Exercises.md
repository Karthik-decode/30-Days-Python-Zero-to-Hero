# Practical Examples

## Example 1: Even or Odd

```python
def check_even_odd(number):
    if number % 2 == 0:
        return "Even"
    else:
        return "Odd"

print(check_even_odd(10))
print(check_even_odd(7))
```

Output:

```text
Even
Odd
```

---

## Example 2: Find Maximum

```python
def find_max(a, b):
    if a > b:
        return a
    else:
        return b

print(find_max(10, 20))
```

Output:

```text
20
```

---

## Example 3: Calculate Average

```python
def average(numbers):
    return sum(numbers) / len(numbers)

marks = [80, 90, 70, 85]

print(average(marks))
```

Output:

```text
81.25
```

---

# Practice Exercises

## Exercise 1

Create a function called `greet()` that prints:

```text
Hello, Python!
```

---

## Exercise 2

Create a function that accepts a name and prints:

```text
Hello Karthik
```

---

## Exercise 3

Create a function that accepts two numbers and returns their sum.

---

## Exercise 4

Create a function that returns the square of a number.

Example:

```text
Input: 5
Output: 25
```

---

## Exercise 5

Create a function to check whether a number is even or odd.

---

## Exercise 6

Create a function that accepts three numbers and returns the largest number.

---

## Exercise 7

Create a function that calculates the factorial of a number.

---

## Exercise 8

Create a function that accepts a list of numbers and returns their average.

---

## Exercise 9

Create a function using a default argument.

Example:

```python
greet()
greet("Karthik")
```

---

## Exercise 10

Create a function using `*args` that calculates the sum of any number of values.

Example:

```python
add(10, 20)
add(10, 20, 30, 40)
```

---


# Mini Project: Calculator Using Functions

```python
def add(a, b):
    return a + b


def subtract(a, b):
    return a - b


def multiply(a, b):
    return a * b


def divide(a, b):
    return a / b


a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

print("Addition:", add(a, b))
print("Subtraction:", subtract(a, b))
print("Multiplication:", multiply(a, b))
print("Division:", divide(a, b))
```

---