# Day 7: Loops in Python

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

* Why loops are needed
* The `for` loop
* The `while` loop
* The `break` statement
* The `continue` statement
* Nested loops
* Real-world loop examples
* Pattern printing and multiplication tables

---

# 1. Introduction to Loops

Loops allow us to execute a block of code multiple times.

Without loops:

```python
print("Python")
print("Python")
print("Python")
print("Python")
print("Python")
```

With loops:

```python
for i in range(5):
    print("Python")
```

Output:

```text
Python
Python
Python
Python
Python
```

Loops reduce code repetition and make programs more efficient.

---

# 2. The for Loop

The `for` loop is used when we know how many times we want to repeat something.

## Syntax

```python
for variable in sequence:
    # code block
```

---

## Example

```python
for i in range(5):
    print(i)
```

Output:

```text
0
1
2
3
4
```

---

# Understanding range()

The `range()` function generates a sequence of numbers.

---

## range(stop)

```python
for i in range(5):
    print(i)
```

Output:

```text
0
1
2
3
4
```

---

## range(start, stop)

```python
for i in range(1, 6):
    print(i)
```

Output:

```text
1
2
3
4
5
```

---

## range(start, stop, step)

```python
for i in range(0, 11, 2):
    print(i)
```

Output:

```text
0
2
4
6
8
10
```

---

# Looping Through Strings

```python
name = "Python"

for ch in name:
    print(ch)
```

Output:

```text
P
y
t
h
o
n
```

---

# Looping Through Lists

```python
fruits = ["Apple", "Banana", "Mango"]

for fruit in fruits:
    print(fruit)
```

Output:

```text
Apple
Banana
Mango
```

---

# 3. The while Loop

A `while` loop runs as long as a condition remains True.

## Syntax

```python
while condition:
    # code block
```

---

## Example

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

Output:

```text
1
2
3
4
5
```

---

# Infinite Loops

Be careful.

```python
while True:
    print("Hello")
```

This runs forever unless stopped manually.

---

# User-Controlled Loop

```python
password = ""

while password != "python":
    password = input("Enter password: ")

print("Access Granted")
```

The loop continues until the correct password is entered.

---

# 4. break Statement

The `break` statement immediately terminates a loop.

---

## Example

```python
for i in range(10):
    if i == 5:
        break

    print(i)
```

Output:

```text
0
1
2
3
4
```

The loop stops when `i` becomes 5.

---

# break with while

```python
count = 1

while True:
    print(count)

    if count == 5:
        break

    count += 1
```

Output:

```text
1
2
3
4
5
```

---

# 5. continue Statement

The `continue` statement skips the current iteration and moves to the next one.

---

## Example

```python
for i in range(1, 6):
    if i == 3:
        continue

    print(i)
```

Output:

```text
1
2
4
5
```

The number 3 is skipped.

---

# continue with while

```python
count = 0

while count < 5:
    count += 1

    if count == 3:
        continue

    print(count)
```

Output:

```text
1
2
4
5
```

---

# Difference Between break and continue

| Statement | Effect                    |
| --------- | ------------------------- |
| break     | Stops the loop completely |
| continue  | Skips current iteration   |

---

## Example

```python
for i in range(5):
    if i == 2:
        break

    print(i)
```

Output:

```text
0
1
```

---

```python
for i in range(5):
    if i == 2:
        continue

    print(i)
```

Output:

```text
0
1
3
4
```

---

# 6. Nested Loops

A loop inside another loop is called a nested loop.

---

## Example

```python
for i in range(3):
    for j in range(3):
        print(i, j)
```

Output:

```text
0 0
0 1
0 2
1 0
1 1
1 2
2 0
2 1
2 2
```

---

# Multiplication Table

```python
number = 5

for i in range(1, 11):
    print(f"{number} x {i} = {number * i}")
```

Output:

```text
5 x 1 = 5
5 x 2 = 10
...
5 x 10 = 50
```

---

# Pattern Printing

## Pattern 1

```python
for i in range(5):
    print("*")
```

Output:

```text
*
*
*
*
*
```

---

## Pattern 2

```python
for i in range(5):
    print("*" * 5)
```

Output:

```text
*****
*****
*****
*****
*****
```

---

## Pattern 3

```python
for i in range(1, 6):
    print("*" * i)
```

Output:

```text
*
**
***
****
*****
```

---



### Key Takeaways

✅ Loops allow code to be executed repeatedly.

✅ `for` loops are used when the number of iterations is known.

✅ `while` loops run as long as a condition remains True.

✅ `range()` generates sequences of numbers.

✅ `break` immediately exits a loop.

✅ `continue` skips the current iteration and moves to the next one.

✅ Nested loops are loops inside other loops.

✅ Loops are commonly used for counting, searching, validation, and pattern printing.

✅ Infinite loops occur when loop conditions never become False.

✅ Loops are essential for automation and repetitive tasks.

---

