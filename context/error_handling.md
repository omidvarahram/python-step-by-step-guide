← [back to index page](../index.md)

# **1.6 Basic Error Handling**

Error handling is a crucial part of programming. Python provides robust mechanisms to catch and handle errors, ensuring your programs can gracefully recover from unexpected situations. Without error handling, unhandled exceptions can crash your program.

---

## **1.6.1 Understanding `try`, `except`, and `finally` Blocks**

Python's `try` block lets you test a block of code for exceptions. If an exception occurs, it is caught by the `except` block. The `finally` block is used for cleanup actions, regardless of whether an exception occurred or not.

### **Basic Structure**
```python
try:
    # Code that might raise an exception
    risky_operation = 10 / 0
except ZeroDivisionError:
    # Handle the exception
    print("You can't divide by zero!")
finally:
    # Code that will always execute
    print("Execution completed.")
```
---

### **Multiple `except` Blocks**
You can handle different types of exceptions using multiple `except` blocks.

```python
try:
    number = int(input("Enter a number: "))
    result = 10 / number
except ValueError:
    print("That's not a valid number!")
except ZeroDivisionError:
    print("You can't divide by zero!")
finally:
    print("End of program.")
```
---

## **1.6.2 Raising Exceptions**

You can use the `raise` keyword to manually trigger an exception.

### **Raising a Specific Exception**
```python
def validate_age(age):
    if age < 0:
        raise ValueError("Age cannot be negative.")
    print(f"Your age is {age}.")

try:
    validate_age(-5)
except ValueError as e:
    print(f"Error: {e}")
```
---

### **Custom Exceptions**
You can define your own exceptions by inheriting from the `Exception` class.

```python
class CustomError(Exception):
    pass

try:
    raise CustomError("This is a custom error.")
except CustomError as e:
    print(f"Caught a custom error: {e}")
```
---

## **1.6.3 Common Python Exceptions**

Here are some of the most common exceptions you may encounter:

| Exception             | Description                                  |
|-----------------------|----------------------------------------------|
| `ValueError`          | Raised when a value is inappropriate.       |
| `TypeError`           | Raised when an operation is performed on incompatible types. |
| `IndexError`          | Raised when trying to access an invalid list index. |
| `KeyError`            | Raised when trying to access a non-existent dictionary key. |
| `ZeroDivisionError`   | Raised when dividing by zero.               |
| `FileNotFoundError`   | Raised when a file operation fails due to the file not existing. |

### **Example of Multiple Common Exceptions**
```python
try:
    numbers = [1, 2, 3]
    print(numbers[5])  # Will raise an IndexError
except IndexError:
    print("Index out of range.")
except Exception as e:
    print(f"An unexpected error occurred: {e}")
```
---

## **Best Practices for Error Handling**

1. **Use Specific Exceptions**: Catch specific exceptions rather than using a generic `except Exception`.
2. **Keep `try` Blocks Small**: Only include code that might raise an exception.
3. **Avoid Silent Failures**: Always log or inform the user when an exception occurs.
4. **Clean Up with `finally`**: Use `finally` to release resources (e.g., close files, release database connections).

---

# **Tasks for Chapter 1.6**

## **Task 1: Divide Safely**
Write a program that accepts two numbers and divides them. Handle the following exceptions:
- Division by zero
- Invalid input (non-numeric)

### **Solution:**
```python
try:
    num1 = float(input("Enter the numerator: "))
    num2 = float(input("Enter the denominator: "))
    result = num1 / num2
    print(f"Result: {result}")
except ZeroDivisionError:
    print("You can't divide by zero!")
except ValueError:
    print("Please enter valid numbers.")
```
---

## **Task 2: File Operations with Error Handling**
Write a program that tries to read a file. If the file doesn't exist, catch the exception and create the file.

### **Solution:**
```python
import os

try:
    with open("data.txt", "r") as file:
        print(file.read())
except FileNotFoundError:
    print("File not found. Creating a new file...")
    with open("data.txt", "w") as file:
        file.write("This is a new file.")
```
---

## **Task 3: Custom Age Validation**
Write a program that validates an age input. Raise an exception if the age is negative or over 120.

### **Solution:**
```python
def validate_age(age):
    if age < 0 or age > 120:
        raise ValueError("Invalid age. Age must be between 0 and 120.")
    print(f"Valid age: {age}")

try:
    user_age = int(input("Enter your age: "))
    validate_age(user_age)
except ValueError as e:
    print(f"Error: {e}")
```
---



← [back to index page](../index.md)