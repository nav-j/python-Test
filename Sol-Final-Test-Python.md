Absolutely. Below is the **complete solution/answer key** for the final Python Theory + Practical Test, including **Python basics, loops, functions, OOP, NumPy, Pandas, and Matplotlib**.

# 🐍 Final Python Test — Complete Solution

## PART A — THEORY SOLUTIONS

### Q1. Multiple Choice Questions

| Q  | Answer                 | Explanation                                                             |
| -- | ---------------------- | ----------------------------------------------------------------------- |
| 1  | **c) Tuple**           | Tuples are immutable.                                                   |
| 2  | **b) `**`**            | `**` is the exponentiation operator.                                    |
| 3  | **c) `def`**           | `def` is used to define a function.                                     |
| 4  | **c) `break`**         | `break` terminates the loop.                                            |
| 5  | **b) `class`**         | `class` is used to create a class.                                      |
| 6  | **b) NumPy**           | NumPy is mainly used for numerical and array operations.                |
| 7  | **b) Series**          | A Pandas Series is one-dimensional.                                     |
| 8  | **c) `show()`**        | `plt.show()` displays a Matplotlib graph.                               |
| 9  | **b) Inheritance**     | Inheritance allows a child class to acquire features of a parent class. |
| 10 | **b) `pd.read_csv()`** | It is used to read CSV files into a Pandas DataFrame.                   |

---

# Q2. Short Answer Questions

### 1. Difference between List and Tuple

**List:**

* Ordered
* Mutable
* Uses `[ ]`

```python
numbers = [10, 20, 30]
numbers[0] = 100
```

**Tuple:**

* Ordered
* Immutable
* Uses `( )`

```python
numbers = (10, 20, 30)
```

---

### 2. What is a Function?

A function is a reusable block of code designed to perform a particular task.

Example:

```python
def add(a, b):
    return a + b

print(add(10, 20))
```

Functions help make programs **reusable, organized, and easier to maintain**.

---

### 3. What is a Class and Object?

A **class** is a blueprint for creating objects.

An **object** is an instance of a class.

```python
class Student:
    name = "Aman"

student1 = Student()

print(student1.name)
```

Here:

* `Student` → Class
* `student1` → Object

---

### 4. Difference between NumPy Array and Python List

**Python List:**

```python
numbers = [10, 20, 30]
```

**NumPy Array:**

```python
import numpy as np

numbers = np.array([10, 20, 30])
```

NumPy arrays are designed for **fast numerical calculations** and support vectorized mathematical operations.

---

### 5. Difference between Series and DataFrame

A **Series** is a one-dimensional data structure.

```python
import pandas as pd

s = pd.Series([10, 20, 30])
```

A **DataFrame** is a two-dimensional table containing rows and columns.

```python
df = pd.DataFrame({
    "Name": ["Aman", "Neha"],
    "Age": [25, 28]
})
```

---

# Q3. OOP Concepts

### 1. Class

A class is a blueprint for creating objects.

```python
class Student:
    pass
```

### 2. Object

An object is an instance of a class.

```python
student1 = Student()
```

### 3. Inheritance

Inheritance allows one class to inherit properties and methods from another class.

```python
class Animal:
    def eat(self):
        print("Eating")

class Dog(Animal):
    pass

d = Dog()
d.eat()
```

### 4. Encapsulation

Encapsulation means combining data and methods inside a class and controlling access to the data.

```python
class Student:
    def __init__(self):
        self.__marks = 90
```

`__marks` is treated as a private attribute.

### 5. Polymorphism

Polymorphism means the same method/interface can behave differently for different objects.

```python
class Dog:
    def sound(self):
        print("Bark")

class Cat:
    def sound(self):
        print("Meow")

for animal in [Dog(), Cat()]:
    animal.sound()
```

---

# Q4. Output-Based Questions

## A.

```python
numbers = [10, 20, 30, 40, 50]

for num in numbers:
    if num > 25:
        print(num)
```

### Output:

```text
30
40
50
```

---

## B.

```python
import numpy as np

arr = np.array([10, 20, 30, 40])

print(arr * 2)
print(arr.mean())
```

### Output:

