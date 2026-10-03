# Day 14: Exception Handling in Python

Exception handling allows Python programs to handle unexpected problems without crashing.

---

## 🎯 Learning Objectives

By the end of Day 14, you will understand:

- What errors are
- Types of errors in Python
- What exceptions are
- Difference between errors and exceptions
- Why exception handling is important
- `try`, `except`, `else`, and `finally`
- Handling specific and multiple exceptions
- Getting exception messages
- The `raise` keyword
- Custom exceptions
- Nested exception handling
- Exception handling with functions and user input
- Real-world applications
- How to write reliable Python programs

---

# 1. What is an Error?

An **error** is a problem in a program that prevents it from working correctly.

```python
print("Hello"
```

Output:

```text
SyntaxError: '(' was never closed
```

---

# 2. Why Do Errors Occur?

Errors can occur because of:

- Incorrect syntax
- Invalid input
- Wrong data type
- Missing files
- Invalid calculations
- Accessing unavailable data
- Programming mistakes

```python
age = int(input("Enter age: "))
```

If the user enters `abc`, Python cannot convert it into an integer.

---

# 3. Types of Errors

Python errors can broadly be classified as:

1. Syntax Errors
2. Runtime Errors
3. Logical Errors
4. Exceptions

---

# 4. Syntax Error

A syntax error occurs when Python cannot understand the structure of the program.

```python
if 10 > 5
    print("Yes")
```

Correct:

```python
if 10 > 5:
    print("Yes")
```

Syntax errors must be fixed before the program can execute.

---

# 5. Runtime Error

A runtime error occurs while the program is running.

```python
a = 10
b = 0

print(a / b)
```

Output:

```text
ZeroDivisionError: division by zero
```

---

# 6. Logical Error

A logical error occurs when the program runs but produces the wrong result.

```python
a = 10
b = 20

average = a + b / 2
```

Correct:

```python
average = (a + b) / 2
```

Logical errors are often harder to detect because Python does not automatically report them.

---

# 7. What is an Exception?

An **exception** is an unexpected event that occurs while a program is running.

```python
num = int("hello")
```

Output:

```text
ValueError
```

Another example:

```python
10 / 0
```

Output:

```text
ZeroDivisionError
```

---

# 8. Why Do We Need Exception Handling?

Without exception handling:

```python
num = int(input("Enter a number: "))
print(100 / num)
```

If the user enters `0`, the program crashes.

With exception handling:

```python
try:
    num = int(input("Enter a number: "))
    print(100 / num)

except ZeroDivisionError:
    print("Cannot divide by zero.")
```

---

# 9. try and except

Basic structure:

```python
try:
    # Code that may cause an exception

except:
    # Code that handles the exception
```

Example:

```python
try:
    number = int(input("Enter a number: "))
    print(number)

except:
    print("Invalid input")
```

---

# 10. Handling a Specific Exception

It is better to handle specific exceptions.

```python
try:
    number = int(input("Enter a number: "))

except ValueError:
    print("Please enter a valid number.")
```

---

# 11. ZeroDivisionError

```python
try:
    result = 10 / 0

except ZeroDivisionError:
    print("Cannot divide by zero.")
```

---

# 12. Multiple except Blocks

```python
try:
    number = int(input("Enter a number: "))
    result = 100 / number
    print(result)

except ValueError:
    print("Please enter a valid integer.")

except ZeroDivisionError:
    print("Cannot divide by zero.")
```

---

# 13. else Block

The `else` block executes when no exception occurs.

```python
try:
    number = int(input("Enter a number: "))

except ValueError:
    print("Invalid input.")

else:
    print("You entered:", number)
```

---

# 14. finally Block

The `finally` block always executes.

```python
try:
    number = int(input("Enter number: "))
    print(number)

except ValueError:
    print("Invalid input.")

finally:
    print("Program finished.")
```

---

# 15. try + except + else + finally

```python
try:
    number = int(input("Enter a number: "))
    result = 100 / number

except ValueError:
    print("Invalid input.")

except ZeroDivisionError:
    print("Cannot divide by zero.")

else:
    print("Result:", result)

finally:
    print("Execution completed.")
```

Execution flow:

```text
try
 ↓
Exception?
 ↓
Yes → except
 ↓
No → else
 ↓
finally
```

---

# 16. Common Python Exceptions

