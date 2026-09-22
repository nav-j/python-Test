Absolutely. If this is your **final Python test**, I would include the complete syllabus from basic Python through **OOP, NumPy, Pandas, and Matplotlib**, with a balanced **theory + practical** structure.

# 🐍 Final Python Test — Theory + Practical

**Total Marks:** 100
**Time:** 3 Hours
**Theory:** 40 Marks
**Practical:** 60 Marks

### Topics Covered

* Python Basics
* Variables & Data Types
* Operators
* Conditional Statements
* `for` / `while` Loops
* Strings
* Lists, Tuples, Sets & Dictionaries
* Functions
* `break`, `continue`, `pass`
* Classes & Objects
* OOP Concepts
* NumPy
* Pandas
* Matplotlib

---

# PART A — THEORY

## 40 Marks

### Q1. Multiple Choice Questions

**10 × 1 = 10 Marks**

Choose the correct answer.

1. Which data type is immutable?

   * a) List
   * b) Set
   * c) Tuple
   * d) Dictionary

2. Which operator is used for exponentiation?

   * a) `^`
   * b) `**`
   * c) `//`
   * d) `%%`

3. Which keyword is used to create a function?

   * a) `function`
   * b) `func`
   * c) `def`
   * d) `define`

4. Which statement is used to stop a loop completely?

   * a) `skip`
   * b) `continue`
   * c) `break`
   * d) `stop`

5. Which keyword is used to create a class?

   * a) `object`
   * b) `class`
   * c) `define`
   * d) `struct`

6. Which library is mainly used for numerical array operations?

   * a) Pandas
   * b) NumPy
   * c) Matplotlib
   * d) Tkinter

7. Which Pandas object is one-dimensional?

   * a) DataFrame
   * b) Series
   * c) Array
   * d) Matrix

8. Which function is used to display a Matplotlib graph?

   * a) `graph()`
   * b) `display()`
   * c) `show()`
   * d) `plot()`

9. Which OOP concept allows a child class to acquire properties of a parent class?

   * a) Encapsulation
   * b) Inheritance
   * c) Abstraction
   * d) Polymorphism

10. Which function is commonly used to read a CSV file using Pandas?

* a) `pd.open_csv()`
* b) `pd.read_csv()`
* c) `pd.load_csv()`
* d) `pd.csv()`

---

## Q2. Short Answer Questions

### 5 × 2 = 10 Marks

Answer briefly.

1. What is the difference between a **list and a tuple**?
2. What is a **function** and why do we use functions?
3. What is a **class and object** in Python?
4. What is the difference between a **NumPy array and Python list**?
5. What is the difference between a **Series and DataFrame** in Pandas?

---

## Q3. Explain OOP Concepts

### 5 Marks

Explain the following OOP concepts with a short example:

1. Class
2. Object
3. Inheritance
4. Encapsulation
5. Polymorphism

---

## Q4. Output-Based Questions

### 3 × 3 = 9 Marks

### A.

```python
numbers = [10, 20, 30, 40, 50]

for num in numbers:
    if num > 25:
        print(num)
```

Write the output.

---

### B.

```python
import numpy as np

arr = np.array([10, 20, 30, 40])

print(arr * 2)
print(arr.mean())
```

Write the output.

---

### C.

```python
student = {
    "name": "Aman",
    "marks": 85
}

print(student["name"])
print(student["marks"] + 5)
```

Write the output.

---

## Q5. Difference Between

### 3 × 2 = 6 Marks

Explain the difference between:

1. `for` loop and `while` loop
2. Class and Object
3. NumPy and Pandas

---

# PART B — PRACTICAL

## 60 Marks

## Q6. Python Basics & Loops

### 10 Marks

Create a **Student Result Program**.

The program should:

1. Take student's name.
2. Take marks of 5 subjects.
3. Calculate total and percentage.
4. Display grade using `if-elif-else`.
5. Display **Pass/Fail**.
6. Use a loop to accept the five subject marks.

Grade system:

```text
90+       A+
80–89     A
70–79     B
60–69     C
50–59     D
Below 50  F
```

---

# Q7. Functions, Lists & Dictionaries

### 10 Marks

Create an **Employee Management Program**.

Create a function:

```python
add_employee()
```

The program should:

