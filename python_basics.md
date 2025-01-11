# **1.1 Python Basics**

## **1.1.1 Installing Python and Setting Up the Development Environment**
Python can be installed from [python.org](https://www.python.org/). Here’s how to set up Python and your development environment:
1. Download the latest stable version for your OS.
2. Install Python, ensuring you check the option to add Python to your PATH during installation.
3. Verify installation by typing `python --version` or `python3 --version` in your terminal.

For development, consider using:
- **PyCharm**: Full-featured IDE with debugging and tools for large projects.
- **VSCode**: Lightweight and extensible with Python support via extensions.
- **Jupyter Notebook**: Great for interactive coding, data analysis, and visualization.

---

## **1.1.2 Understanding Python Syntax and Indentation**
Python uses indentation to define code blocks, such as functions, loops, and conditionals. For example:

```python
if True:
    print("Python uses indentation!")
    print("This is part of the same block.")
print("This is outside the block.")
```

Python’s simplicity lies in its readability, with no need for `{}` or `;` to structure code.

---

## **1.1.3 Variables and Data Types**
Variables are dynamically typed in Python. Examples:

```python
# Strings
name = "Python"
# Integers
year = 2023
# Floats
pi = 3.14
# Booleans
is_python_fun = True
```

---

## **1.1.4 Input and Output Operations**
To interact with users:

```python
# Input
name = input("What is your name? ")
# Output
print(f"Hello, {name}!")
```

---

## **1.1.5 Basic Operators**
Python supports arithmetic, comparison, logical, and bitwise operators:

```python
# Arithmetic
x = 10 + 5
# Comparison
is_greater = 10 > 5
# Logical
logical_and = True and False
```

---

# **Tasks for Chapter 1**

## **Task 1: Basic Calculator**
Write a program to take two numbers as input and perform addition, subtraction, multiplication, and division.

### **Solution:**
```python
# Basic Calculator
num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))
print(f"Addition: {num1 + num2}")
print(f"Subtraction: {num1 - num2}")
print(f"Multiplication: {num1 * num2}")
print(f"Division: {num1 / num2}")
```

---

## **Task 2: Odd or Even Checker**
Write a program to check if a number is odd or even.

### **Solution:**
```python
# Odd or Even Checker
num = int(input("Enter a number: "))
if num % 2 == 0:
    print(f"{num} is Even.")
else:
    print(f"{num} is Odd.")
```
---
