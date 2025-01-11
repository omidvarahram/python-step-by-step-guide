← [back to index page](../index.md)
# **1.2 Control Flow**

Control flow statements determine the order in which code is executed. Python provides multiple tools for control flow, including conditionals, loops, and specialized loop controls.

---

## **1.2.1 Conditional Statements**

Conditional statements allow Python programs to execute specific blocks of code based on a condition. The primary structures are `if`, `elif`, and `else`.

### **Basic Conditional Statement**
```python
# Example: Simple if statement
age = int(input("Enter your age: "))
if age >= 18:
    print("You are an adult.")
```
If the condition evaluates to `True`, the indented block under the `if` statement is executed.

### **Using `elif` and `else`**
You can include multiple conditions with `elif` and a default action with `else`.

```python
# Example: if-elif-else structure
grade = int(input("Enter your grade: "))
if grade >= 90:
    print("Excellent!")
elif grade >= 75:
    print("Good job!")
elif grade >= 50:
    print("You passed.")
else:
    print("Better luck next time.")
```

---

## **1.2.2 Loops**

### **For Loops**
`for` loops are used to iterate over sequences like lists, tuples, strings, or ranges.

#### **Iterating Through a List**
```python
# Example: Iterating through a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(f"I like {fruit}.")
```

#### **Using `range()`**
`range()` generates a sequence of numbers.

```python
# Example: Using range()
for i in range(5):
    print(f"Number: {i}")
```
`range(start, stop, step)` can also take additional parameters for more control.

#### **Enumerate**
Use `enumerate()` to get both the index and value of items in a sequence.

```python
# Example: Using enumerate
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")
```

---

### **While Loops**
`while` loops repeat a block of code as long as a condition is `True`.

```python
# Example: Simple while loop
count = 0
while count < 5:
    print(f"Count: {count}")
    count += 1
```

Use `while` for situations where the number of iterations is not predetermined.

---

## **1.2.3 Loop Control Statements**

### **Break Statement**
`break` exits the loop immediately, regardless of the condition.

```python
# Example: Using break
for num in range(10):
    if num == 5:
        break
    print(num)
```

---

### **Continue Statement**
`continue` skips the current iteration and moves to the next one.

```python
# Example: Using continue
for num in range(5):
    if num == 2:
        continue
    print(num)
```

---

### **Pass Statement**
`pass` is a placeholder that does nothing. Use it in situations where code will be added later.

```python
# Example: Using pass
for num in range(3):
    if num == 1:
        pass  # Placeholder for future logic
    else:
        print(num)
```

---

## **1.2.4 List Comprehensions and Generator Expressions**

### **List Comprehensions**
List comprehensions offer a concise way to create lists.

```python
# Example: List comprehension
squares = [x**2 for x in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```

### **Generator Expressions**
Generator expressions create iterators that generate items on demand, saving memory.

```python
# Example: Generator expression
squares_gen = (x**2 for x in range(5))
for square in squares_gen:
    print(square)
```
Generators are especially useful for large datasets.

---

# **Tasks for Chapter 1.2**

## **Task 1: FizzBuzz**
Write a program that prints numbers from 1 to 50. For multiples of 3, print "Fizz"; for multiples of 5, print "Buzz"; and for multiples of both 3 and 5, print "FizzBuzz."

### **Solution:**
```python
# FizzBuzz solution
for num in range(1, 51):
    if num % 3 == 0 and num % 5 == 0:
        print("FizzBuzz")
    elif num % 3 == 0:
        print("Fizz")
    elif num % 5 == 0:
        print("Buzz")
    else:
        print(num)
```
---

## **Task 2: Factorial Calculator**
Write a program that calculates the factorial of a number using a `while` loop.

### **Solution:**
```python
# Factorial calculator
number = int(input("Enter a number: "))
factorial = 1
while number > 0:
    factorial *= number
    number -= 1
print(f"The factorial is {factorial}.")
```
---

## **Task 3: Create a List of Even Numbers**
Use a list comprehension to create a list of even numbers between 1 and 100.

### **Solution:**
```python
# Even numbers list comprehension
even_numbers = [x for x in range(1, 101) if x % 2 == 0]
print(even_numbers)
```
---

← [back to index page](../index.md)