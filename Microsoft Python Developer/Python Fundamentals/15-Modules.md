# Modules in Python

As your Python projects grow, they can quickly become large and complex. Imagine a single file containing thousands of lines of code! It would be incredibly difficult to find specific parts, understanding how each part works, making changes, reusing code. Modules are the perfect way to solve these problems.

A module is simply a file containing Python code that you can import into your project and use the functions of that module without writing your own. By breaking your code into modules, you achieve better organization and maintainability. You can also import the module in another project and make the code reusable.
## Creating and Using Modules
Creating a module is incredibly simple: just create a new file with a `.py` extension.  

```python
# my_math.py

PI = 3.14159  # A constant

def add(x, y):
  """Adds two numbers together."""
  return x + y

def subtract(x, y):
  """Subtracts y from x."""
  return x - y

def circle_area(radius):
  """Calculates the area of a circle."""
  return PI * (radius ** 2)

class Calculator:
    """Performs basic calculations"""
    def multiply(self, x, y):
        return x * y
```

To use the code defined in a module, you use the `import` statement. There are several ways to do this:

1.  **Importing the Entire Module:**

    ```python
    # main.py
    import my_math

    result = my_math.add(5, 3)  # Access functions using module_name.function_name
    print(result)  # Output: 8

    area = my_math.circle_area(4)
    print(area)  # Output: 50.26544

    my_calc = my_math.Calculator()
    print(my_calc.multiply(3,9)) # Output: 27
    ```

2.  **Importing Specific Items:**

    ```python
    # main.py
    from my_math import add, circle_area

    result = add(10, 2)  # No need for my_math. prefix
    print(result)  # Output: 12

    area = circle_area(2)
    print(area)  # Output: 12.56636
    
    #subtract(5,2) #this would produce an error, since we haven't imported it
    ```

3.  **Importing with an Alias:**

    ```python
    # main.py
    import my_math as mm  # Give the module a shorter alias

    result = mm.add(7, 1)
    print(result)  # Output: 8

    # You can also use aliases with 'from' imports:
    from my_math import circle_area as ca
    print(ca(3)) # Output: 28.27431
    ```

4. **Importing everything (Generally Discouraged):**

    ```python
    from my_math import *
    ```

> [!Warning]
> This imports *everything* from `my_math` without requiring the prefix.  **However, this is generally discouraged** because it can lead to naming conflicts and make it harder to understand where functions are coming from. It's best to be explicit about what you're importing.

## Standard Library Modules
Python comes with a vast "standard library" of built-in modules.  You don't need to install these; they're already available.  Some common examples:

*   `math`:  Mathematical functions (e.g., `math.sqrt`, `math.sin`, `math.pi`).
*   `random`:  Generating random numbers (e.g., `random.randint`, `random.choice`).
*   `datetime`:  Working with dates and times.
*   `os`:  Interacting with the operating system (e.g., listing files, creating directories).
*   `sys`: System-specific parameters and functions.
* `json`: Working with JSON files.

```python
import math
import random

print(math.sqrt(16))  # Output: 4.0
print(random.randint(1, 10))  # Output: A random integer between 1 and 10
```

## Third-Party Modules (Packages)
Beyond the standard library, there's a massive ecosystem of "third-party" modules (also called "packages") created by other developers.  You can install these using a package manager called `pip`.

```bash
pip install requests
```

Then, in your Python code:

```python
import requests

response = requests.get("https://www.google.com")
print(response.status_code)  # Output: 200 (usually means success)
# print(response.text) # Would print the HTML content of Google's homepage
```
