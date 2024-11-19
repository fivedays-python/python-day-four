### **Exercises**

#### **Exercise 1: Vowel Counter**

**Objective:** Write a program that reads a text file and counts the number of vowels.

**Instructions:**

1. Prompt the user for the filename.
2. Read the file content.
3. Count and display the number of vowels (`a`, `e`, `i`, `o`, `u`).

**Solution:**

```python
def count_vowels(filename):
    vowels = "aeiouAEIOU"
    count = 0
    try:
        with open(filename, 'r') as file:
            text = file.read()
            for char in text:
                if char in vowels:
                    count += 1
        print(f"Total vowels: {count}")
    except FileNotFoundError:
        print("Error: File not found.")

file_name = input("Enter the filename: ")
count_vowels(file_name)
```

---

#### **Exercise 2: Simple Bank Account Class**

**Objective:** Create a `BankAccount` class with methods to deposit, withdraw, and check the balance.

**Instructions:**

1. Define a `BankAccount` class with an attribute `balance`.
2. Implement methods:
   - `deposit(amount)`
   - `withdraw(amount)`
   - `get_balance()`
3. Create an object and demonstrate using the methods.

**Solution:**

```python
class BankAccount:
    def __init__(self):
        self.balance = 0.0

    def deposit(self, amount):
        self.balance += amount
        print(f"Deposited: ${amount:.2f}")

    def withdraw(self, amount):
        if amount > self.balance:
            print("Insufficient funds.")
        else:
            self.balance -= amount
            print(f"Withdrawn: ${amount:.2f}")

    def get_balance(self):
        print(f"Current Balance: ${self.balance:.2f}")

# Usage
account = BankAccount()
account.deposit(100)
account.withdraw(30)
account.get_balance()
```

**Output:**

```
Deposited: $100.00
Withdrawn: $30.00
Current Balance: $70.00
```

---
