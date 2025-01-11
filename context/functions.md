← [back to index page](../index.md)
# **1.3 Functions**

Functions are reusable blocks of code that allow you to encapsulate logic, making programs more modular and maintainable. Python offers a range of tools to create and use functions effectively.

---

## **1.3.1 Defining and Calling Functions**

A function is defined using the `def` keyword, followed by the function name and parentheses. Inside the parentheses, you can define parameters that the function can accept.

### **Defining a Function**
```python
# Example: Defining and calling a function
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # Output: Hello, Alice!
```

### **Function Naming Rules**
1. Function names must start with a letter or underscore (_).
2. Function names can only contain alphanumeric characters and underscores.
3. Function names should follow the snake_case convention (e.g., `calculate_sum`).

---

## **1.3.2 Function Arguments and Return Values**

Python functions can take arguments and return values, making them versatile.

### **Positional Arguments**
Arguments are passed in the same order they are defined.

```python
# Example: Positional arguments
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # Output: 8
```

### **Keyword Arguments**
Keyword arguments specify values explicitly by their parameter name.

```python
# Example: Keyword arguments
def introduce(name, age):
    print(f"My name is {name} and I am {age} years old.")

introduce(age=25, name="Bob")  # Output: My name is Bob and I am 25 years old.
```

### **Return Values**
Functions can return values using the `return` keyword.

```python
# Example: Returning a value
def multiply(a, b):
    return a * b

product = multiply(4, 5)
print(product)  # Output: 20
```

---

## **1.3.3 Default Arguments**

Default arguments allow you to specify default values for parameters.

```python
# Example: Default arguments
def greet(name="Stranger"):
    print(f"Hello, {name}!")

greet()  # Output: Hello, Stranger!
greet("Alice")  # Output: Hello, Alice!
```

---

## **1.3.4 `*args` and `**kwargs`

### **`*args`**
`*args` allows a function to accept any number of positional arguments.

```python
# Example: *args
def sum_all(*numbers):
    return sum(numbers)

print(sum_all(1, 2, 3, 4))  # Output: 10
```

### **`**kwargs`**
`**kwargs` allows a function to accept any number of keyword arguments.

```python
# Example: **kwargs
def print_details(**info):
    for key, value in info.items():
        print(f"{key}: {value}")

print_details(name="Alice", age=30, city="New York")
# Output:
# name: Alice
# age: 30
# city: New York
```

---

## **1.3.5 Lambda Functions**

Lambda functions are small, anonymous functions defined using the `lambda` keyword. They are often used for short, simple operations.

```python
# Example: Lambda function
square = lambda x: x**2
print(square(5))  # Output: 25
```

#### **Use Cases**
- Quick calculations
- Use as arguments in higher-order functions like `map`, `filter`, or `sorted`.

```python
# Example: Lambda with sorted
students = [("Alice", 85), ("Bob", 75), ("Charlie", 90)]
students_sorted = sorted(students, key=lambda student: student[1])
print(students_sorted)
# Output: [('Bob', 75), ('Alice', 85), ('Charlie', 90)]
```

---

# **Tasks for Chapter 1.3**

## **Task 1: Maximum of Three Numbers**
Write a function that takes three numbers and returns the largest.

### **Solution:**
```python
# Maximum of three numbers
def max_of_three(a, b, c):
    return max(a, b, c)

print(max_of_three(5, 10, 7))  # Output: 10
```

---

## **Task 2: Word Counter**
Write a function that takes a string and returns the number of words in it.

### **Solution:**
```python
# Word counter
def count_words(sentence):
    words = sentence.split()
    return len(words)

print(count_words("Python is a great programming language."))  # Output: 6
```

---

## **Task 3: Multiplication Table**
Write a function that prints the multiplication table for a given number.

### **Solution:**
```python
# Multiplication table
def multiplication_table(number):
    for i in range(1, 11):
        print(f"{number} x {i} = {number * i}")

multiplication_table(5)
# Output:
# 5 x 1 = 5
# 5 x 2 = 10
# ...
# 5 x 10 = 50
```
---

## **Task 4: Sum of Arbitrary Numbers**
Write a function that accepts any number of numbers and returns their sum.

### **Solution:**
```python
# Sum of arbitrary numbers
def sum_numbers(*numbers):
    return sum(numbers)

print(sum_numbers(10, 20, 30, 40))  # Output: 100
```
---

← [back to index page](../index.md)
