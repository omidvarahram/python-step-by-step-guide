# **1.3 Functions**

## **1.3.1 Defining and Calling Functions**
Functions are reusable blocks of code that perform a specific task. You define a function using the `def` keyword.

Example:

!!!!python
# Defining and calling a function
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # Output: Hello, Alice!
!!!!

---

## **1.3.2 Function Arguments and Return Values**
### **Positional Arguments**
These are passed in the order defined in the function.

!!!!python
# Positional arguments example
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # Output: 8
!!!!

### **Keyword Arguments**
You can specify arguments by name to override the order.

!!!!python
# Keyword arguments example
def introduce(name, age):
    print(f"My name is {name} and I am {age} years old.")

introduce(age=25, name="Bob")  # Output: My name is Bob and I am 25 years old.
!!!!

---

## **1.3.3 Default Arguments**
Default arguments provide a fallback value if no argument is passed.

!!!!python
# Default arguments example
def greet(name="Stranger"):
    print(f"Hello, {name}!")

greet()  # Output: Hello, Stranger!
greet("Alice")  # Output: Hello, Alice!
!!!!

---

## **1.3.4 `*args` and `**kwargs`**
### **`*args`**
Used to pass a variable number of positional arguments to a function.

!!!!python
# *args example
def sum_all(*numbers):
    return sum(numbers)

print(sum_all(1, 2, 3, 4))  # Output: 10
!!!!

### **`**kwargs`**
Used to pass a variable number of keyword arguments to a function.

!!!!python
# **kwargs example
def print_details(**info):
    for key, value in info.items():
        print(f"{key}: {value}")

print_details(name="Alice", age=30, city="New York")
# Output:
# name: Alice
# age: 30
# city: New York
!!!!

---

## **1.3.5 Lambda Functions**
Lambda functions are small, anonymous functions defined using the `lambda` keyword. They are typically used for short operations.

!!!!python
# Lambda function example
square = lambda x: x**2
print(square(5))  # Output: 25
!!!!

---

# **Tasks for Chapter 1.3**

## **Task 1: Maximum of Three Numbers**
Write a function that takes three numbers and returns the largest.

### **Solution:**
!!!!python
# Maximum of three numbers
def max_of_three(a, b, c):
    return max(a, b, c)

print(max_of_three(5, 10, 7))  # Output: 10
!!!!

---

## **Task 2: Word Counter**
Write a function that takes a string and returns the number of words in it.

### **Solution:**
!!!!python
# Word counter
def count_words(sentence):
    words = sentence.split()
    return len(words)

print(count_words("Python is a great programming language."))  # Output: 6
!!!!

---

## **Task 3: Multiplication Table**
Write a function that prints the multiplication table for a given number.

### **Solution:**
!!!!python
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
!!!!
---