```text
[20 40 60 80]
25.0
```

---

## C.

```python
student = {
    "name": "Aman",
    "marks": 85
}

print(student["name"])
print(student["marks"] + 5)
```

### Output:

```text
Aman
90
```

---

# Q5. Difference Between

### 1. `for` loop vs `while` loop

| `for`                                                        | `while`                                   |
| ------------------------------------------------------------ | ----------------------------------------- |
| Generally used when iterating over a sequence or known range | Used when a condition controls repetition |
| Commonly used with `range()`                                 | Depends on a condition                    |
| Example: `for i in range(5)`                                 | Example: `while i < 5`                    |

Example:

```python
for i in range(5):
    print(i)
```

```python
i = 0

while i < 5:
    print(i)
    i += 1
```

---

### 2. `break` vs `continue`

**`break`** completely terminates the loop.

```python
for i in range(1, 6):
    if i == 3:
        break
    print(i)
```

Output:

```text
1
2
```

**`continue`** skips the current iteration and continues with the next iteration.

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

Output:

```text
1
2
4
5
```

---

### 3. Class vs Object

**Class:** Blueprint/template.

**Object:** Actual instance created from that class.

```python
class Car:
    pass

car1 = Car()
```

Here:

```text
Car   → Class
car1  → Object
```

---

# PART B — PRACTICAL SOLUTIONS

# Q6. Student Result Program

### Solution

```python
name = input("Enter student name: ")

marks = []

for i in range(1, 6):
    mark = float(input(f"Enter marks for subject {i}: "))
    marks.append(mark)

total = sum(marks)
percentage = total / 5

if percentage >= 90:
    grade = "A+"
elif percentage >= 80:
    grade = "A"
elif percentage >= 70:
    grade = "B"
elif percentage >= 60:
    grade = "C"
elif percentage >= 50:
    grade = "D"
else:
    grade = "F"

# Check whether every subject has at least 40 marks
if all(mark >= 40 for mark in marks):
    result = "Pass"
else:
    result = "Fail"

print("\n----- Student Result -----")
print("Name:", name)
print("Marks:", marks)
print("Total:", total)
print("Percentage:", percentage)
print("Grade:", grade)
print("Result:", result)
```

### Important point

The student must score **at least 40 in every subject** to pass.

For example:

```text
Marks = [80, 75, 65, 35, 90]
```

Even though the overall percentage may be above 50, the result is:

```text
Fail
```

because one subject is below 40.

---

# Q7. Employee Management Program

### Solution

```python
employees = []


def add_employee():
    employee_id = input("Enter employee ID: ")
    name = input("Enter employee name: ")
    department = input("Enter department: ")
    salary = float(input("Enter salary: "))

    employee = {
        "id": employee_id,
        "name": name,
        "department": department,
        "salary": salary
    }

    employees.append(employee)
    print("Employee added successfully.")


def display_employees():
    if len(employees) == 0:
        print("No employees found.")
        return

    print("\n----- Employee Records -----")

    for employee in employees:
        print("ID:", employee["id"])
        print("Name:", employee["name"])
        print("Department:", employee["department"])
        print("Salary:", employee["salary"])
        print("------------------------")


def search_employee():
    employee_id = input("Enter employee ID to search: ")

    for employee in employees:
        if employee["id"] == employee_id:
            print("\nEmployee Found")
            print("ID:", employee["id"])
            print("Name:", employee["name"])
            print("Department:", employee["department"])
            print("Salary:", employee["salary"])
            return

    print("Employee not found.")


def update_salary():
    employee_id = input("Enter employee ID: ")

    for employee in employees:
        if employee["id"] == employee_id:
            new_salary = float(input("Enter new salary: "))
            employee["salary"] = new_salary

            print("Salary updated successfully.")
            return

    print("Employee not found.")


def delete_employee():
    employee_id = input("Enter employee ID: ")

    for employee in employees:
        if employee["id"] == employee_id:
            employees.remove(employee)
            print("Employee deleted successfully.")
            return

    print("Employee not found.")


while True:

    print("\n===== Employee Management =====")
    print("1. Add Employee")
    print("2. Display Employees")
    print("3. Search Employee")
    print("4. Update Salary")
    print("5. Delete Employee")
    print("6. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        add_employee()

    elif choice == "2":
        display_employees()

    elif choice == "3":
        search_employee()

    elif choice == "4":
        update_salary()

    elif choice == "5":
        delete_employee()

    elif choice == "6":
        print("Program ended.")
        break

    else:
        print("Invalid choice.")
```

