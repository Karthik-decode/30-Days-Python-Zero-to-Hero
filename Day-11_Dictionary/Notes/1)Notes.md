# Day 11: Dictionaries in Python

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

* What dictionaries are
* Key-Value Pairs
* Creating dictionaries
* Accessing dictionary values
* Adding and updating items
* Removing items
* Dictionary methods
* Nested dictionaries
* Real-world applications of dictionaries

---

# 1. What is a Dictionary?

A dictionary is a collection of data stored as **key-value pairs**.

Think of it like a real dictionary:

```text
Word        Meaning
Python  →   Programming Language
Apple   →   Fruit
Car     →   Vehicle
```

In Python:

```python
student = {
    "name": "Karthik",
    "age": 20,
    "cgpa": 8.5
}
```

---

# Why Use Dictionaries?

Lists store values by position.

```python
student = ["Karthik", 20, 8.5]
```

Problem:

```python
student[2]
```

What does 2 mean?

Not obvious.

---

Dictionaries solve this:

```python
student = {
    "name": "Karthik",
    "age": 20,
    "cgpa": 8.5
}
```

Now:

```python
student["cgpa"]
```

Clearly means CGPA.

---

# 2. Creating Dictionaries

## Empty Dictionary

```python
data = {}
```

---

## Student Dictionary

```python
student = {
    "name": "Karthik",
    "age": 20,
    "cgpa": 8.5
}
```

---

## Mixed Data Types

```python
data = {
    "name": "Python",
    "version": 3.13,
    "popular": True
}
```

---

# Dictionary Structure

```text
{
   key : value,
   key : value
}
```

Example:

```python
{
   "name": "Karthik",
   "age": 20
}
```

---

# 3. Accessing Values

Use the key to access a value.

```python
student = {
    "name": "Karthik",
    "age": 20
}

print(student["name"])
```

Output:

```text
Karthik
```

---

## Multiple Values

```python
student = {
    "name": "Karthik",
    "age": 20,
    "cgpa": 8.5
}

print(student["name"])
print(student["age"])
print(student["cgpa"])
```

Output:

```text
Karthik
20
8.5
```

---

# get() Method

A safer way to access values.

```python
student = {
    "name": "Karthik"
}

print(student.get("name"))
```

Output:

```text
Karthik
```

---

## Difference Between [] and get()

Using:

```python
student["age"]
```

Output:

```text
KeyError
```

if the key does not exist.

---

Using:

```python
student.get("age")
```

Output:

```python
None
```

No error occurs.

---

## Default Value

```python
student.get("age", "Not Found")
```

Output:

```text
Not Found
```

---

# 4. Adding New Key-Value Pairs

```python
student = {
    "name": "Karthik"
}

student["age"] = 20

print(student)
```

Output:

```text
{'name': 'Karthik', 'age': 20}
```

---

# 5. Updating Values

```python
student = {
    "name": "Karthik",
    "age": 20
}

student["age"] = 21

print(student)
```

Output:

```text
{'name': 'Karthik', 'age': 21}
```

---

# 6. Removing Items

## pop()

Removes a key and returns its value.

```python
student = {
    "name": "Karthik",
    "age": 20
}

removed = student.pop("age")

print(removed)
print(student)
```

Output:

```text
20
{'name': 'Karthik'}
```

---

## popitem()

Removes the last inserted item.

```python
student = {
    "name": "Karthik",
    "age": 20
}

student.popitem()

print(student)
```

Output:

```text
{'name': 'Karthik'}
```

---

## del

```python
student = {
    "name": "Karthik",
    "age": 20
}

del student["age"]

print(student)
```

Output:

```text
{'name': 'Karthik'}
```

---

## clear()

Removes all items.

```python
student.clear()

print(student)
```

Output:

```text
{}
```

---

# 7. Dictionary Methods

## keys()

Returns all keys.

```python
student = {
    "name": "Karthik",
    "age": 20
}

print(student.keys())
```

Output:

```text
dict_keys(['name', 'age'])
```

---

## values()

Returns all values.

```python
print(student.values())
```

Output:

```text
dict_values(['Karthik', 20])
```

---

## items()

Returns key-value pairs.

```python
print(student.items())
```

Output:

```text
dict_items([('name', 'Karthik'), ('age', 20)])
```

---

## update()

Adds or updates multiple items.

```python
student = {
    "name": "Karthik"
}

student.update({
    "age": 20,
    "cgpa": 8.5
})

print(student)
```

Output:

```text
{'name': 'Karthik', 'age': 20, 'cgpa': 8.5}
```

---

# 8. Looping Through Dictionaries

## Loop Through Keys

```python
student = {
    "name": "Karthik",
    "age": 20
}

for key in student:
    print(key)
```

Output:

```text
name
age
```

---

## Loop Through Values

```python
for value in student.values():
    print(value)
```

Output:

```text
Karthik
20
```

---

## Loop Through Key-Value Pairs

```python
for key, value in student.items():
    print(key, ":", value)
```

Output:

```text
name : Karthik
age : 20
```

---

# 9. Nested Dictionaries

Dictionaries can contain other dictionaries.

```python
students = {
    "student1": {
        "name": "Karthik",
        "age": 20
    },
    "student2": {
        "name": "Ram",
        "age": 21
    }
}
```

---

## Access Nested Values

```python
print(students["student1"]["name"])
```

Output:

```text
Karthik
```

---

# Membership Operators

```python
student = {
    "name": "Karthik",
    "age": 20
}

print("name" in student)
```

Output:

```text
True
```

---

```python
print("cgpa" not in student)
```

Output:

```text
True
```

---

# Useful Built-in Functions

## len()

```python
student = {
    "name": "Karthik",
    "age": 20
}

print(len(student))
```

Output:

```text
2
```

---

### Key Takeaways

✅ Dictionaries store data using key-value pairs.

✅ Keys are unique identifiers used to access values.

✅ Values can be any data type.

✅ `[]` and `get()` are used to access values.

✅ Dictionaries are mutable and can be updated.

✅ `keys()`, `values()`, and `items()` are the most commonly used methods.

✅ Nested dictionaries allow storing complex structured data.

✅ Dictionaries are one of the most important data structures in Python.

✅ Dictionaries are widely used in APIs, databases, configurations, and real-world applications.

✅ Fast key-based lookup makes dictionaries extremely efficient.

---
