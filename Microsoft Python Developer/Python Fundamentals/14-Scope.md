# Variable Scope
Variable scope defines the region of your code where a particular variable is accessible or can be used.  Think of it as the variable's "visibility zone."  Python has two main types of scope:

1. **Local Scope:**
   - Variables declared *inside* a function have local scope.
   - They are only accessible within that specific function.
   - They are created when the function is called and destroyed when the function finishes executing.
   - This is like having separate workspaces for different tasks – tools in one workspace don't interfere with tools in another.

2. **Global Scope:**
   - Variables declared *outside* any function have global scope.
   - They are accessible from anywhere in your code, both inside and outside functions.
   - They exist for the entire duration of your program's execution.
   - Think of this as a shared resource accessible by everyone.

## Why is Scope Important?

* **Organization and Readability:** Local scope helps keep your code organized by preventing accidental modification of variables from different parts of the program. This makes your code easier to understand and maintain.  Each function has its own isolated environment.


* **Preventing Naming Conflicts:** You can use the same variable name in different functions without causing conflicts because they are treated as separate local variables.


* **Memory Management:**  Local variables are automatically deleted when the function finishes, freeing up memory.

## Caution with Global Variables

While global variables can be useful for storing information that needs to be accessed throughout your program, overuse can lead to problems:

* **Increased Risk of Errors:**  Modifying a global variable in one function can have unintended side effects in other parts of your code that rely on that variable.  This makes debugging more difficult.
* **Reduced Code Maintainability:** It becomes harder to understand and maintain code when global variables are frequently modified in different places.  It's harder to track where changes are being made.

## Example

```python
global_var = 10  # Global variable


def my_function():
    local_var = 5  # Local variable
    print(global_var)  # Accessing a global variable inside a function is allowed.
    print(local_var) # Output:5


my_function()  #Output :10
print(global_var)  # Output: 10
#print(local_var)  # This will cause an error! local_var is not accessible outside the function.



def modify_global():
      global global_var #use global keyword to modify the global variable inside the function. otherwise, it will be treated as local variable
      global_var = 20

modify_global()
print(global_var) #output 20
```

## Best Practice

* **Favor local variables:** Use local variables whenever possible to keep your code modular and reduce the risk of errors.
* **Minimize the use of global variables:**  Only use global variables when absolutely necessary for data that truly needs to be accessed throughout your program.  Consider alternative approaches like passing data as arguments to functions.
* **Use meaningful variable names:** This helps clarify the purpose and scope of your variables.

## LEGB Rule: Python's Search Order

When you use a variable, Python searches for it in this order:

- **L**ocal: Inside the current function or block.
- **E**nclosing function locals: If the variable is not found locally, Python searches the local scopes of any enclosing (outer) functions.
- **G**lobal: At the top level of the module (file).
- **B**uilt-in: Predefined Python names (e.g., print, len, list). These are essentially global but defined by Python itself.

## Nested Scopes

Functions can be nested inside other functions. Inner functions have access to variables in their own local scope, as well as the local scopes of any enclosing functions and the global scope. (Workers in a smaller room can access tools in that room, the larger room it is in, and the main warehouse area).

## Modifying Global Variables

Use the global keyword inside a function to indicate that you want to modify a global variable. Modifying global variables can make code harder to understand and debug. Use with care. Often, it's better to pass the global variable as an argument to the function and return a modified value.

---# Variable Scope

