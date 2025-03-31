# Virtual Environments

Sometimes, you might need to use `pip3` instead of pip, especially if you have both Python 2 and Python 3 installed on your system. `pip3` ensures you're installing the library for Python 3. It's also good practice to use a virtual environment.

It's highly recommended to use virtual environments when working with Python projects. A virtual environment is an isolated space for your project's dependencies. This prevents conflicts between different projects that might require different versions of the same library.

To create a virtual environment (using the built-in `venv` module):

``` Python
python3 -m venv .venv  # Creates a virtual environment named ".venv" (you can choose any name)
```

To activate the virtual environment:

- **macOS/Linux:** source .venv/bin/activate
- **Windows:** .venv\Scripts\activate    

Once activated, any libraries you install with pip will be installed within the virtual environment, keeping your global Python installation clean. 
