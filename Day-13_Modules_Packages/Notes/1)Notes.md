# Day 13 – Modules & Packages in Python

## 1. What is a Module?

A **module** is a Python file containing reusable code such as functions, variables, classes, and statements.

Example:

```text
math_tools.py
```

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

A module allows us to reuse this code in another Python file.

---

## 2. Why Do We Use Modules?

Modules help us:

- Avoid repeating code
- Reuse functions
- Organize large programs
- Make programs easier to maintain
- Divide a large project into smaller files

Example project:

```text
project/
├── main.py
├── calculator.py
└── student.py
```

---

## 3. Creating Your Own Module

Create a file called:

```text
calculator.py
```

```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

Create another file called:

```text
main.py
```

---

## 4. Importing a Module

We use `import` to use a module.

### Syntax

```python
import module_name
```

### Example

```python
import calculator

print(calculator.add(10, 5))
print(calculator.subtract(10, 5))
```

### Output

```text
15
5
```

---

## 5. Importing Specific Functions

We can import only the functions we need.

### Syntax

```python
from module_name import function_name
```

### Example

```python
from calculator import add

print(add(20, 10))
```

### Output

```text
30
```

---

## 6. Importing Multiple Functions

```python
from calculator import add, subtract

print(add(10, 5))
print(subtract(10, 5))
```

### Output

```text
15
5
```

---

## 7. Import Everything from a Module

```python
from calculator import *

print(add(5, 3))
print(subtract(5, 3))
```

### Output

```text
8
2
```

`import *` is generally avoided in larger projects because it can make it unclear where names came from.

---

## 8. Using an Alias

We can give a module a shorter name using `as`.

### Syntax

```python
import module_name as alias
```

### Example

```python
import calculator as calc

print(calc.add(10, 20))
```

### Output

```text
30
```

---

## 9. Built-in Modules

Python provides many useful modules.

| Module | Purpose |
|---|---|
| `math` | Mathematical operations |
| `random` | Random values |
| `datetime` | Date and time |
| `os` | Operating-system operations |
| `statistics` | Statistical calculations |

---

# 10. The `math` Module

The `math` module provides mathematical functions and constants.

```python
import math
```

### `math.sqrt()`

```python
import math

print(math.sqrt(25))
```

Output:

```text
5.0
```

### `math.pow()`

```python
import math

print(math.pow(2, 3))
```

Output:

```text
8.0
```

### `math.ceil()`

Rounds upward.

```python
import math

print(math.ceil(4.2))
```

Output:

```text
5
```

### `math.floor()`

Rounds downward.

```python
import math

print(math.floor(4.8))
```

Output:

```text
4
```

### `math.factorial()`

```python
import math

print(math.factorial(5))
```

Output:

```text
120
```

### `math.pi`

```python
import math

print(math.pi)
```

Output:

```text
3.141592653589793
```

### `math.e`

```python
import math

print(math.e)
```

---

# 11. The `random` Module

The `random` module is used to generate random values.

```python
import random
```

### `random.randint()`

```python
import random

print(random.randint(1, 10))
```

Possible output:

```text
7
```

The output can be different each time.

### `random.random()`

Generates a random floating-point number between `0` and `1`.

```python
import random

print(random.random())
```

Possible output:

```text
0.583421
```

### `random.choice()`

Selects a random item from a sequence.

```python
import random

names = ["Karthik", "Rahul", "Anu", "Priya"]

print(random.choice(names))
```

Possible output:

```text
Anu
```

---

# 12. The `datetime` Module

The `datetime` module is used to work with dates and times.

```python
import datetime
```

### Current Date and Time

```python
import datetime

now = datetime.datetime.now()

print(now)
```

Possible output:

```text
2026-09-30 19:25:43.123456
```

### Today's Date

```python
import datetime

today = datetime.date.today()

print(today)
```

Possible output:

```text
2026-09-30
```

### Creating a Specific Date

```python
import datetime

date = datetime.date(2026, 10, 15)

print(date)
```

Output:

```text
2026-10-15
```

### Accessing Date Components

```python
import datetime

today = datetime.date.today()

