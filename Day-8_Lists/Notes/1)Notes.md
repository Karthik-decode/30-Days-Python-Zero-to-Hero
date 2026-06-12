# Day 8: Lists in Python

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

* What lists are
* Creating Lists
* List Indexing
* Negative Indexing
* List Slicing
* Modifying Lists
* Common List Methods
* Looping Through Lists
* Real-World Applications of Lists

---

# 1. What is a List?

A list is an ordered collection of items.

Lists allow us to store multiple values in a single variable.

Example:

```python
fruits = ["Apple", "Banana", "Mango"]

print(fruits)
```

Output:

```text
['Apple', 'Banana', 'Mango']
```

---

# Why Use Lists?

Without lists:

```python
fruit1 = "Apple"
fruit2 = "Banana"
fruit3 = "Mango"
```

With lists:

```python
fruits = ["Apple", "Banana", "Mango"]
```

Lists make data easier to manage and process.

---

# 2. Creating Lists

## Empty List

```python
numbers = []
```

---

## List of Integers

```python
numbers = [10, 20, 30, 40, 50]
```

---

## List of Strings

```python
fruits = ["Apple", "Banana", "Mango"]
```

---

## Mixed Data Types

```python
data = ["Karthik", 20, 8.5, True]
```

Python lists can store different data types together.

---

## Nested Lists

```python
matrix = [
    [1, 2],
    [3, 4]
]

print(matrix)
```

Output:

```text
[[1, 2], [3, 4]]
```

---

# 3. List Indexing

Like strings, lists use indexing.

```text
Apple  Banana  Mango
  0       1      2
```

---

## Accessing Elements

```python
fruits = ["Apple", "Banana", "Mango"]

print(fruits[0])
print(fruits[1])
print(fruits[2])
```

Output:

```text
Apple
Banana
Mango
```

---

# Negative Indexing

```text
Apple  Banana  Mango
 -3      -2      -1
```

---

```python
fruits = ["Apple", "Banana", "Mango"]

print(fruits[-1])
print(fruits[-2])
```

Output:

```text
Mango
Banana
```

---

# 4. List Slicing

Slicing extracts part of a list.

## Syntax

```python
list[start:end]
```

---

## Example

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[1:4])
```

Output:

```text
[20, 30, 40]
```

---

## More Examples

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[:3])
print(numbers[2:])
print(numbers[:])
```

Output:

```text
[10, 20, 30]
[30, 40, 50]
[10, 20, 30, 40, 50]
```

---

# Step Slicing

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[::2])
```

Output:

```text
[10, 30, 50]
```

---

## Reverse a List

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[::-1])
```

Output:

```text
[50, 40, 30, 20, 10]
```

---

# 5. Modifying List Elements

Lists are mutable, meaning they can be changed.

---

## Example

```python
fruits = ["Apple", "Banana", "Mango"]

fruits[1] = "Orange"

print(fruits)
```

Output:

```text
['Apple', 'Orange', 'Mango']
```

---

# 6. List Methods

Methods are built-in functions that work on lists.

---

## append()

Adds an element at the end.

```python
fruits = ["Apple", "Banana"]

fruits.append("Mango")

print(fruits)
```

Output:

```text
['Apple', 'Banana', 'Mango']
```

---

## insert()

Adds an element at a specific position.

```python
fruits = ["Apple", "Mango"]

fruits.insert(1, "Banana")

print(fruits)
```

Output:

```text
['Apple', 'Banana', 'Mango']
```

---

## remove()

Removes a specific element.

```python
fruits = ["Apple", "Banana", "Mango"]

fruits.remove("Banana")

print(fruits)
```

Output:

```text
['Apple', 'Mango']
```

---

## pop()

Removes and returns an element.

```python
fruits = ["Apple", "Banana", "Mango"]

removed = fruits.pop()

print(removed)
print(fruits)
```

Output:

```text
Mango
['Apple', 'Banana']
```

---

## sort()

Sorts the list.

```python
numbers = [5, 2, 8, 1]

numbers.sort()

print(numbers)
```

Output:

```text
[1, 2, 5, 8]
```

---

## reverse()

Reverses the list.

```python
numbers = [1, 2, 3, 4]

numbers.reverse()

print(numbers)
```

Output:

```text
[4, 3, 2, 1]
```

---

## count()

Counts occurrences of an element.

```python
numbers = [1, 2, 2, 3, 2]

print(numbers.count(2))
```

Output:

```text
3
```

---

## index()

Returns the index of an element.

```python
fruits = ["Apple", "Banana", "Mango"]

print(fruits.index("Banana"))
```

Output:

```text
1
```

---

## clear()

Removes all elements.

```python
fruits = ["Apple", "Banana"]

fruits.clear()

print(fruits)
```

Output:

```text
[]
```

---

# 7. Useful Built-in Functions

## len()

Returns the number of elements.

```python
numbers = [10, 20, 30]

print(len(numbers))
```

Output:

```text
3
```

---

## max()

Returns the largest element.

```python
numbers = [10, 40, 20]

print(max(numbers))
```

Output:

```text
40
```

---

## min()

Returns the smallest element.

```python
numbers = [10, 40, 20]

print(min(numbers))
```

Output:

```text
10
```

---

## sum()

Returns the total sum.

```python
numbers = [10, 20, 30]

print(sum(numbers))
```

Output:

```text
60
```

---

# 8. Looping Through Lists

## Using for Loop

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

## Using Indexes

```python
fruits = ["Apple", "Banana", "Mango"]

for i in range(len(fruits)):
    print(i, fruits[i])
```

Output:

```text
0 Apple
1 Banana
2 Mango
```

---

### Key Takeaways

✅ Lists are ordered collections used to store multiple values.

✅ Lists can contain different data types.

✅ Indexing is used to access individual elements.

✅ Negative indexing accesses elements from the end.

✅ Slicing extracts portions of a list.

✅ Lists are mutable, meaning they can be modified.

✅ `append()`, `insert()`, `remove()`, `pop()`, `sort()`, and `reverse()` are commonly used list methods.

✅ `len()`, `max()`, `min()`, and `sum()` are useful built-in functions for lists.

✅ Lists work seamlessly with loops.

✅ Lists are one of the most frequently used data structures in Python.

---
