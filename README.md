[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/WfNmjXUk)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15316416&assignment_repo_type=AssignmentRepo)
# SE-Assignment-6
 Assignment: Introduction to Python
Instructions:
Answer the following questions based on your understanding of Python programming. Provide detailed explanations and examples where appropriate.

 Questions:

1. Python Basics:
   - What is Python, and what are some of its key features that make it popular among developers? Provide examples of use cases where Python is particularly effective.

 What is Python?

Python is a high-level, interpreted programming language known for its readability, simplicity, and flexibility. It was created by Guido van Rossum and first released in 1991. Python supports multiple programming paradigms, including procedural, object-oriented, and functional programming.

 Key Features of Python

1. Readability and Simplicity:
    Python's syntax is designed to be easy to read and write, which makes it an excellent choice for beginners and for rapid development.
    Example:
     ```python
     def greet(name):
         print(f"Hello, {name}!")

     greet("Alice")
     ```

2. Interpreted Language:
    Python code is executed line-by-line, which makes debugging easier and allows for quick testing and prototyping.
    Example:
     ```python
     print("This will run immediately")
     ```

3. Dynamic Typing:
    Variables in Python do not need explicit declaration to reserve memory space. The declaration happens automatically when you assign a value to a variable.
    Example:
     ```python
     a = 10
     a = "Hello"
     ```

4. Extensive Standard Library:
    Python comes with a vast standard library that includes modules and packages for various tasks, such as file I/O, system calls, and web development.
    Example:
     ```python
     import math
     print(math.sqrt(16))
     ```

5. Support for Multiple Paradigms:
    Python supports procedural, object-oriented, and functional programming paradigms, making it versatile for different types of projects.
    Example (Object-Oriented):
     ```python
     class Animal:
         def __init__(self, name):
             self.name = name

         def speak(self):
             raise NotImplementedError("Subclasses must implement this method")

     class Dog(Animal):
         def speak(self):
             return "Woof!"

     my_dog = Dog("Buddy")
     print(my_dog.speak())
     ```

6. Community and Ecosystem:
    Python has a large and active community, which means plenty of resources, tutorials, and third-party modules are available.
    Example:
     ```python
     # Using the requests library for HTTP requests
     import requests

     response = requests.get('https://api.github.com')
     print(response.status_code)
     ```

 Use Cases Where Python is Particularly Effective

1. Web Development:
    Frameworks like Django and Flask make it easy to build robust and scalable web applications.
    Example (Flask):
     ```python
     from flask import Flask

     app = Flask(__name__)

     @app.route('/')
     def hello_world():
         return 'Hello, World!'

     if __name__ == '__main__':
         app.run()
     ```

2. Data Science and Machine Learning:
    Libraries like Pandas, NumPy, SciPy, TensorFlow, and scikit-learn provide powerful tools for data manipulation, analysis, and machine learning.
    Example (Pandas):
     ```python
     import pandas as pd

     data = {'Name': ['John', 'Anna', 'Peter', 'Linda'],
             'Age': [28, 24, 35, 32]}
     df = pd.DataFrame(data)
     print(df)
     ```

3. Automation and Scripting:
    Python is frequently used for writing scripts to automate repetitive tasks such as file management, web scraping, and data extraction.
    Example:
     ```python
     import os

     for filename in os.listdir('.'):
         if filename.endswith('.txt'):
             print(f"Found text file: {filename}")
     ```

4. Game Development:
    Libraries like Pygame enable the creation of simple 2D games and prototyping game ideas.
    Example:
     ```python
     import pygame

     pygame.init()
     screen = pygame.display.set_mode((640, 480))
     running = True

     while running:
         for event in pygame.event.get():
             if event.type == pygame.QUIT:
                 running = False
     pygame.quit()
     ```

5. Scientific Computing:
    Python is widely used in scientific computing due to its simplicity and the availability of specialized libraries such as SciPy and SymPy.
    Example (SciPy):
     ```python
     from scipy import stats

     data = [1, 2, 2, 3, 4, 4, 4, 5, 6]
     mode = stats.mode(data)
     print(mode)
     ```


2. Installing Python:
   - Describe the steps to install Python on your operating system (Windows, macOS, or Linux). Include how to verify the installation and set up a virtual environment.


 Installing Python on Windows