### Concepts used

* List
* Dictionary
* Functions
* `for` loop
* `while` loop
* `if-elif-else`
* Searching
* Updating
* Deleting

---

# Q8. Classes & OOP — Bank Account

### Solution

```python
class BankAccount:

    def __init__(self, name, account_number, balance):
        self.name = name
        self.account_number = account_number
        self.balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            print("Amount deposited successfully.")
        else:
            print("Invalid amount.")

    def withdraw(self, amount):
        if amount <= 0:
            print("Invalid amount.")

        elif amount > self.balance:
            print("Insufficient balance.")

        else:
            self.balance -= amount
            print("Amount withdrawn successfully.")

    def display_balance(self):
        print("Account Holder:", self.name)
        print("Account Number:", self.account_number)
        print("Current Balance:", self.balance)


# Create object
account = BankAccount("Aman", "ACC101", 10000)

account.display_balance()

print("\nDepositing ₹2000")
account.deposit(2000)

print("\nWithdrawing ₹3000")
account.withdraw(3000)

print("\nFinal Account Details")
account.display_balance()
```

---

## Inheritance — SavingsAccount

```python
class BankAccount:

    def __init__(self, name, account_number, balance):
        self.name = name
        self.account_number = account_number
        self.balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            print("Amount deposited successfully.")
        else:
            print("Invalid amount.")

    def withdraw(self, amount):
        if amount > self.balance:
            print("Insufficient balance.")
        elif amount <= 0:
            print("Invalid amount.")
        else:
            self.balance -= amount
            print("Amount withdrawn successfully.")

    def display_balance(self):
        print("Name:", self.name)
        print("Account Number:", self.account_number)
        print("Balance:", self.balance)


class SavingsAccount(BankAccount):

    def add_interest(self):
        interest = self.balance * 0.05
        self.balance += interest

        print("Interest added:", interest)


account = SavingsAccount(
    "Aman",
    "SA101",
    10000
)

account.display_balance()

account.deposit(2000)

account.withdraw(1000)

account.add_interest()

print("\nFinal Details:")
account.display_balance()
```

### OOP concepts demonstrated

```text
BankAccount       → Parent Class
SavingsAccount    → Child Class
account           → Object
__init__()        → Constructor
deposit()         → Method
withdraw()        → Method
add_interest()    → Child-class method
Inheritance       → SavingsAccount inherits BankAccount
```

---

# Q9. NumPy Practical

### Solution

```python
import numpy as np

arr = np.array([
    10, 20, 30, 40, 50,
    60, 70, 80, 90, 100
])

print("Array:")
print(arr)

print("\nShape:")
print(arr.shape)

print("\nSize:")
print(arr.size)

print("\nMaximum:")
print(arr.max())

print("\nMinimum:")
print(arr.min())

print("\nMean:")
print(arr.mean())

print("\nSum:")
print(arr.sum())

print("\nArray multiplied by 2:")
print(arr * 2)

print("\nElements greater than 50:")
print(arr[arr > 50])

print("\nReshaped Array:")
print(arr.reshape(2, 5))
```

### Expected Output

```text
Array:
[ 10  20  30  40  50  60  70  80  90 100]

Shape:
(10,)

Size:
10

Maximum:
100

Minimum:
10

Mean:
55.0

Sum:
550

Array multiplied by 2:
[ 20  40  60  80 100 120 140 160 180 200]

Elements greater than 50:
[ 60  70  80  90 100]

Reshaped Array:
[[ 10  20  30  40  50]
 [ 60  70  80  90 100]]
```

---

# Q10. Pandas Practical

### Solution

