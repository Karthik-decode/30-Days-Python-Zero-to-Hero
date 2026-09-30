# Day 12: Functions in Python

## 🎯 Learning Objectives

By the end of this lesson, you will understand:

- What functions are
- Why functions are useful
- Defining functions
- Calling functions
- Parameters and arguments
- Return values
- Multiple parameters
- Default arguments
- Keyword arguments
- Variable-length arguments
- Local and global scope
- Lambda functions
- Practical function-based programs

---

# 1. What is a Function?

A **function** is a reusable block of code designed to perform a specific task.

Instead of writing the same code repeatedly, we can write it once inside a function and reuse it whenever needed.

### Without a Function

```python
name = "Karthik"
print("Hello", name)

name = "Rahul"
print("Hello", name)

name = "Priya"
print("Hello", name)
```

### With a Function

```python
def greet(name):
    print("Hello", name)

greet("Karthik")
greet("Rahul")
greet("Priya")
```

Output:

```text
Hello Karthik
Hello Rahul
Hello Priya
```

---

# 2. Why Use Functions?

Functions provide:

✅ Code reusability

✅ Better organization

✅ Easier debugging

✅ Reduced code duplication

✅ Better readability

---

# 3. Defining a Function

The `def` keyword is used to create a function.

## Syntax

```python
def function_name():
    # code
```

Example:

```python
def greet():
    print("Hello, Python!")
```

The function is only **defined** at this point.

To execute it, we need to call it.

---

# 4. Calling a Function

```python
def greet():
    print("Hello, Python!")

greet()
```

Output:

```text
Hello, Python!
```

---

# 5. Function with Parameters

A parameter allows us to pass information into a function.

```python
def greet(name):
    print("Hello", name)

greet("Karthik")
```

Output:

```text
Hello Karthik
```

Here:

```text
name → parameter
"Karthik" → argument
```

---

# 6. Parameters vs Arguments

### Parameter

A variable defined inside the function definition.

```python
def greet(name):
```

`name` is a parameter.

### Argument

The actual value passed when calling the function.

```python
greet("Karthik")
```

`"Karthik"` is an argument.

---

# 7. Multiple Parameters

A function can have multiple parameters.

```python
def add(a, b):
    print(a + b)

add(10, 20)
```

Output:

```text
30
```

Another example:

```python
def student(name, age, department):
    print("Name:", name)
    print("Age:", age)
    print("Department:", department)

student("Karthik", 20, "CSE")
```

Output:

```text
Name: Karthik
Age: 20
Department: CSE
```

---

# 8. Return Statement

The `return` statement sends a value back from a function.

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

Output:

```text
30
```

---

## print() vs return

### Using print()

```python
def add(a, b):
    print(a + b)
```

This displays the result.

### Using return

```python
def add(a, b):
    return a + b
```

This gives the result back to the calling code.

We can then reuse it:

```python
result = add(10, 20)

print(result)
print(result * 2)
```

Output:

```text
30
60
```

---

# 9. Function Without return

If a function doesn't explicitly return a value, Python returns `None`.

```python
def greet():
    print("Hello")

result = greet()

print(result)
```

Output:

```text
Hello
None
```

---

# 10. Returning Multiple Values

Python allows a function to return multiple values.

```python
def calculate(a, b):
    return a + b, a - b, a * b

result = calculate(10, 5)

print(result)
```

Output:

```text
(15, 5, 50)
```

The returned values are packed into a tuple.

We can unpack them:

```python
def calculate(a, b):
    return a + b, a - b, a * b

addition, subtraction, multiplication = calculate(10, 5)

print(addition)
print(subtraction)
print(multiplication)
```

Output:

```text
15
5
50
```

---

# 11. Default Arguments

A default argument has a predefined value.

```python
def greet(name="User"):
    print("Hello", name)

greet()
greet("Karthik")
```

Output:

```text
Hello User
Hello Karthik
```

If no argument is provided, `"User"` is used.

---

# 12. Multiple Default Arguments

```python
def student(name, department="CSE"):
    print("Name:", name)
    print("Department:", department)

student("Karthik")
student("Rahul", "ECE")
```

Output:

```text
Name: Karthik
Department: CSE

Name: Rahul
Department: ECE
```

---

# 13. Keyword Arguments

We can specify the parameter name while calling a function.

```python
def student(name, age):
    print(name, age)

student(age=20, name="Karthik")
```

Output:

```text
Karthik 20
```

The order does not matter when using keyword arguments.

