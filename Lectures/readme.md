### **Lecture Notes**

#### **1. File Handling**

Files are used to store data permanently.

##### **Opening Files**

```python
file = open('filename.txt', 'mode')
```

- **Modes:**
  - `'r'`: Read (default).
  - `'w'`: Write (overwrites).
  - `'a'`: Append.
  - `'r+'`: Read and write.

##### **Reading Files**

- **`read()`**: Reads the entire file.

  ```python
  content = file.read()
  ```

- **`readline()`**: Reads one line at a time.

  ```python
  line = file.readline()
  ```

- **`readlines()`**: Reads all lines into a list.

  ```python
  lines = file.readlines()
  ```

##### **Writing Files**

```python
file.write("Hello, World!")
```

##### **Closing Files**

```python
file.close()
```

##### **Using `with` Statement**

Automatically closes the file.

```python
with open('filename.txt', 'r') as file:
    content = file.read()
```

---

#### **2. Exception Handling Review**

Handling exceptions related to file operations.

**Example:**

```python
try:
    with open('nonexistent.txt', 'r') as file:
        content = file.read()
except FileNotFoundError:
    print("Error: File not found.")
```

---

#### **3. Introduction to OOP**

Object-oriented programming allows you to create classes that encapsulate data and functions.

##### **Defining Classes**

```python
class ClassName:
    def __init__(self, parameters):
        # Constructor method
        self.attribute = value

    def method(self):
        # Method definition
```

##### **Creating Objects**

```python
obj = ClassName(arguments)
```

##### **Example:**

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        print(f"{self.name} says woof!")

dog1 = Dog("Buddy")
dog1.bark()
```

**Output:**

```
Buddy says woof!
```

##### **Inheritance**

```python
class Puppy(Dog):
    def play(self):
        print(f"{self.name} is playing!")

puppy = Puppy("Max")
puppy.bark()
puppy.play()
```

**Output:**

```
Max says woof!
Max is playing!
```

---
