← [back to index page](../index.md)
# **1.4 Data Structures**

Data structures are essential for organizing, storing, and manipulating data efficiently. Python offers a variety of built-in data structures, each suited to specific tasks.

---

## **1.4.1 Lists**

A list is an ordered, mutable collection of items. Lists can hold elements of any type and even a mix of types.

### **Creating Lists**
```python
# Example: Creating lists
empty_list = []
numbers = [1, 2, 3, 4, 5]
mixed_list = [1, "apple", 3.14, True]
print(mixed_list)
```

### **Accessing and Modifying Elements**
Lists are zero-indexed, meaning the first element is at index `0`.

```python
# Accessing elements
numbers = [10, 20, 30, 40]
print(numbers[0])  # Output: 10

# Modifying elements
numbers[2] = 99
print(numbers)  # Output: [10, 20, 99, 40]
```

### **Common List Operations**
- **Appending**: Add an item to the end.
- **Removing**: Remove a specific item or by index.
- **Sorting**: Organize elements in ascending or descending order.

```python
numbers = [3, 1, 4, 1, 5]
numbers.append(9)
print(numbers)  # Output: [3, 1, 4, 1, 5, 9]

numbers.remove(1)
print(numbers)  # Output: [3, 4, 1, 5, 9]

numbers.sort()
print(numbers)  # Output: [1, 3, 4, 5, 9]
```

---

## **1.4.2 Tuples**

A tuple is an ordered, immutable collection of items. Once created, you cannot modify it.

### **Creating Tuples**
```python
# Example: Creating tuples
empty_tuple = ()
coordinates = (10, 20)
mixed_tuple = (1, "apple", 3.14)
```

### **Accessing Tuple Elements**
You can access elements in a tuple using indices.

```python
# Accessing elements
coordinates = (10, 20, 30)
print(coordinates[1])  # Output: 20
```

### **Why Use Tuples?**
- Tuples are more memory-efficient than lists.
- They are used for fixed data that should not change, like geographic coordinates.

---

## **1.4.3 Sets**

A set is an unordered collection of unique items. Duplicates are automatically removed.

### **Creating Sets**
```python
# Example: Creating sets
numbers = {1, 2, 3, 3, 4}
print(numbers)  # Output: {1, 2, 3, 4}
```

### **Set Operations**
- **Union**: Combine elements from two sets.
- **Intersection**: Find common elements.
- **Difference**: Find elements in one set but not the other.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

print(set_a | set_b)  # Union: {1, 2, 3, 4, 5}
print(set_a & set_b)  # Intersection: {3}
print(set_a - set_b)  # Difference: {1, 2}
```

---

## **1.4.4 Dictionaries**

A dictionary is a collection of key-value pairs. Keys must be unique, and values can be of any type.

### **Creating Dictionaries**
```python
# Example: Creating dictionaries
person = {"name": "Alice", "age": 25, "city": "New York"}
print(person)
```

### **Accessing and Modifying Values**
```python
# Accessing and modifying values
print(person["name"])  # Output: Alice
person["age"] = 30
print(person)  # Output: {'name': 'Alice', 'age': 30, 'city': 'New York'}
```

### **Common Dictionary Operations**
- **Adding a Key-Value Pair**
- **Deleting a Key**
- **Iterating Through Keys and Values**

```python
# Adding and deleting keys
person["profession"] = "Engineer"
del person["city"]
print(person)  # Output: {'name': 'Alice', 'age': 30, 'profession': 'Engineer'}

# Iterating through keys and values
for key, value in person.items():
    print(f"{key}: {value}")
```
---

## **1.4.5 Nested Data Structures**

Data structures can be nested to represent more complex relationships.

```python
# Example: Nested data structures
company = {
    "name": "TechCorp",
    "departments": [
        {"name": "HR", "employees": 10},
        {"name": "Engineering", "employees": 50}
    ]
}

print(company["departments"][1]["name"])  # Output: Engineering
```
---

# **Tasks for Chapter 1.4**

## **Task 1: Unique Elements**
Write a program that takes a list of numbers and returns a set of unique elements.

### **Solution:**
```python
# Unique elements
numbers = [1, 2, 2, 3, 4, 4, 5]
unique_numbers = set(numbers)
print(unique_numbers)  # Output: {1, 2, 3, 4, 5}
```

---

## **Task 2: Student Grades**
Create a dictionary where keys are student names and values are their grades. Write a program to display each student's name and grade.

### **Solution:**
```python
# Student grades
grades = {"Alice": 85, "Bob": 90, "Charlie": 78}
for student, grade in grades.items():
    print(f"{student}: {grade}")
```
---

## **Task 3: Shopping Cart**
Write a program to represent a shopping cart. The cart should store item names as keys and their quantities as values. Add functionality to:
1. Add items to the cart.
2. Remove items.
3. Display the total items in the cart.

### **Solution:**
```python
# Shopping cart
cart = {}

def add_item(item, quantity):
    cart[item] = cart.get(item, 0) + quantity

def remove_item(item):
    if item in cart:
        del cart[item]

def display_cart():
    print("Shopping Cart:")
    for item, quantity in cart.items():
        print(f"{item}: {quantity}")

# Example usage
add_item("Apple", 3)
add_item("Banana", 2)
remove_item("Apple")
display_cart()
```
---

← [back to index page](../index.md)