---

# 14. Positional Arguments

Arguments can also be passed according to their position.

```python
def student(name, age):
    print(name, age)

student("Karthik", 20)
```

Here:

```text
"Karthik" → name
20        → age
```

---

# 15. *args

`*args` allows a function to accept any number of positional arguments.

```python
def add(*numbers):
    print(numbers)

add(10, 20, 30, 40)
```

Output:

```text
(10, 20, 30, 40)
```

Inside the function, `numbers` is a tuple.

## Example

```python
def add(*numbers):
    total = 0

    for number in numbers:
        total += number

    return total

print(add(10, 20))
print(add(10, 20, 30))
print(add(1, 2, 3, 4, 5))
```

Output:

```text
30
60
15
```

---

# 16. **kwargs

`**kwargs` allows a function to accept any number of keyword arguments.

```python
def student(**details):
    print(details)

student(
    name="Karthik",
    age=20,
    department="CSE"
)
```

Output:

```text
{'name': 'Karthik', 'age': 20, 'department': 'CSE'}
```

Inside the function, `details` is a dictionary.

## Looping Through **kwargs

```python
def student(**details):
    for key, value in details.items():
        print(key, ":", value)

student(
    name="Karthik",
    age=20,
    department="CSE"
)
```

Output:

```text
name : Karthik
age : 20
department : CSE
```

---

# 17. Scope of Variables

Scope determines where a variable can be accessed.

There are two important scopes for now:

- Local scope
- Global scope

---

# Local Variable

A variable created inside a function is local to that function.

```python
def test():
    x = 10
    print(x)

test()
```

Output:

```text
10
```

But:

```python
def test():
    x = 10

test()

print(x)
```

This causes:

```text
NameError
```

because `x` exists only inside the function.

---

# Global Variable

A variable created outside a function is global.

```python
x = 10

def test():
    print(x)

test()
```

Output:

```text
10
```

The function can access the global variable.

---

# 18. Global Keyword

The `global` keyword allows a function to modify a global variable.

```python
count = 0

def increase():
    global count
    count += 1

increase()

print(count)
```

Output:

```text
1
```

Use `global` carefully. In larger programs, passing values through function parameters is usually easier to maintain.

---

# 19. Lambda Functions

A lambda is a small anonymous function.

## Syntax

```python
lambda arguments: expression
```

Example:

```python
square = lambda x: x * x

print(square(5))
```

Output:

```text
25
```

---

## Normal Function vs Lambda

### Normal Function

```python
def square(x):
    return x * x
```

### Lambda

```python
square = lambda x: x * x
```

Both perform the same operation.

---

# Lambda with Multiple Arguments

```python
add = lambda a, b: a + b

print(add(10, 20))
```

Output:

```text
30
```

---

# 20. Functions with Conditions

Functions can contain conditional statements.

```python
def check_number(number):
    if number > 0:
        return "Positive"
    elif number < 0:
        return "Negative"
    else:
        return "Zero"

print(check_number(10))
print(check_number(-5))
print(check_number(0))
```

Output:

```text
Positive
Negative
Zero
```

---

# 21. Functions with Loops

Functions can also contain loops.

```python
def print_numbers(n):
    for i in range(1, n + 1):
        print(i)

print_numbers(5)
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

# 22. Function Calling Another Function

Functions can call other functions.

```python
def square(number):
    return number * number


def display(number):
    result = square(number)
    print("Square:", result)


display(5)
```

Output:

```text
Square: 25
```

---

# 23. Recursive Functions

A function that calls itself is called a **recursive function**.

Example: Factorial

```python
def factorial(n):
    if n == 0:
        return 1

    return n * factorial(n - 1)

print(factorial(5))
```

Output:

```text
120
```

The concept of recursion will be explored more deeply later.

---


### Key Takeaways

✅ Functions are reusable blocks of code.

✅ `def` is used to define a function.

✅ A function is executed when it is called.

✅ Parameters receive values inside a function.

✅ Arguments are the actual values passed to a function.

✅ `return` sends a value back from a function.

✅ Default arguments provide fallback values.

✅ Keyword arguments allow arguments to be passed using parameter names.

✅ `*args` accepts multiple positional arguments.

✅ `**kwargs` accepts multiple keyword arguments.

✅ Local variables exist inside their function.

✅ Global variables are defined outside functions.

✅ Lambda functions are useful for small, simple operations.

✅ Functions make programs modular, reusable, and easier to maintain.

---