print(today.year)
print(today.month)
print(today.day)
```

---

# 13. Importing Specific Parts from `datetime`

```python
from datetime import date

today = date.today()

print(today)
```

This allows us to use `date` directly.

---

# 14. Creating Your Own Module

Create:

```text
student.py
```

```python
def welcome(name):
    print("Welcome", name)

def calculate_average(m1, m2, m3):
    return (m1 + m2 + m3) / 3
```

Now create:

```text
main.py
```

```python
import student

student.welcome("Karthik")

average = student.calculate_average(80, 90, 85)

print("Average:", average)
```

Output:

```text
Welcome Karthik
Average: 85.0
```

---

# 15. Importing Your Own Functions

### `student.py`

```python
def calculate_average(m1, m2, m3):
    return (m1 + m2 + m3) / 3
```

### `main.py`

```python
from student import calculate_average

average = calculate_average(80, 90, 85)

print(average)
```

Output:

```text
85.0
```

---

# 16. Modules with Variables

A module can also contain variables.

### `college.py`

```python
college_name = "ABC College"
location = "Hyderabad"
```

### `main.py`

```python
import college

print(college.college_name)
print(college.location)
```

Output:

```text
ABC College
Hyderabad
```

---

# 17. Modules with Functions and Variables

### `college.py`

```python
college_name = "ABC College"

def welcome():
    print("Welcome to", college_name)
```

### `main.py`

```python
import college

college.welcome()
```

Output:

```text
Welcome to ABC College
```

---

# 18. What is a Package?

A **package** is a folder used to organize multiple Python modules.

Example:

```text
myproject/
├── main.py
└── utilities/
    ├── calculator.py
    ├── student.py
    └── marks.py
```

Here, `utilities` is the package.

---

# 19. Creating a Package

Example:

```text
project/
├── main.py
└── tools/
    ├── __init__.py
    ├── calculator.py
    └── message.py
```

### `calculator.py`

```python
def add(a, b):
    return a + b
```

### `message.py`

```python
def welcome(name):
    print("Welcome", name)
```

### `main.py`

```python
from tools.calculator import add
from tools.message import welcome

welcome("Karthik")

print(add(10, 20))
```

Output:

```text
Welcome Karthik
30
```

---

# 20. What is `__init__.py`?

A file named:

```text
__init__.py
```

is commonly placed inside a regular Python package.

Example:

```text
tools/
├── __init__.py
├── calculator.py
└── message.py
```

It can be used for package initialization and package-level code.

Modern Python can also use namespace packages without this file, but `__init__.py` is still very common.

---

# 21. Importing from a Package

Suppose:

```text
tools/
├── __init__.py
└── calculator.py
```

`calculator.py`:

```python
def add(a, b):
    return a + b
```

Import it using:

```python
from tools.calculator import add

print(add(10, 5))
```

Output:

```text
15
```

---

# 22. Module vs Package

| Module | Package |
|---|---|
| Usually a single `.py` file | Usually a directory containing modules |
| Contains functions, variables, classes, etc. | Organizes multiple modules |
| Example: `calculator.py` | Example: `tools/` |
| Useful for code reuse | Useful for larger project organization |

---

# 23. Standard Library vs Third-Party Libraries

Python provides a large standard library.

Examples:

```text
math
random
datetime
os
statistics
```

Third-party libraries are installed separately.

Examples:

```text
numpy
pandas
matplotlib
requests
```

They can commonly be installed using:

```bash
pip install package_name
```

For example:

```bash
pip install pandas
```

---

# 31. Key Takeaways

### Key Takeaways

✅ A **module** is a Python file containing reusable code.

✅ `import` is used to import a module.

✅ `from ... import ...` is used to import specific functions or objects.

✅ `as` can be used to create an alias for a module.

✅ Python provides built-in modules such as `math`, `random`, and `datetime`.

✅ The `math` module is useful for mathematical operations.

✅ The `random` module is useful for generating random values.

✅ The `datetime` module is useful for working with dates and times.

✅ We can create our own modules to organize reusable code.

✅ A **package** is used to organize multiple Python modules.

✅ `__init__.py` is commonly used in regular Python packages.

✅ Modules and packages make large Python projects easier to organize and maintain.

---