| Exception | Meaning |
|---|---|
| `ValueError` | Invalid value |
| `TypeError` | Wrong data type |
| `ZeroDivisionError` | Division by zero |
| `IndexError` | Invalid list index |
| `KeyError` | Missing dictionary key |
| `NameError` | Variable does not exist |
| `FileNotFoundError` | File does not exist |
| `AttributeError` | Invalid attribute |
| `ImportError` | Import problem |

---

# 17. ValueError

```python
try:
    age = int("twenty")

except ValueError:
    print("Age must be a number.")
```

---

# 18. TypeError

```python
try:
    result = 10 + "20"

except TypeError:
    print("Cannot add integer and string.")
```

---

# 19. IndexError

```python
numbers = [10, 20, 30]

try:
    print(numbers[5])

except IndexError:
    print("Index does not exist.")
```

---

# 20. KeyError

```python
student = {
    "name": "Rahul",
    "age": 20
}

try:
    print(student["marks"])

except KeyError:
    print("Marks key does not exist.")
```

---

# 21. NameError

```python
try:
    print(name)

except NameError:
    print("Variable does not exist.")
```

---

# 22. FileNotFoundError

```python
try:
    file = open("data.txt")

except FileNotFoundError:
    print("File not found.")
```

---

# 23. AttributeError

```python
number = 10

try:
    number.append(20)

except AttributeError:
    print("This object does not have append().")
```

---

# 24. Getting the Exception Message

Use `as` to store the exception.

```python
try:
    number = int("abc")

except ValueError as error:
    print("Error:", error)
```

Syntax:

```python
except ExceptionType as error:
```

---

# 25. Multiple Exceptions in One except

```python
try:
    number = int(input("Enter number: "))
    result = 100 / number

except (ValueError, ZeroDivisionError):
    print("Invalid input or division by zero.")
```

---

# 26. General Exception

```python
try:
    number = int(input("Enter number: "))

except Exception as error:
    print("Something went wrong:", error)
```

Prefer specific exceptions whenever possible.

---

# 27. The raise Keyword

`raise` manually creates an exception.

```python
age = 15

if age < 18:
    raise ValueError("Age must be 18 or above.")
```

---

# 28. raise with try and except

```python
try:
    age = 15

    if age < 18:
        raise ValueError("You must be 18 or older.")

except ValueError as error:
    print(error)
```

---

# 29. Custom Exceptions

Create your own exception classes by inheriting from `Exception`.

```python
class AgeError(Exception):
    pass
```

---

# 30. Custom Exception Example

```python
class AgeError(Exception):
    pass

age = 15

try:
    if age < 18:
        raise AgeError("Age must be 18 or above.")

except AgeError as error:
    print(error)
```

Custom exceptions are useful in larger applications.

---

# 31. Exception Handling with Functions

```python
def divide(a, b):

    try:
        return a / b

    except ZeroDivisionError:
        return "Cannot divide by zero."

print(divide(10, 2))
print(divide(10, 0))
```

---

# 32. Exception Handling with User Input

```python
try:
    age = int(input("Enter your age: "))
    print("Your age is:", age)

except ValueError:
    print("Please enter a valid number.")
```

---

# 33. Safe Calculator

```python
try:
    a = float(input("Enter first number: "))
    operator = input("Enter operator (+ - * /): ")
    b = float(input("Enter second number: "))

    if operator == "+":
        print(a + b)

    elif operator == "-":
        print(a - b)

    elif operator == "*":
        print(a * b)

    elif operator == "/":
        print(a / b)

    else:
        print("Invalid operator.")

except ValueError:
    print("Please enter valid numbers.")

except ZeroDivisionError:
    print("Cannot divide by zero.")
```

---

# 34. Handling List Access

```python
numbers = [10, 20, 30]

try:
    index = int(input("Enter index: "))
    print(numbers[index])

except ValueError:
    print("Index must be a number.")

except IndexError:
    print("Invalid index.")
```

---

# 35. Handling Dictionary Search

```python
student = {
    "name": "Rahul",
    "age": 20,
    "course": "Python"
}

try:
    key = input("Enter key: ")
    print(student[key])

except KeyError:
    print("Key does not exist.")
```

---

# 36. File Handling with Exception Handling

