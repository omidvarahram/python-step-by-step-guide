# **1.2 Control Flow**

## **1.2.1 Conditional Statements**
Conditional statements allow your program to make decisions based on certain conditions. Python uses `if`, `elif`, and `else` to handle conditional logic.

Example:

```python
# Conditional statement example
age = int(input("Enter your age: "))
if age < 18:
    print("You are a minor.")
elif age < 65:
    print("You are an adult.")
else:
    print("You are a senior.")
```

---

## **1.2.2 Loops**
### **For Loops**
A `for` loop is used to iterate over a sequence (like a list, tuple, or string).

Example:

```python
# For loop example
for fruit in ["apple", "banana", "cherry"]:
    print(f"I like {fruit}.")
```

### **While Loops**
A `while` loop repeats as long as a condition is true.

Example:

```python
# While loop example
count = 0
while count < 5:
    print(f"Count is {count}.")
    count += 1
```

---

## **1.2.3 Loop Control Statements**
### **Break Statement**
The `break` statement exits a loop immediately.

```python
# Break statement example
for num in range(10):
    if num == 5:
        break
    print(num)
```

### **Continue Statement**
The `continue` statement skips the rest of the code inside the loop for the current iteration.

```python
# Continue statement example
for num in range(5):
    if num == 3:
        continue
    print(num)
```

### **Pass Statement**
The `pass` statement does nothing. It is a placeholder for future code.

```python
# Pass statement example
for num in range(5):
    if num == 3:
        pass  # Placeholder for future code
    else:
        print(num)
```

---

## **1.2.4 List Comprehensions and Generator Expressions**
### **List Comprehensions**
List comprehensions provide a concise way to create lists.

Example:

```python
# List comprehension example
squares = [x**2 for x in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```

### **Generator Expressions**
Generator expressions create iterators that produce items on demand.

```python
# Generator expression example
squares_gen = (x**2 for x in range(5))
for square in squares_gen:
    print(square)
```
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

## **Task 2: Sum of Even Numbers**
Write a program to calculate the sum of all even numbers between 1 and 100.

### **Solution:**
```python
# Sum of even numbers
total = sum(num for num in range(1, 101) if num % 2 == 0)
print(f"The sum of all even numbers between 1 and 100 is {total}.")
```
---