1. Download the Installer:
    Visit the official Python website: [python.org](https://www.python.org/).
    Go to the Downloads section and click on "Download Python 3.x.x" (where x.x is the latest version).

2. Run the Installer:
    Open the downloaded Python installer `.exe` file.
    In the installer window, make sure to check the box that says "Add Python to PATH". This ensures that you can use Python from the command line.
    Click "Install Now" for a simple installation, or choose "Customize installation" if you want to select specific features or install to a custom location.

3. Verify the Installation:
    Open Command Prompt (cmd).
    Type the following command and press Enter:
     ```sh
     python --version
     ```
    You should see the Python version number (e.g., `Python 3.9.1`) if the installation was successful.

4. Install pip (if not included):
    Pip, the package installer for Python, usually comes bundled with Python. To check if pip is installed, run:
     ```sh
     pip --version
     ```
    If pip is not installed, you can install it by downloading `get-pip.py` from the official [pip website](https://pip.pypa.io/en/stable/installation/).
    Run the script by typing:
     ```sh
     python get-pip.py
     ```

 Setting Up a Virtual Environment on Windows

1. Install `virtualenv` (if not included):
    Although Python 3.3+ includes the `venv` module, you can use `virtualenv` for additional features. Install `virtualenv` using pip:
     ```sh
     pip install virtualenv
     ```

2. Create a Virtual Environment:
    Navigate to your project directory in Command Prompt.
    Run the following command to create a virtual environment named `myenv`:
     ```sh
     python -m venv myenv
     ```
    This creates a directory named `myenv` with a copy of the Python interpreter and libraries.

3. Activate the Virtual Environment:
    To activate the virtual environment, run:
     ```sh
     myenv\Scripts\activate
     ```
    After activation, your command prompt will change to indicate that you are in the virtual environment (e.g., `(myenv)` will precede your prompt).

4. Verify the Virtual Environment:
    Check the Python executable location to confirm it's using the virtual environment:
     ```sh
     where python
     ```
    This should display the path to the Python executable inside your `myenv` directory.

5. Install Packages in the Virtual Environment:
    With the virtual environment activated, you can now install packages using pip. For example:
     ```sh
     pip install requests
     ```

6. Deactivate the Virtual Environment:
    To deactivate the virtual environment and return to the global Python environment, simply run:
     ```sh
     deactivate
     ```

 Example of Using a Virtual Environment on Windows

 Step-by-step example to illustrate the process:

```sh
# Open Command Prompt and navigate to your project directory
cd path\to\your\project

# Create a virtual environment named 'myenv'
python -m venv myenv

# Activate the virtual environment
myenv\Scripts\activate

# Install a package (e.g., requests)
pip install requests

# Verify installation by listing installed packages
pip list

# Deactivate the virtual environment
deactivate
```


3. Python Syntax and Semantics:
   - Write a simple Python program that prints "Hello, World!" to the console. Explain the basic syntax elements used in the program.

 Python Program: "Hello, World!"

 A simple Python program that prints "Hello, World!" to the console:

```python
print("Hello, World!")
```

 Explanation of Basic Syntax Elements

1. `print` Function:
    The `print` function is a built-in function in Python used to output text to the console.
    Syntax: `print(object(s), sep=separator, end=end, file=file, flush=flush)`
    In this program, `print("Hello, World!")` outputs the string "Hello, World!" to the console.

2. Strings:
    A string in Python is a sequence of characters enclosed in quotes. 
    Strings can be enclosed in single quotes (`'`) or double quotes (`"`).
    In this program, `"Hello, World!"` is a string enclosed in double quotes.

3. Parentheses `()`:
    Parentheses are used in Python to define the parameters of functions and methods.
    In the `print` function, the parentheses enclose the string `"Hello, World!"` which is the argument passed to the function.

4. Comments:
    Comments are not present in this simple example, but they are an essential part of Python syntax. They are used to explain code and are ignored by the Python interpreter.
    Single-line comments start with the hash character (`#`).
    Example:
     ```python
     # This is a comment
     print("Hello, World!")  # This prints "Hello, World!" to the console
     ```

 Detailed Breakdown

 Function Call:
   The `print` function is called with the string `"Hello, World!"` as its argument.
   When the function is executed, it processes the argument and outputs the string to the standard output (usually the console).

 String Argument:
   The argument to the `print` function in this case is a string.
   Strings in Python are immutable sequences of Unicode characters.

 Complete Program with Comments

Here's the same program with added comments to explain each part:

```python
# This is a simple Python program to print "Hello, World!" to the console

# The print function is called with the string "Hello, World!" as its argument
print("Hello, World!")
```


4. Data Types and Variables:
   - List and describe the basic data types in Python. Write a short script that demonstrates how to create and use variables of different data types.

 Basic Data Types in Python

Python has several built-in data types that are used to store various kinds of data. Here’s a list of some of the most common data types:

1. Integers (`int`):
    Whole numbers, positive or negative, without a decimal point.
    Example: `42`, `-3`

2. Floating-Point Numbers (`float`):
    Numbers that contain a decimal point.
    Example: `3.14`, `-0.001`

3. Strings (`str`):
    Sequences of characters enclosed in single, double, or triple quotes.
    Example: `"Hello, World!"`, `'Python'`

4. Booleans (`bool`):
    Logical values representing `True` or `False`.
    Example: `True`, `False`

5. Lists (`list`):
    Ordered, mutable collections of items, which can be of different types.
    Example: `[1, 2, 3]`, `["apple", "banana", "cherry"]`

6. Tuples (`tuple`):
    Ordered, immutable collections of items, which can be of different types.
    Example: `(1, 2, 3)`, `("apple", "banana", "cherry")`

7. Dictionaries (`dict`):
    Unordered collections of key-value pairs.
    Example: `{"name": "John", "age": 30}`, `{"fruit": "apple", "color": "red"}`

8. Sets (`set`):
    Unordered collections of unique items.
    Example: `{1, 2, 3}`, `{"apple", "banana", "cherry"}`

 Demonstrating Variables of Different Data Types


```python
# Integer
age = 25
print("Age:", age)
print("Type of age:", type(age))

# Float
height = 5.9
print("Height:", height)
print("Type of height:", type(height))

# String
name = "Alice"
print("Name:", name)
print("Type of name:", type(name))

# Boolean
is_student = True
print("Is student:", is_student)
print("Type of is_student:", type(is_student))

# List
fruits = ["apple", "banana", "cherry"]
print("Fruits:", fruits)
print("Type of fruits:", type(fruits))

# Tuple
coordinates = (10.0, 20.0)
print("Coordinates:", coordinates)
print("Type of coordinates:", type(coordinates))

# Dictionary
person = {"name": "Bob", "age": 25}
print("Person:", person)
print("Type of person:", type(person))

# Set
unique_numbers = {1, 2, 3, 3, 2, 1}
print("Unique numbers:", unique_numbers)
print("Type of unique_numbers:", type(unique_numbers))
```

 Explanation of the Script

 Integer:
   Variable `age` is assigned an integer value `25`.
   `print` statements display the value and type of `age`.

 Float:
   Variable `height` is assigned a floating-point number `5.9`.
   `print` statements display the value and type of `height`.

 String:
   Variable `name` is assigned a string value `"Alice"`.
   `print` statements display the value and type of `name`.

 Boolean:
   Variable `is_student` is assigned a boolean value `True`.
   `print` statements display the value and type of `is_student`.

 List:
   Variable `fruits` is assigned a list of strings `["apple", "banana", "cherry"]`.
   `print` statements display the value and type of `fruits`.

 Tuple:
   Variable `coordinates` is assigned a tuple `(10.0, 20.0)`.
   `print` statements display the value and type of `coordinates`.

 Dictionary:
   Variable `person` is assigned a dictionary with keys `"name"` and `"age"`, and their corresponding values.
   `print` statements display the value and type of `person`.

 Set:
   Variable `unique_numbers` is assigned a set `{1, 2, 3, 3, 2, 1}`. Duplicate values are automatically removed.
   `print` statements display the value and type of `unique_numbers`.


5. Control Structures:
   - Explain the use of conditional statements and loops in Python. Provide examples of an `if-else` statement and a `for` loop.

 Control Structures in Python

Control structures in Python allow you to control the flow of execution in your programs. The two main types of control structures are conditional statements and loops.

 Conditional Statements

Conditional statements allow you to execute certain parts of your code based on specific conditions. The primary conditional statements in Python are `if`, `elif`, and `else`.

 Example of an `if-else` Statement


```python
# Define a variable
age = 18

# Conditional statement
if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

 Explanation

 `if` Statement:
   The `if` statement checks whether the condition `age >= 18` is true.
   If the condition is true, the indented block of code under the `if` statement is executed, printing "You are an adult."

 `else` Statement:
   The `else` statement is executed if the condition in the `if` statement is false.
   If `age` is less than 18, the indented block of code under the `else` statement is executed, printing "You are a minor."

 Loops

Loops allow you to execute a block of code repeatedly. The two main types of loops in Python are `for` loops and `while` loops.

 Example of a `for` Loop

Here’s a simple example demonstrating the use of a `for` loop:

```python
# Define a list of fruits
fruits = ["apple", "banana", "cherry"]

# For loop to iterate over the list
for fruit in fruits:
    print(fruit)
```

 Explanation

 `for` Loop:
   The `for` loop iterates over each item in the `fruits` list.
   The variable `fruit` takes on the value of each item in the list one by one.
   The indented block of code under the `for` loop is executed for each item in the list, printing the name of each fruit.

 Combining Conditional Statements and Loops


```python
# Define a list of numbers
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# For loop to iterate over the list
for number in numbers:
    # Conditional statement to check if the number is even or odd
    if number % 2 == 0:
        print(f"{number} is even.")
    else:
        print(f"{number} is odd.")
```

 Explanation

 `for` Loop:
   The `for` loop iterates over each number in the `numbers` list.
   The variable `number` takes on the value of each item in the list one by one.

 `if-else` Statement:
   Inside the `for` loop, the `if-else` statement checks whether the current number is even or odd.
   If the number is even (i.e., `number % 2 == 0`), it prints "X is even."
   If the number is odd, it prints "X is odd."


6. Functions in Python:
   - What are functions in Python, and why are they useful? Write a Python function that takes two arguments and returns their sum. Include an example of how to call this function.

 Functions in Python

Functions are a fundamental building block in Python, used to group a set of statements so they can be executed more than once. Functions can also accept parameters and return values. They are useful for the following reasons:

1. Code Reusability: Functions allow you to write code once and reuse it multiple times without rewriting it.
2. Modularity: Functions enable you to break down complex problems into smaller, manageable pieces.
3. Maintainability: By isolating code into functions, it becomes easier to update and maintain.
4. Readability: Functions with meaningful names make the code more understandable and readable.

 Defining and Using Functions

 Defining a Function

To define a function in Python, you use the `def` keyword, followed by the function name and parentheses `()`. Inside the parentheses, you can define parameters that the function will accept.

 Example: Function to Sum Two Numbers


```python
def add_numbers(a, b):
    """
    This function takes two arguments and returns their sum.
    :param a: First number
    :param b: Second number
    :return: Sum of a and b
    """
    return a + b
```

 Explanation

 Function Definition:
   `def add_numbers(a, b):`: This line defines a function named `add_numbers` that takes two parameters, `a` and `b`.
   The colon `:` indicates the start of the function body.

 Docstring:
   The triple-quoted string `"""..."""` is a docstring, providing a description of the function. This is optional but recommended for documentation purposes.

 Return Statement:
   `return a + b`: This line returns the sum of `a` and `b`.

 Calling the Function

To use the function, you call it by its name and pass the required arguments. Here’s an example of how to call the `add_numbers` function:

```python
# Example of calling the add_numbers function
result = add_numbers(10, 5)
print("The sum is:", result)
```

 Explanation

 Calling the Function:
   `add_numbers(10, 5)`: This calls the `add_numbers` function with arguments `10` and `5`.
   The function returns the sum, which is `15`.

 Storing the Result:
   `result = add_numbers(10, 5)`: The returned value (`15`) is stored in the variable `result`.

 Printing the Result:
   `print("The sum is:", result)`: This prints the sum to the console.

 Complete Example


```python
def add_numbers(a, b):
    """
    This function takes two arguments and returns their sum.
    :param a: First number
    :param b: Second number
    :return: Sum of a and b
    """
    return a + b

# Example of calling the add_numbers function
result = add_numbers(10, 5)
print("The sum is:", result)
```

 Output

When you run the above code, the output will be:

```
The sum is: 15
```

7. Lists and Dictionaries:
   - Describe the differences between lists and dictionaries in Python. Write a script that creates a list of numbers and a dictionary with some key-value pairs, then demonstrates basic operations on both.

 Differences Between Lists and Dictionaries in Python

 Lists

 Ordered: Lists maintain the order of the elements as they were added.
 Indexed: Elements in a list can be accessed using their index, starting from 0.
 Mutable: Lists can be modified after creation (elements can be added, removed, or changed).
 Duplicates: Lists can contain duplicate elements.

Example: 
```python
my_list = [1, 2, 3, 4, 5]
```

Dictionaries

 Unordered: Dictionaries do not maintain the order of the elements (in versions before Python 3.7). From Python 3.7 onwards, insertion order is preserved as an implementation detail.
 Key-Value Pairs: Elements are stored as key-value pairs. Keys must be unique and immutable (e.g., strings, numbers, tuples), while values can be of any type.
 Mutable: Dictionaries can be modified after creation (key-value pairs can be added, removed, or changed).
 No Duplicates: Keys must be unique within a dictionary.

Example: 
```python
my_dict = {"name": "Alice", "age": 25, "city": "New York"}
```

 Script Demonstrating Lists and Dictionaries


```python
# Creating a list of numbers
numbers = [1, 2, 3, 4, 5]

# Basic operations on the list
print("Original list:", numbers)
numbers.append(6)  # Adding an element to the end of the list
print("After appending 6:", numbers)
numbers.remove(3)  # Removing an element from the list
print("After removing 3:", numbers)
print("Element at index 2:", numbers[2])  # Accessing an element by index
print("Length of the list:", len(numbers))  # Getting the length of the list

# Creating a dictionary with key-value pairs
person = {"name": "Alice", "age": 25, "city": "New York"}

# Basic operations on the dictionary
print("Original dictionary:", person)
person["email"] = "alice@example.com"  # Adding a new key-value pair
print("After adding email:", person)
person["age"] = 26  # Updating the value of an existing key
print("After updating age:", person)
del person["city"]  # Removing a key-value pair
print("After deleting city:", person)
print("Name:", person["name"])  # Accessing a value by key
print("Keys in the dictionary:", person.keys())  # Getting all keys
print("Values in the dictionary:", person.values())  # Getting all values
```

 Explanation of the Script

 List Operations

 Creating a List:
  ```python
  numbers = [1, 2, 3, 4, 5]
  ```

 Appending an Element:
  ```python
  numbers.append(6)
  ```
  Adds `6` to the end of the list.

 Removing an Element:
  ```python
  numbers.remove(3)
  ```
  Removes the first occurrence of `3` from the list.

 Accessing an Element by Index:
  ```python
  print("Element at index 2:", numbers[2])
  ```
  Prints the element at index `2`, which is `4`.

 Getting the Length of the List:
  ```python
  print("Length of the list:", len(numbers))
  ```
  Prints the number of elements in the list.

 Dictionary Operations

 Creating a Dictionary:
  ```python
  person = {"name": "Alice", "age": 25, "city": "New York"}
  ```

 Adding a New Key-Value Pair:
  ```python
  person["email"] = "alice@example.com"
  ```
  Adds a new key `email` with the value `"alice@example.com"`.

 Updating an Existing Key's Value:
  ```python
  person["age"] = 26
  ```
  Updates the value of the `age` key to `26`.

 Removing a Key-Value Pair:
  ```python
  del person["city"]
  ```
  Deletes the key-value pair where the key is `city`.

 Accessing a Value by Key:
  ```python
  print("Name:", person["name"])
  ```
  Prints the value associated with the key `name`, which is `"Alice"`.

 Getting All Keys:
  ```python
  print("Keys in the dictionary:", person.keys())
  ```
  Prints all the keys in the dictionary.

 Getting All Values:
  ```python
  print("Values in the dictionary:", person.values())
  ```
  Prints all the values in the dictionary.


8. Exception Handling:
   - What is exception handling in Python? Provide an example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script.

 Exception Handling in Python

Exception handling in Python is a mechanism to handle runtime errors in a graceful manner, allowing the program to continue execution or terminate cleanly. It involves using `try`, `except`, `else`, and `finally` blocks to catch and manage exceptions that might be raised during the execution of the code.

 Key Components of Exception Handling

1. `try` Block: Contains the code that might raise an exception.
2. `except` Block: Contains the code that runs if an exception occurs in the `try` block.
3. `else` Block: Contains the code that runs if no exception occurs in the `try` block (optional).
4. `finally` Block: Contains the code that runs no matter what, whether an exception occurs or not (optional).

 Example: Using `try`, `except`, and `finally` Blocks


```python
def divide_numbers(a, b):
    try:
        # Attempt to divide the two numbers
        result = a / b
    except ZeroDivisionError:
        # Handle the case where division by zero occurs
        print("Error: Division by zero is not allowed.")
        result = None
    except TypeError:
        # Handle the case where non-numeric types are used
        print("Error: Both arguments must be numbers.")
        result = None
    else:
        # This block executes if no exception occurs
        print("Division successful.")
    finally:
        # This block always executes
        print("Execution of the divide_numbers function is complete.")
    return result

# Test cases
print("Result of division:", divide_numbers(10, 2))
print("Result of division:", divide_numbers(10, 0))
print("Result of division:", divide_numbers(10, "a"))
```

 Explanation

1. `try` Block:
    `result = a / b`: This line attempts to divide `a` by `b`. If `b` is zero, a `ZeroDivisionError` will be raised. If either `a` or `b` is not a number, a `TypeError` will be raised.

2. `except` Blocks:
    `except ZeroDivisionError:`: This block catches the `ZeroDivisionError` if `b` is zero and prints an error message. It also sets `result` to `None`.
    `except TypeError:`: This block catches the `TypeError` if either `a` or `b` is not a number and prints an error message. It also sets `result` to `None`.

3. `else` Block:
    This block executes only if no exception occurs in the `try` block. It prints a success message.

4. `finally` Block:
    This block always executes, regardless of whether an exception was raised or not. It prints a completion message.

 Output


```
Division successful.
Execution of the divide_numbers function is complete.
Result of division: 5.0
Error: Division by zero is not allowed.
Execution of the divide_numbers function is complete.
Result of division: None
Error: Both arguments must be numbers.
Execution of the divide_numbers function is complete.
Result of division: None
```


9. Modules and Packages:
   - Explain the concepts of modules and packages in Python. How can you import and use a module in your script? Provide an example using the `math` module.

 Modules and Packages in Python

Modules

A module in Python is a file containing Python code. This code can define functions, classes, and variables, and can also include runnable code. Modules help in organizing code logically, making it easier to maintain and reuse.

 Packages

A package is a way of organizing related modules into a directory hierarchy. A package is essentially a directory that contains a special `__init__.py` file (which can be empty) and other module files. The `__init__.py` file indicates to Python that the directory should be treated as a package.

 Importing and Using a Module

To use a module in your script, you need to import it. You can import a module using the `import` statement.

 Importing the `math` Module

The `math` module provides access to mathematical functions and constants. Here's how you can import and use it:

```python
import math

# Using functions from the math module
number = 16
sqrt_result = math.sqrt(number)  # Calculate the square root
print(f"The square root of {number} is {sqrt_result}")

angle = math.pi / 4  # 45 degrees in radians
sin_result = math.sin(angle)  # Calculate the sine
print(f"The sine of 45 degrees is {sin_result}")

# Using constants from the math module
print(f"The value of pi is {math.pi}")
print(f"The value of e is {math.e}")
```

 Explanation

1. Importing the `math` Module:
   ```python
   import math
   ```
   This statement imports the `math` module, making its functions and constants available in the current namespace.

2. Using `math.sqrt()`:
   ```python
   sqrt_result = math.sqrt(number)
   ```
   The `sqrt()` function calculates the square root of a number.

3. Using `math.sin()`:
   ```python
   sin_result = math.sin(angle)
   ```
   The `sin()` function calculates the sine of an angle (in radians).

4. Using Constants:
   ```python
   print(f"The value of pi is {math.pi}")
   print(f"The value of e is {math.e}")
   ```
   The `math` module includes mathematical constants like `pi` and `e`.

 Using Aliases

You can also import a module with an alias to make it easier to use:

```python
import math as m

sqrt_result = m.sqrt(16)
print(f"The square root of 16 is {sqrt_result}")
```

 Importing Specific Functions

If you only need specific functions or constants from a module, you can import them directly:

```python
from math import sqrt, pi

sqrt_result = sqrt(16)
print(f"The square root of 16 is {sqrt_result}")
print(f"The value of pi is {pi}")
```

 Example Using a Custom Module

To demonstrate creating and using a custom module, consider the following example:

1. Create a Module File: Save the following code in a file named `mymodule.py`:

   ```python
   # mymodule.py
   def add(a, b):
       return a + b

   def subtract(a, b):
       return a - b
   ```

2. Import and Use the Custom Module:

   ```python
   # script.py
   import mymodule

   result_add = mymodule.add(10, 5)
   result_subtract = mymodule.subtract(10, 5)

   print(f"The result of addition is {result_add}")
   print(f"The result of subtraction is {result_subtract}")
   ```

 Explanation

 Creating `mymodule.py`:
  This file defines two functions: `add()` and `subtract()`.

 Importing and Using `mymodule`:
  The script `script.py` imports `mymodule` and calls its functions, demonstrating how to organize and reuse code.


10. File I/O:
    - How do you read from and write to files in Python? Write a script that reads the content of a file and prints it to the console, and another script that writes a list of strings to a file.

 File I/O in Python

File I/O (Input/Output) operations in Python allow you to work with files on your computer's filesystem. You can perform operations like reading from files, writing to files, appending to files, etc. Here's how you can read from and write to files in Python:

 Reading from a File

To read from a file in Python, you typically follow these steps:

1. Open the File: Use the `open()` function with the file path and mode (`'r'` for reading).
2. Read the Content: Use methods like `read()`, `readline()`, or `readlines()` to read the content.
3. Close the File: Always close the file using the `close()` method to free up system resources.

 Example: Reading from a File

```python
# Assuming a file named 'sample.txt' exists with some content
file_path = 'sample.txt'

try:
    # Open file in read mode
    with open(file_path, 'r') as file:
        # Read and print the entire content
        content = file.read()
        print("File Content:")
        print(content)
        
except FileNotFoundError:
    print(f"Error: The file '{file_path}' does not exist.")
except IOError:
    print(f"Error: Failed to read from the file '{file_path}'.")
```

 Writing to a File


1. Open the File: Use the `open()` function with the file path and mode (`'w'` for writing). If the file does not exist, Python will create it.
2. Write Content: Use methods like `write()` to write content to the file.
3. Close the File: Always close the file using the `close()` method to save the changes and free up system resources.

 Example: Writing to a File

```python
# List of strings to write to a file
lines_to_write = [
    "This is line 1.",
    "This is line 2.",
    "This is line 3."
]

file_path = 'output.txt'

try:
    # Open file in write mode
    with open(file_path, 'w') as file:
        # Write each line to the file
        for line in lines_to_write:
            file.write(line + "\n")
    
    print(f"Successfully wrote {len(lines_to_write)} lines to '{file_path}'.")

except IOError:
    print(f"Error: Failed to write to the file '{file_path}'.")
```

 Explanation

 Reading from a File:
   `with open(file_path, 'r') as file:`: Opens the file `'sample.txt'` in read mode (`'r'`).
   `content = file.read()`: Reads the entire content of the file into the `content` variable.
   `print(content)`: Prints the content to the console.

 Writing to a File:
   `with open(file_path, 'w') as file:`: Opens the file `'output.txt'` in write mode (`'w'`).
   `for line in lines_to_write:`: Iterates through each line in `lines_to_write`.
   `file.write(line + "\n")`: Writes each line followed by a newline character (`"\n"`).

 Closing Files Safely:
   Using `with open(...) as file:` ensures that the file is properly closed even if an exception occurs.

 File Content Examples

```
Hello, this is a sample file.
It contains multiple lines of text.
Python file I/O operations can read and write to files.
```

Output of Reading Script:
```
File Content:
Hello, this is a sample file.
It contains multiple lines of text.
Python file I/O operations can read and write to files.
```

Output of Writing Script:
Creates a file named `output.txt` with the following content:
```
This is line 1.
This is line 2.
This is line 3.
```
References

1. Python Documentation:
    Official Python documentation on [Modules](https://docs.python.org/3/tutorial/modules.html) and [Packages](https://docs.python.org/3/tutorial/modules.html#packages)
   - Python documentation on [Built-in Exceptions](https://docs.python.org/3/library/exceptions.html)

2. Real Python Tutorials:
    [Python Exception Handling Techniques](https://realpython.com/python-exceptions/)
    [Python Modules and Packages](https://realpython.com/python-modules-packages/)

3. GeeksforGeeks:
    [File handling in Python](https://www.geeksforgeeks.org/file-handling-python/)
    [Python | Modules in Python](https://www.geeksforgeeks.org/modules-python/)

4. W3Schools:
    [Python Files I/O](https://www.w3schools.com/python/python_file_handling.asp)
    [Python Modules](https://www.w3schools.com/python/python_modules.asp)



# Submission Guidelines:
- Your answers should be well-structured, concise, and to the point.
- Provide code snippets or complete scripts where applicable.
- Cite any references or sources you use in your answers.
- Submit your completed assignment by [due date].


