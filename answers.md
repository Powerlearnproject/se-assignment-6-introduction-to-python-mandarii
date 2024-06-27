## QUESTION 1

What is Python, and what are some of its key features that make it popular among developers? Provide examples of use cases where Python is particularly effective.
**Answer**
Python is an object-oriented, high-level programming language with dynamic semantics.
Python is popular because:
* It is easy to use
* It works on different platforms
* Its syntax allows developers to write code with fewer lines
* The code in python can be executed as soon as it is written
Examples of cases where python is effective:
* web development (server-side)
* software development
* mathematics
* system scripting.


## QUESTION 2

Describe the steps to install Python on your operating system (Windows, macOS, or Linux). Include how to verify the installation and set up a virtual environment.
**Answer**
Go to python.org
Download the setup that fits your operating system
Access the setup from your computer after downloading
Double click the installer and on the first dialogue box click install now
Chect the box for adding python path and click on customize installation if you want to customize any features
Finish the process
To verify whether the install was successful, open command prompt as administrator and use the command (python --version)
To install required packages use PIP ( for installing packages)
To set up a virtual environment ( python pip install virtualenv)



## QUESTION 3

 Write a simple Python program that prints "Hello, World!" to the console. Explain the basic syntax elements used in the program.
 **Answer**
 Print("Hello, World!")
The syntax print is a built in function that outputs text to the console.
The "()" are used to enclose the arguments of the function
"Hello, World!" is a string literal.
The double quotes are used to define the beginning and end of the string literal.

 ## QUESTION 4

 List and describe the basic data types in Python. Write a short script that demonstrates how to create and use variables of different data types.
 **Answer**
* Integer (int): Represents whole numbers (e.g. 5,9).
* Floating-Point (float): Represents decimal numbers (e.g., 5.67).
* Complex (complex): Represents complex numbers with a real and imaginary part (e.g., 5 + 7k).
* String (str): Represents data with text (e.g., “Hello, World!”).
* Boolean (bool): Represents either True or False.
* List (list): An ordered collection of items (e.g., [1, 2, 3]).
* Tuple (tuple): Similar to a list but immutable (e.g., (1, 2, 3)).
* Range (range): Represents a sequence of numbers (e.g., range(4) gives [0, 1, 2, 3]).
* Dictionary (dict): Stores key-value pairs (e.g., {"name": "Bree", "age": 25}).
* Set (set): An unordered collection of unique elements (e.g., {1, 2, 3}).
* None (NoneType): Represents absence of a value.
## Script 

* Integer
my_integer = 25
* Floating-point
my_float = 5.67
* Complex
my_complex = 5 + 7k
* String
my_string = "Hello, World!"
* Boolean
my_boolean = True
* List
my_list = [1, 2, 3]
* Tuple
my_tuple = (4, 5, 6)
* Range
my_range = range(5)
* Dictionary
my_dict = {"name": "Bree", "age": 25}
* Set
my_set = {1, 2, 3}
* None
my_none = None

 ## QUESTION 5

 Explain the use of conditional statements and loops in Python. Provide examples of an `if-else` statement and a `for` loop.
 **Answer**
Conditional statements allow you to make decisions in your code based on certain conditions.
## Code
number = 20

if number > 0:
    print("The number is positive.")
elif number == 0:
    print("The number is zero.")
else:
    print("The number is negative.")

Loops allow you to repeat a block of code multiple times.
## Code
numbers = [1, 2, 3, 4, 5]

for number in numbers:
    print(f"The current number is {number}")
    
## QUESTION 6

What are functions in Python, and why are they useful? Write a Python function that takes two arguments and returns their sum. Include an example of how to call this function.
**Answer**
Python functions are reusable code blocks that carry out particular tasks, helping programmers structure their code and make it easier to read.

# Code
def add_numbers(a, b):
    return a + b

# Example usage:
result = add_numbers(40, 30)
print("Sum:", result)

## QUESTION 7

Describe the differences between lists and dictionaries in Python. Write a script that creates a list of numbers and a dictionary with some key-value pairs, then demonstrates basic operations on both.

**Answer**
Lists are generally linear while dictionaries store data in key value pair.
# Script
# Create a list of numbers
numbers = [1, 2, 3, 4, 5]
# Basic operations in list
print("Original list:", numbers)

# Create a dictinary
person = {
    'name': 'Bree',
    'age': 25,
    'city': 'Nairobi'
}
# Basic operations on dictionary
print("\nOriginal dictionary:", person)


## QUESTION 8

 What is exception handling in Python? Provide an example of how to use `try`, `except`, and `finally` blocks to handle errors in a Python script.
**Answer**
Exception handling allows you to manage and respond to runtime errors, preventing your program from crashing unexpectedly.
# Example
def divide(a, b):
    try:
        result = a / b
    except ZeroDivisionError:
        print("Error: Division by zero is not allowed.")
        result = None
    except TypeError:
        print("Error: Unsupported operand type(s). Both arguments must be numbers.")
        result = None
    else:
        print("Division successful.")
    finally:
        print("Execution of the 'divide' function complete.")
    return result

## QUESTION 9

Explain the concepts of modules and packages in Python. How can you import and use a module in your script? Provide an example using the `math` module.
**Answer**
A module can define functions, classes, and variables. It can also include runnable code.
Packages allow you to organize related modules together, creating a hierarchical structure.

You can import a module using the import statement.
# Example using math module
Import math
From math import sqrt, pi
# Code
number = 16
square_root = math.sqrt(number)
print(f"The square root of {number} is {square_root}")


## QUESTION 10

How do you read from and write to files in Python? Write a script that reads the content of a file and prints it to the console, and another script that writes a list of strings to a file.
**Answer**
The open() function is used to open a file, and different modes ('r' for reading, 'w' for writing, etc.) determine how the file is handled.
# Code 

# Script to read the content of a file and print it to the console

def read_file(file_path):
    try:
        with open(file_path, 'r') as file:
            content = file.read()
            print(content)
    except FileNotFoundError:
        print(f"The file {file_path} does not exist.")
    except IOError:
        print(f"An error occurred while reading the file {file_path}.")

# Specify the path to the file you want to read
file_path = 'example.txt'

# Call the function to read and print the file content
read_file(file_path)

# Script to write a list of strings to a file

def write_to_file(file_path, lines):
    try:
        with open(file_path, 'w') as file:
            for line in lines:
                file.write(line + '\n')
        print(f"Successfully wrote to the file {file_path}.")
    except IOError:
        print(f"An error occurred while writing to the file {file_path}.")

# Specify the path to the file you want to write to
file_path = 'output.txt'

# List of strings to write to the file
lines = [
    "First line of text.",
    "Second line of text.",
    "Third line of text."
]

# Call the function to write the list of strings to the file
write_to_file(file_path, lines)

## REFERENCES
* Class notes
* https://www.w3schools.com/python
* https://www.geeksforgeeks.org
* ChatGPT