```python
try:
    file = open("data.txt", "r")
    content = file.read()
    print(content)
    file.close()

except FileNotFoundError:
    print("File does not exist.")
```

---

# 37. finally for Cleanup

```python
file = None

try:
    file = open("data.txt", "r")
    print(file.read())

except FileNotFoundError:
    print("File not found.")

finally:
    if file:
        file.close()

    print("File operation completed.")
```

---

# 38. Nested try-except

```python
try:
    number = int(input("Enter number: "))

    try:
        result = 100 / number
        print(result)

    except ZeroDivisionError:
        print("Cannot divide by zero.")

except ValueError:
    print("Invalid number.")
```

---

# 39. Practical Example – Student Marks

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

# 40. Practical Example – Age Validation

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

# 41. Practical Example – Login System

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

# 48. Exception Handling Best Practices

### 1. Handle specific exceptions

Prefer:

```python
except ValueError:
```

instead of:

```python
except:
```

### 2. Keep try blocks small

Avoid putting the entire program inside one huge `try` block.

### 3. Use meaningful error messages

```python
print("Age must be a positive number.")
```

is better than:

```python
print("Error")
```

### 4. Don't hide errors unnecessarily

Avoid:

```python
try:
    something()
except:
    pass
```

### 5. Use finally for cleanup

Use `finally` when something must happen regardless of success or failure.

---

# 49. Exception Handling Flow

```text
             Start
               |
               v
             try
               |
        +------+------+
        |             |
    Exception?       No
        |             |
       Yes            v
        |            else
        v             |
      except          |
        |             |
        +------+------+
               |
               v
            finally
               |
               v
              End
```

---

# 50. Exception Handling Structure

Basic:

```python
try:
    risky_code()

except ExceptionType:
    handle_error()
```

With `else`:

```python
try:
    risky_code()

except ExceptionType:
    handle_error()

else:
    success_code()
```

With `finally`:

```python
try:
    risky_code()

except ExceptionType:
    handle_error()

else:
    success_code()

finally:
    cleanup()
```

---

# 51. Important Keywords

| Keyword | Purpose |
|---|---|
| `try` | Contains risky code |
| `except` | Handles exceptions |
| `else` | Runs if no exception occurs |
| `finally` | Always runs |
| `raise` | Manually raises an exception |

---

# 52. Real-World Applications

Exception handling is used in:

- Banking systems
- ATM systems
- Login systems
- E-commerce applications
- Database applications
- File processing
- APIs
- Web applications
- Data processing
- Machine learning applications
- Automation scripts
- Payment systems

---

# 53. Exception Handling vs if-else

`if-else` handles expected conditions.

```python
age = 20

if age >= 18:
    print("Eligible")
else:
    print("Not eligible")
```

Exception handling handles unexpected runtime problems.

```python
try:
    age = int(input("Enter age: "))

except ValueError:
    print("Invalid input.")
```

| if-else | Exception Handling |
|---|---|
| Handles conditions | Handles exceptions |
| Normal program flow | Unexpected runtime problems |
| Checks conditions | Handles runtime exceptions |

---

# 54. Common Mistakes

### Mistake 1: Using empty except

```python
try:
    something()

except:
    pass
```

### Mistake 2: Catching everything

```python
except Exception:
    print("Error")
```

Use specific exceptions when possible.

### Mistake 3: Putting too much code inside try

Keep the `try` block focused.

### Mistake 4: Ignoring the error message

```python
except ValueError as error:
    print(error)
```

---

# 64. Key Takeaways

✅ Errors are problems that occur in a program.

✅ Syntax errors happen when Python cannot understand the program structure.

✅ Runtime errors occur while the program is executing.

✅ Logical errors produce incorrect results without necessarily crashing the program.

✅ Exceptions are runtime events that can interrupt normal program execution.

✅ `try` contains code that may cause an exception.

✅ `except` handles the exception.

✅ `else` runs when no exception occurs.

✅ `finally` always executes.

✅ `raise` is used to manually raise an exception.

✅ Python provides built-in exceptions such as `ValueError`, `TypeError`, `IndexError`, `KeyError`, and `ZeroDivisionError`.

✅ Specific exceptions should be handled whenever possible.

✅ Custom exceptions can be created by inheriting from `Exception`.

✅ Exception handling makes programs more reliable and user-friendly.

---

- Challenge Project

---
