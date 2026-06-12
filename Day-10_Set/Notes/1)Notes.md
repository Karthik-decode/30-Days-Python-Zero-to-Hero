# Day 10: Sets in Python

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

* What sets are
* Creating sets
* Unique values in sets
* Set indexing limitations
* Adding and removing elements
* Set operations
* Union
* Intersection
* Difference
* Symmetric Difference
* Set methods
* Real-world applications of sets

---

# 1. What is a Set?

A set is an unordered collection of unique elements.

Unlike lists and tuples:

* Sets do not allow duplicates.
* Sets are unordered.
* Sets are mutable (can be modified).

---

## Creating a Set

```python
fruits = {"Apple", "Banana", "Mango"}

print(fruits)
```

Output:

```text
{'Apple', 'Banana', 'Mango'}
```

---

# Why Use Sets?

Sets are useful when:

* Duplicate values should be removed.
* Fast searching is required.
* Mathematical set operations are needed.

Example:

```python
numbers = {1, 2, 3, 4, 5}
```

---

# 2. Unique Values

One of the most important features of sets is that duplicate values are automatically removed.

```python
numbers = {1, 2, 2, 3, 3, 4, 5}

print(numbers)
```

Output:

```text
{1, 2, 3, 4, 5}
```

Python automatically keeps only unique values.

---

## Removing Duplicates from a List

```python
numbers = [1, 2, 2, 3, 3, 4, 5]

unique_numbers = set(numbers)

print(unique_numbers)
```

Output:

```text
{1, 2, 3, 4, 5}
```

---

# 3. Creating Sets

## Empty Set

Incorrect:

```python
data = {}
```

This creates a dictionary.

---

Correct:

```python
data = set()
```

---

## Integer Set

```python
numbers = {10, 20, 30, 40}
```

---

## String Set

```python
fruits = {"Apple", "Banana", "Mango"}
```

---

## Mixed Data Types

```python
data = {10, "Python", True, 5.5}
```

---

# 4. Sets are Unordered

Sets do not maintain insertion order.

```python
fruits = {"Apple", "Banana", "Mango"}

print(fruits)
```

Output may vary.

```text
{'Banana', 'Apple', 'Mango'}
```

---

# No Indexing

Lists:

```python
fruits[0]
```

Valid ✅

---

Sets:

```python
fruits[0]
```

Invalid ❌

Output:

```text
TypeError
```

Because sets are unordered.

---

# 5. Adding Elements

## add()

Adds a single element.

```python
fruits = {"Apple", "Banana"}

fruits.add("Mango")

print(fruits)
```

Output:

```text
{'Apple', 'Banana', 'Mango'}
```

---

## update()

Adds multiple elements.

```python
fruits = {"Apple"}

fruits.update(["Banana", "Mango"])
```

Output:

```text
{'Apple', 'Banana', 'Mango'}
```

---

# 6. Removing Elements

## remove()

Removes an element.

```python
fruits = {"Apple", "Banana", "Mango"}

fruits.remove("Banana")

print(fruits)
```

Output:

```text
{'Apple', 'Mango'}
```

---

## discard()

Removes an element safely.

```python
fruits.discard("Orange")
```

No error occurs.

---

## pop()

Removes a random element.

```python
fruits.pop()
```

Since sets are unordered, any element may be removed.

---

## clear()

Removes all elements.

```python
fruits.clear()

print(fruits)
```

Output:

```text
set()
```

---

# 7. Set Operations

Set operations are inspired by mathematical sets.

---

## Union ( | )

Combines all unique elements.

```python
A = {1, 2, 3}
B = {3, 4, 5}

print(A | B)
```

Output:

```text
{1, 2, 3, 4, 5}
```

---

## union() Method

```python
print(A.union(B))
```

Output:

```text
{1, 2, 3, 4, 5}
```

---

# Visual Representation

```text
A = {1, 2, 3}
B = {3, 4, 5}

Union

{1, 2, 3, 4, 5}
```

---

# 8. Intersection ( & )

Returns common elements.

```python
A = {1, 2, 3}
B = {3, 4, 5}

print(A & B)
```

Output:

```text
{3}
```

---

## intersection() Method

```python
print(A.intersection(B))
```

Output:

```text
{3}
```

---

# Visual Representation

```text
A = {1, 2, 3}
B = {3, 4, 5}

Intersection

{3}
```

---

# 9. Difference ( - )

Returns elements present in the first set but not in the second.

```python
A = {1, 2, 3}
B = {3, 4, 5}

print(A - B)
```

Output:

```text
{1, 2}
```

---

## difference() Method

```python
print(A.difference(B))
```

Output:

```text
{1, 2}
```

---

# Difference is Directional

```python
print(B - A)
```

Output:

```text
{4, 5}
```

Notice the result changes.

---

# 10. Symmetric Difference

Returns elements that are not common.

```python
A = {1, 2, 3}
B = {3, 4, 5}

print(A ^ B)
```

Output:

```text
{1, 2, 4, 5}
```

---

## symmetric_difference()

```python
print(A.symmetric_difference(B))
```

Output:

```text
{1, 2, 4, 5}
```

---

# Visual Representation

```text
A = {1, 2, 3}
B = {3, 4, 5}

Symmetric Difference

{1, 2, 4, 5}
```

---

# 11. Membership Operators

```python
fruits = {"Apple", "Banana", "Mango"}

print("Banana" in fruits)
```

Output:

```text
True
```

---

```python
print("Orange" not in fruits)
```

Output:

```text
True
```

---

# 12. Useful Built-in Functions

## len()

```python
numbers = {1, 2, 3, 4}

print(len(numbers))
```

Output:

```text
4
```

---

## max()

```python
numbers = {10, 20, 30}

print(max(numbers))
```

Output:

```text
30
```

---

## min()

```python
numbers = {10, 20, 30}

print(min(numbers))
```

Output:

```text
10
```

---

## sum()

```python
numbers = {10, 20, 30}

print(sum(numbers))
```

Output:

```text
60
```

---

### Key Takeaways

✅ Sets store unique values only.

✅ Duplicate elements are automatically removed.

✅ Sets are unordered and do not support indexing.

✅ `add()` and `update()` add elements to a set.

✅ `remove()`, `discard()`, and `pop()` remove elements.

✅ Union combines all unique elements.

✅ Intersection returns common elements.

✅ Difference returns unique elements from one set.

✅ Symmetric Difference returns non-common elements.

✅ Sets are extremely useful for duplicate removal and fast membership testing.

---