1. Store employee details in a dictionary.
2. Store multiple employees in a list.
3. Take:

   * Employee ID
   * Name
   * Department
   * Salary
4. Display all employees.
5. Search for an employee using Employee ID.
6. Update the salary of an employee.
7. Delete an employee.

---

# Q8. Classes & OOP

### 10 Marks

Create a class called:

```python
BankAccount
```

The class should contain:

### Attributes

* Account holder name
* Account number
* Balance

### Methods

```python
deposit()
withdraw()
display_balance()
```

Requirements:

1. Create an object of the class.
2. Allow the user to deposit money.
3. Allow the user to withdraw money.
4. Do not allow withdrawal if the balance is insufficient.
5. Display the final balance.

### Bonus OOP Requirement

Create another class:

```python
SavingsAccount
```

that inherits from `BankAccount`.

Add an additional method:

```python
add_interest()
```

This will test **class, object, methods, constructor and inheritance**.

---

# Q9. NumPy Practical

### 10 Marks

Create a NumPy array containing:

```python
[10, 20, 30, 40, 50, 60, 70, 80, 90, 100]
```

Perform the following operations:

1. Display the array.
2. Display its shape.
3. Display its size.
4. Find the maximum value.
5. Find the minimum value.
6. Find the mean.
7. Find the sum.
8. Multiply every element by 2.
9. Display elements greater than 50.
10. Reshape the array into a **2 × 5** array.

---

# Q10. Pandas Practical

### 10 Marks

Create the following DataFrame:

| Name   | Age | Department | Salary |
| ------ | --: | ---------- | -----: |
| Aman   |  25 | IT         |  35000 |
| Neha   |  28 | HR         |  40000 |
| Rahul  |  30 | IT         |  50000 |
| Simran |  26 | Marketing  |  38000 |
| Karan  |  32 | IT         |  55000 |

Perform the following:

1. Display the complete DataFrame.
2. Display the first 3 records.
3. Display only the `Name` and `Salary` columns.
4. Find employees whose salary is greater than 40000.
5. Find the average salary.
6. Find the maximum salary.
7. Add a new column called `Bonus`.
8. Calculate bonus as **10% of salary**.
9. Sort employees according to salary.
10. Display basic information about the DataFrame using `info()`.

---

# Q11. Matplotlib Practical

### 10 Marks

Using Matplotlib, create a graph for the following data:

```python
months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun"]

sales = [12000, 15000, 13000, 18000, 22000, 20000]
```

Create a **line chart** that includes:

1. X-axis label — `Months`
2. Y-axis label — `Sales`
3. Chart title — `Monthly Sales`
4. Markers on data points
5. Grid
6. Display the graph using `plt.show()`.

### Additional Task

Create a **bar chart** using the same data.

---

# 📊 FINAL MARKING SCHEME

| Question  | Topic                           |   Marks |
| --------- | ------------------------------- | ------: |
| Q1        | MCQs                            |      10 |
| Q2        | Basic Python + Libraries Theory |      10 |
| Q3        | OOP Theory                      |       5 |
| Q4        | Output Questions                |       9 |
| Q5        | Differences                     |       6 |
| Q6        | Python Basics & Loops           |      10 |
| Q7        | Functions, Lists & Dictionaries |      10 |
| Q8        | Classes & OOP                   |      10 |
| Q9        | NumPy                           |      10 |
| Q10       | Pandas                          |      10 |
| Q11       | Matplotlib                      |      10 |
| **TOTAL** |                                 | **100** |

### ✅ Final Syllabus Coverage

**Core Python:**
Variables → Data Types → Operators → Input/Output → Conditions → Loops → Strings → Lists → Tuples → Sets → Dictionaries → Functions

**Advanced Python:**
Classes → Objects → Constructors → Methods → Encapsulation → Inheritance → Polymorphism

**Libraries:**
NumPy → Arrays → Array Operations → Statistics → Reshaping

Pandas → Series → DataFrame → Filtering → Sorting → Columns → CSV concepts → Data Analysis

Matplotlib → Line Plot → Bar Plot → Labels → Titles → Grid → Markers

This structure gives students a **proper final assessment rather than just a basic Python test**, because it tests both their Python fundamentals and their ability to work with the three major data-analysis/visualization libraries.
