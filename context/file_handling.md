← [back to index page](../index.md)

# **1.5 File Handling**

File handling in Python allows you to create, read, update, and delete files. Python provides built-in methods and functions to work with files efficiently. Understanding file operations is critical for tasks like data processing, logging, and configuration management.

---

## **1.5.1 Reading and Writing Files**

### **Opening a File**
The `open()` function is used to open files. It returns a file object, which can be used for various file operations. The syntax is:
`open(file, mode)`
- `file`: The path of the file to open.
- `mode`: The mode in which the file is opened (e.g., read, write, append).

### **Modes**
| Mode  | Description                          |
|-------|--------------------------------------|
| `r`   | Read mode (default).                 |
| `w`   | Write mode (overwrites if exists).   |
| `a`   | Append mode.                         |
| `x`   | Create mode (fails if exists).       |
| `rb`  | Read binary.                         |
| `wb`  | Write binary.                        |

### **Reading Files**
```python
# Reading a file
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```
- **`read()`**: Reads the entire file.
- **`readline()`**: Reads one line at a time.
- **`readlines()`**: Reads all lines into a list.

```python
# Example: Reading lines
with open("example.txt", "r") as file:
    for line in file:
        print(line.strip())  # Print each line without trailing newline
```

### **Writing Files**
```python
# Writing to a file
with open("example.txt", "w") as file:
    file.write("Hello, World!")
```
- **`write()`**: Writes a string to the file.
- **`writelines()`**: Writes a list of strings.

### **Appending Files**
```python
# Appending to a file
with open("example.txt", "a") as file:
    file.write("\nThis is an appended line.")
```
---

## **1.5.2 Working with Different File Modes**

### **Binary Files**
Binary files store data in binary format (e.g., images, executables).

```python
# Writing binary data
data = b"Binary data example"
with open("binary_file.bin", "wb") as file:
    file.write(data)

# Reading binary data
with open("binary_file.bin", "rb") as file:
    content = file.read()
    print(content)
```
Binary mode is indicated by adding a `b` to the mode (e.g., `rb`, `wb`).

---

## **1.5.3 Handling File Exceptions**

When working with files, exceptions can occur (e.g., file not found, permission denied). Python provides tools to handle these exceptions gracefully.

### **Try-Except for File Handling**
```python
# Example: Handling file not found
try:
    with open("nonexistent_file.txt", "r") as file:
        content = file.read()
except FileNotFoundError:
    print("File not found.")
```
### **Using `finally`**
The `finally` block ensures cleanup, like closing the file, even if an exception occurs.

```python
# Example: Using finally
file = None
try:
    file = open("example.txt", "r")
    content = file.read()
except FileNotFoundError:
    print("File not found.")
finally:
    if file:
        file.close()
```
---

## **Additional Features**

### **Checking if a File Exists**
The `os` module allows you to check file existence.

```python
import os
if os.path.exists("example.txt"):
    print("File exists.")
else:
    print("File does not exist.")
```

### **Deleting a File**
```python
# Example: Deleting a file
import os
if os.path.exists("example.txt"):
    os.remove("example.txt")
    print("File deleted.")
else:
    print("File does not exist.")
```
---

# **Tasks for Chapter 1.5**

## **Task 1: Word Counter**
Write a program to read a text file and count the number of words in it.

### **Solution:**
```python
# Word counter
try:
    with open("example.txt", "r") as file:
        content = file.read()
        words = content.split()
        print(f"Word count: {len(words)}")
except FileNotFoundError:
    print("File not found.")
```
---

## **Task 2: Copy File Content**
Write a program to copy the content of one file to another.

### **Solution:**
```python
# File copy
try:
    with open("source.txt", "r") as source_file:
        content = source_file.read()
    with open("destination.txt", "w") as destination_file:
        destination_file.write(content)
    print("File copied successfully.")
except FileNotFoundError:
    print("Source file not found.")
```
---

## **Task 3: Log File Creator**
Write a program that appends log messages to a log file with timestamps.

### **Solution:**
```python
# Log file creator
from datetime import datetime

def log_message(message):
    timestamp = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    with open("log.txt", "a") as log_file:
        log_file.write(f"[{timestamp}] {message}\n")

log_message("Application started.")
log_message("Another log entry.")
```
---

← [back to index page](../index.md)