```python
import pandas as pd

data = {
    "Name": ["Aman", "Neha", "Rahul", "Simran", "Karan"],
    "Age": [25, 28, 30, 26, 32],
    "Department": [
        "IT",
        "HR",
        "IT",
        "Marketing",
        "IT"
    ],
    "Salary": [35000, 40000, 50000, 38000, 55000]
}

df = pd.DataFrame(data)

# 1. Display complete DataFrame
print("Complete DataFrame:")
print(df)

# 2. First 3 records
print("\nFirst 3 Records:")
print(df.head(3))

# 3. Name and Salary
print("\nName and Salary:")
print(df[["Name", "Salary"]])

# 4. Salary greater than 40000
print("\nEmployees with Salary > 40000:")
print(df[df["Salary"] > 40000])

# 5. Average salary
print("\nAverage Salary:")
print(df["Salary"].mean())

# 6. Maximum salary
print("\nMaximum Salary:")
print(df["Salary"].max())

# 7. Add Bonus column
df["Bonus"] = df["Salary"] * 0.10

print("\nDataFrame with Bonus:")
print(df)

# 8. Bonus is already calculated above

# 9. Sort according to salary
print("\nSorted by Salary:")
print(df.sort_values("Salary"))

# 10. DataFrame information
print("\nDataFrame Information:")
df.info()
```

### Important Pandas operations

```python
df.head(3)
```

Displays the first 3 rows.

```python
df[["Name", "Salary"]]
```

Selects specific columns.

```python
df[df["Salary"] > 40000]
```

Filters records.

```python
df["Salary"].mean()
```

Calculates average salary.

```python
df["Salary"].max()
```

Finds maximum salary.

```python
df["Bonus"] = df["Salary"] * 0.10
```

Creates a new column.

```python
df.sort_values("Salary")
```

Sorts the DataFrame by salary.

```python
df.info()
```

Displays information about columns, data types, and non-null values.

---

# Q11. Matplotlib Practical

## Line Chart Solution

```python
import matplotlib.pyplot as plt

months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun"]

sales = [12000, 15000, 13000, 18000, 22000, 20000]

plt.plot(
    months,
    sales,
    marker="o"
)

plt.xlabel("Months")
plt.ylabel("Sales")

plt.title("Monthly Sales")

plt.grid()

plt.show()
```

---

## Bar Chart Solution

```python
import matplotlib.pyplot as plt

months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun"]

sales = [12000, 15000, 13000, 18000, 22000, 20000]

plt.bar(months, sales)

plt.xlabel("Months")
plt.ylabel("Sales")

plt.title("Monthly Sales")

plt.show()
```

---

# 📚 Quick Revision — Important Syntax

### Variables

```python
name = "Aman"
age = 25
salary = 35000
```

### Condition

```python
if age >= 18:
    print("Adult")
else:
    print("Minor")
```

### For Loop

```python
for i in range(1, 11):
    print(i)
```

### While Loop

```python
i = 1

while i <= 10:
    print(i)
    i += 1
```

### Function

```python
def add(a, b):
    return a + b
```

### List

```python
fruits = ["Apple", "Mango", "Banana"]
```

### Tuple

```python
numbers = (10, 20, 30)
```

### Set

```python
numbers = {10, 20, 30}
```

### Dictionary

```python
student = {
    "name": "Aman",
    "age": 20
}
```

### Class

```python
class Student:

    def __init__(self, name):
        self.name = name

student1 = Student("Aman")
```

### NumPy

```python
import numpy as np

arr = np.array([10, 20, 30])
```

### Pandas

```python
import pandas as pd

df = pd.DataFrame(data)
```

### Matplotlib

```python
import matplotlib.pyplot as plt

plt.plot(x, y)
plt.show()
```

## Final Topic Coverage

```text
Python Basics
     ↓
Variables & Data Types
     ↓
Operators
     ↓
Conditions
     ↓
Loops
     ↓
Strings
     ↓
List / Tuple / Set / Dictionary
     ↓
Functions
     ↓
Classes & Objects
     ↓
OOP
     ↓
NumPy
     ↓
Pandas
     ↓
Matplotlib
```

This solution set covers all **100 marks** of the test and provides runnable code for each practical question.

If you're using this for your students at **KUBEARC Academy**, I can also turn this into a **professional student question paper + separate teacher answer key**, with the question paper containing **no solutions/hints**.
