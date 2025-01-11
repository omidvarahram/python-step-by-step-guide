← [back to index page](../index.md)
# **1.1 Python Basics**

## **1.1.1 Installing Python and Setting Up the Development Environment**

Python is a versatile programming language available on all major operating systems. Here's a detailed guide to installing and setting up Python on different platforms:

### **Installing Python on Windows**
1. Visit the official [Python website](https://www.python.org/).
2. Download the latest stable release for Windows.
3. Run the installer:
   - Check the box for **Add Python to PATH**.
   - Choose "Customize installation" if you want to specify additional options (recommended).
4. Verify the installation by opening the command prompt and typing:
   ```bash
   python --version
   ```
   or
   ```bash
   python3 --version
   ```

### **Installing Python on macOS**
1. macOS often comes with a pre-installed version of Python, but it's usually outdated. Install the latest version using [Homebrew](https://brew.sh/):
   ```bash
   brew install python
   ```
2. Alternatively, download the installer from the [Python website](https://www.python.org/).
3. Verify the installation:
   ```bash
   python3 --version
   ```

### **Installing Python on Linux**
1. Most Linux distributions come with Python pre-installed. To check:
   ```bash
   python3 --version
   ```
2. If it's not installed or outdated, use the package manager for your distribution:
   - **Ubuntu/Debian**:
     ```bash
     sudo apt update
     sudo apt install python3
     ```
   - **Fedora**:
     ```bash
     sudo dnf install python3
     ```
   - **Arch**:
     ```bash
     sudo pacman -S python
     ```

### **Setting Up Development Environments**
Once Python is installed, choose an Integrated Development Environment (IDE) or code editor for writing Python code:
1. **PyCharm**: A full-featured IDE suitable for complex projects. Free Community Edition available.
2. **VSCode**: Lightweight, with excellent Python support via extensions.
3. **Jupyter Notebook**: Ideal for data analysis and visualization. Install with:
   ```bash
   pip install notebook
   ```
4. **IDLE**: Comes bundled with Python. Basic but sufficient for small scripts.

---

## **1.1.2 Understanding Python Syntax and Indentation**

Python enforces indentation to define code blocks. This makes code visually clean and reduces the chance of errors.

### **Indentation Example**
```python
# Correct indentation
if True:
    print("This block is indented properly.")
    print("Python requires indentation to define blocks.")

# Incorrect indentation (will throw an IndentationError)
if True:
print("This will cause an error.")
```

### **Key Rules**
1. Use 4 spaces per indentation level (PEP 8 style guide).
2. Mixing tabs and spaces is discouraged and will cause errors.

---

## **1.1.3 Variables and Data Types**

Python variables do not require explicit type declarations. Their type is inferred based on the value assigned.

### **Primitive Data Types**
1. **Integers**: Whole numbers.
   ```python
   x = 10
   ```
2. **Floats**: Decimal numbers.
   ```python
   y = 3.14
   ```
3. **Strings**: Text enclosed in quotes.
   ```python
   name = "Python"
   ```
4. **Booleans**: True or False.
   ```python
   is_fun = True
   ```

### **Advanced Data Types**
1. **Lists**: Ordered, mutable collections.
   ```python
   fruits = ["apple", "banana", "cherry"]
   ```
2. **Tuples**: Ordered, immutable collections.
   ```python
   coordinates = (10, 20)
   ```
3. **Dictionaries**: Key-value pairs.
   ```python
   person = {"name": "Alice", "age": 30}
   ```
4. **Sets**: Unordered collections of unique items.
   ```python
   unique_numbers = {1, 2, 3, 3}
   ```

### **Generics**
Python supports generic types through `typing` (e.g., `List[int]` for lists containing integers). These help with static type checking in large projects.

---

## **1.1.4 Input and Output Operations**

### **Input Example**
```python
# Input from the user
name = input("Enter your name: ")
print(f"Hello, {name}!")
```

### **Output Example**
```python
# Using print for output
x = 5
y = 10
print(f"The sum of {x} and {y} is {x + y}.")
```

---

## **1.1.5 Basic Operators**

### **Arithmetic Operators**
```python
# Addition, subtraction, multiplication, division
a = 10
b = 5
print(a + b)  # 15
print(a - b)  # 5
print(a * b)  # 50
print(a / b)  # 2.0
```

### **Comparison Operators**
```python
# Greater than, less than, equality
print(a > b)  # True
print(a == b)  # False
```

### **Logical Operators**
```python
# and, or, not
print(a > 5 and b < 10)  # True
print(not a > 5)  # False
```

---

# **Tasks for Chapter 1.1**

## **Task 1: Python Installation**
Install Python on your operating system and set up a development environment. Verify the installation by running:
```bash
python3 --version
```

## **Task 2: Basic Calculator**
Write a program to take two numbers and perform addition, subtraction, multiplication, and division.

```python
# Basic Calculator Solution
num1 = float(input("Enter the first number: "))
num2 = float(input("Enter the second number: "))
print(f"Addition: {num1 + num2}")
print(f"Subtraction: {num1 - num2}")
print(f"Multiplication: {num1 * num2}")
print(f"Division: {num1 / num2}")
```
---

← [back to index page](../index.md)