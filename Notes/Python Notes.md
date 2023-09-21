### Python Notes - 9.12

Python is a popular, high-level programming language known for its simplicity and readability. It's a great choice for beginners. Let's start with the basics:

### 1. Installation:
Before you can start writing Python code, you need to install Python on your computer. Visit the official Python website (https://www.python.org/downloads/) to download the latest version of Python for your operating system. Follow the installation instructions.

### 2. Python Interpreter:
Python comes with an interactive interpreter that allows you to run Python code line by line. You can access it by opening your terminal or command prompt and typing python or python3 (depending on your installation). This will open the Python shell, where you can type Python code directly and see the results.

### 3. Writing Your First Python Program:
Let's start with a simple "Hello, World!" program. Open a text editor (like Notepad, Visual Studio Code, or PyCharm) and create a new file with the .py extension (e.g., hello.py).

# hello.py

print("Hello, World!")

Save the file and open your terminal or command prompt. Navigate to the directory where you saved hello.py, and then run the program using the python command:

python hello.py

You should see the output: "Hello, World!"

### 4. Basic Python Concepts:
Now, let's cover some fundamental concepts:

## Variables and Data Types:
Python supports various data types, including integers, floats, strings, lists, and more. You can create variables to store data.

# Variables

name = "John"
age = 30
height = 5.9
is_student = True

# Data Types

print(type(name))        # <class 'str'>
print(type(age))         # <class 'int'>
print(type(height))      # <class 'float'>
print(type(is_student))  # <class 'bool'>

## Control Structures:
Python uses indentation to define blocks of code. Common control structures include if statements and loops (for and while).

# If statement

x = 10
if x > 5:
    print("x is greater than 5")

# For loop

for i in range(5):
    print(i)

# While loop

count = 0
while count < 3:
    print(count)
    count += 1
    
## Functions:

Functions allow you to encapsulate reusable code. You can define your functions using the def keyword.

def greet(name):
    return f"Hello, {name}!"

message = greet("Alice")
print(message)  # Output: Hello, Alice!

These are the very basics of Python programming. As you progress, you can explore more advanced topics like object-oriented programming, file handling, libraries, and frameworks specific to your interests (e.g., web development, data analysis, machine learning).
