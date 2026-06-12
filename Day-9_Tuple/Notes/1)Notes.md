# Day 9: Tuples in Python

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

* What tuples are
* Creating tuples
* Tuple indexing
* Tuple slicing
* Tuple operations
* Tuple packing
* Tuple unpacking
* Built-in tuple methods
* Real-world tuple examples

---

# 1. What is a Tuple?

A tuple is an ordered collection of items.

Similar to a list, but tuples are **immutable**.

Immutable means once created, elements cannot be changed.

---

## Creating a Tuple

```python
fruits = ("Apple", "Banana", "Mango")

print(fruits)
```

Output:

```text
('Apple', 'Banana', 'Mango')
```

---

# Why Use Tuples?

Use tuples when data should not change.

Examples:

* Days of the week
* Months of the year
* Geographic coordinates
* RGB colors

---

# List vs Tuple

| Feature          | List  | Tuple |
| ---------------- | ----- | ----- |
| Syntax           | []    | ()    |
| Mutable          | ✅ Yes | ❌ No  |
| Faster           | ❌     | ✅     |
| Memory Efficient | ❌     | ✅     |

---

# 2. Creating Tuples

## Empty Tuple

```python
data = ()
```

---

## Integer Tuple

```python
numbers = (10, 20, 30, 40)
```

---

## String Tuple

```python
fruits = ("Apple", "Banana", "Mango")
```

---

## Mixed Data Types

```python
student = ("Karthik", 20, 8.5, True)
```

---

# Single Element Tuple

Incorrect:

```python
number = (10)
```

Type:

```python
print(type(number))
```

Output:

```text
<class 'int'>
```

---

Correct:

```python
number = (10,)
```

Output:

```text
<class 'tuple'>
```

Notice the comma.

---

# 3. Tuple Indexing

```text
Apple  Banana  Mango
  0       1      2
```

---

## Access Elements

```python
fruits = ("Apple", "Banana", "Mango")

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

```python
print(fruits[-1])
```

Output:

```text
Mango
```

---

# 4. Tuple Slicing

## Syntax

```python
tuple[start:end]
```

---

## Example

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[1:4])
```

Output:

```text
(20, 30, 40)
```

---

## More Examples

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[:3])
print(numbers[2:])
print(numbers[:])
```

Output:

```text
(10, 20, 30)
(30, 40, 50)
(10, 20, 30, 40, 50)
```

---

# Step Slicing

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[::2])
```

Output:

```text
(10, 30, 50)
```

---

## Reverse a Tuple

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[::-1])
```

Output:

```text
(50, 40, 30, 20, 10)
```

---

# 5. Tuple Operations

## Concatenation

Combining tuples using `+`.

```python
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)

result = tuple1 + tuple2

print(result)
```

Output:

```text
(1, 2, 3, 4, 5, 6)
```

---

## Repetition

Using `*`.

```python
numbers = (1, 2)

print(numbers * 3)
```

Output:

```text
(1, 2, 1, 2, 1, 2)
```

---

## Membership Operator

```python
fruits = ("Apple", "Banana", "Mango")

print("Banana" in fruits)
```

Output:

```text
True
```

---

## Length

```python
numbers = (10, 20, 30)

print(len(numbers))
```

Output:

```text
3
```

---

# 6. Tuple Packing

Packing means storing multiple values into a tuple automatically.

```python
student = "Karthik", 20, 8.5
```

Python automatically creates:

```python
("Karthik", 20, 8.5)
```

---

## Example

```python
data = 10, 20, 30

print(data)
print(type(data))
```

Output:

```text
(10, 20, 30)
<class 'tuple'>
```

---

# 7. Tuple Unpacking

Unpacking means extracting tuple values into variables.

```python
student = ("Karthik", 20, 8.5)

name, age, cgpa = student

print(name)
print(age)
print(cgpa)
```

Output:

```text
Karthik
20
8.5
```

---

# Visual Representation

```text
Tuple
↓
("Karthik", 20, 8.5)

↓ Unpacking

name = "Karthik"
age = 20
cgpa = 8.5
```

---

# Multiple Assignment

```python
a, b, c = (10, 20, 30)

print(a)
print(b)
print(c)
```

Output:

```text
10
20
30
```

---

# Swapping Variables

Without temporary variable:

```python
a = 10
b = 20

a, b = b, a

print(a, b)
```

Output:

```text
20 10
```

This works because of tuple packing and unpacking.

---

# 8. Tuple Methods

Tuples have only two built-in methods.

---

## count()

Counts occurrences.

```python
numbers = (1, 2, 2, 3, 2)

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
fruits = ("Apple", "Banana", "Mango")

print(fruits.index("Banana"))
```

Output:

```text
1
```

---

# Useful Built-in Functions

## len()

```python
numbers = (10, 20, 30)

print(len(numbers))
```

Output:

```text
3
```

---

## max()

```python
numbers = (10, 40, 20)

print(max(numbers))
```

Output:

```text
40
```

---

## min()

```python
numbers = (10, 40, 20)

print(min(numbers))
```

Output:

```text
10
```

---

## sum()

```python
numbers = (10, 20, 30)

print(sum(numbers))
```

Output:

```text
60
```

---

### Key Takeaways

✅ Tuples are ordered and immutable collections.

✅ Tuples use parentheses `()`.

✅ Indexing and slicing work similarly to lists.

✅ Tuple elements cannot be modified after creation.

✅ Tuple operations include concatenation and repetition.

✅ Packing automatically creates tuples.

✅ Unpacking extracts tuple values into variables.

✅ Variable swapping is commonly done using tuple unpacking.

✅ Tuples provide better performance and memory efficiency than lists.

✅ Tuples are ideal for fixed data that should not change.

---
