# Day 4: User Input in Python

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

* The `input()` function
* Taking user input
* Type conversion with input
* Taking multiple inputs
* Common beginner mistakes
* Building interactive programs

---

# 1. What is User Input?

So far, all values in our programs have been hardcoded.

Example:

```python
name = "Karthik"

print(name)
```

Output:

```text
Karthik
```

The user cannot change the value.

To make programs interactive, we use the `input()` function.

---

# 2. The input() Function

The `input()` function allows users to enter data while the program is running.

## Syntax

```python
input("Prompt Message")
```

---

## Example

```python
name = input("Enter your name: ")

print(name)
```

Output:

```text
Enter your name: Karthik
Karthik
```

---

# 3. Storing User Input

Input is usually stored in a variable.

```python
name = input("Enter your name: ")

print("Hello", name)
```

Output:

```text
Enter your name: Karthik
Hello Karthik
```

---

# 4. Important: input() Always Returns a String

Many beginners assume numbers entered by users become integers automatically.

They do not.

Example:

```python
age = input("Enter age: ")

print(age)
print(type(age))
```

Output:

```text
Enter age: 20
20
<class 'str'>
```

Even though the user entered 20, Python stores it as a string.

---

# 5. Type Conversion with Input

To perform calculations, convert the input.

---

## Integer Input

```python
age = int(input("Enter your age: "))

print(age)
print(type(age))
```

Output:

```text
20
<class 'int'>
```

---

## Float Input

```python
height = float(input("Enter your height: "))

print(height)
```

Output:

```text
5.8
```

---

# 6. Why Type Conversion is Necessary

Incorrect:

```python
num1 = input("Enter first number: ")
num2 = input("Enter second number: ")

print(num1 + num2)
```

Input:

```text
10
20
```

Output:

```text
1020
```

Because Python joins two strings.

---

Correct:

```python
num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

print(num1 + num2)
```

Output:

```text
30
```

---

# 7. Taking Multiple Inputs

## Method 1

```python
name = input("Enter name: ")
age = int(input("Enter age: "))
city = input("Enter city: ")
```

---

## Method 2

Using one line:

```python
name, city = input("Enter name and city: ").split()
```

Input:

```text
Karthik Hyderabad
```

Output:

```python
name = "Karthik"
city = "Hyderabad"
```

---

## Multiple Numbers

```python
a, b = map(int, input("Enter two numbers: ").split())
```

Input:

```text
10 20
```

Output:

```python
a = 10
b = 20
```

---

# 8. Common Beginner Mistakes

## Mistake 1

```python
age = input("Enter age: ")

print(age + 5)
```

Error:

```text
TypeError
```

Correct:

```python
age = int(input("Enter age: "))

print(age + 5)
```

---

## Mistake 2

```python
num = int(input("Enter number: "))

print(type(num))
```

Some beginners forget the conversion and wonder why calculations fail.

Always check the data type when debugging.

---

### Key Takeaways

✅ `input()` allows users to enter data while the program is running.

✅ `input()` always returns data as a string.

✅ Use `int()` and `float()` to convert input into numeric types.

✅ Type conversion is necessary before performing mathematical calculations.

✅ Multiple inputs can be taken using `split()` and `map()`.

✅ Interactive programs are more useful than programs with hardcoded values.

✅ User input is the foundation for building real-world applications.

---
