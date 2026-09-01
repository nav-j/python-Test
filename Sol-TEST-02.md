Sure. Below are the **complete solutions for all 5 Python practical tasks**, written at a beginner/intermediate level and matching the questions exactly.

## Task 1 — Student Marks System — 10 Marks

```python
# Student Marks System

name = input("Enter student name: ")
age = int(input("Enter age: "))

python_marks = int(input("Enter Python marks: "))
linux_marks = int(input("Enter Linux marks: "))
aws_marks = int(input("Enter AWS marks: "))

# Calculate total
total = python_marks + linux_marks + aws_marks

# Calculate average
average = total / 3

# Check average
if average >= 40:
    print("Result: Pass")
else:
    print("Result: Fail")

# Display details
print("\nName:", name)
print("Age:", age)
print("Total Marks:", total)
print("Average:", average)

# Display data types
print("Age Type:", type(age))
print("Average Type:", type(average))
```

---

## Task 2 — Shopping List — 10 Marks

```python
# Shopping List

items = ["Laptop", "Mouse", "Keyboard", "Monitor"]

# 1. Print first item
print("First item:", items[0])

# 2. Print last item
print("Last item:", items[-1])

# 3. Change Mouse to Wireless Mouse
items[1] = "Wireless Mouse"

# 4. Add Headphones
items.append("Headphones")

# 5. Add USB Cable at index 1
items.insert(1, "USB Cable")

# 6. Remove Monitor
items.remove("Monitor")

# 7. Print final list
print("\nFinal List:")
print(items)

# Display each item separately
print("\nItems:")
for item in items:
    print(item)
```

### Output

```text
First item: Laptop
Last item: Monitor

Final List:
['Laptop', 'USB Cable', 'Wireless Mouse', 'Keyboard', 'Headphones']

Items:
Laptop
USB Cable
Wireless Mouse
Keyboard
Headphones
```

---

## Task 3 — Number Calculator — 10 Marks

```python
# Number Calculator

num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

# Calculations
addition = num1 + num2
subtraction = num1 - num2
multiplication = num1 * num2
division = num1 / num2
floor_division = num1 // num2
modulus = num1 % num2
power = num1 ** num2

# Display results
print("\nAddition:", addition)
print("Subtraction:", subtraction)
print("Multiplication:", multiplication)
print("Division:", division)
print("Floor Division:", floor_division)
print("Modulus:", modulus)
print("Power:", power)
```

For input:

```text
Enter first number: 20
Enter second number: 6
```

Output:

```text
Addition: 26
Subtraction: 14
Multiplication: 120
Division: 3.3333333333333335
Floor Division: 3
Modulus: 2
Power: 64000000
```

If you want division to display **3.33**, use:

```python
print("Division:", round(division, 2))
```

---

## Task 4 — Grocery List Manager — 10 Marks

```python
# Grocery List Manager

grocery = []

# Ask user to enter 5 grocery items
for i in range(5):
    item = input("Enter grocery item: ")
    grocery.append(item)

# 1. Display complete list
print("\nComplete Grocery List:")
print(grocery)

# 2. Display item at index 0
print("Item at index 0:", grocery[0])

# 3. Display item at index 3
print("Item at index 3:", grocery[3])

# 4. Ask for a new item and add it
new_item = input("\nEnter a new grocery item: ")
grocery.append(new_item)

# 5. Ask which item to remove
remove_item = input("Enter the item you want to remove: ")

# 6. Remove the item
if remove_item in grocery:
    grocery.remove(remove_item)
else:
    print("Item not found.")

# 7. Change item at index 1 to Milk
grocery[1] = "Milk"

# 8. Display all remaining items
print("\nRemaining Grocery Items:")

for item in grocery:
    print(item)

# 9. Display total number of items
print("\nTotal number of items:", len(grocery))
```

### Important

The check:

```python
if remove_item in grocery:
```

prevents an error if the user enters an item that doesn't exist in the list.

---

## Task 5 — Student List Challenge — 10 Marks

```python
# Student List Challenge

students = ["Aman", "Rohit", "Simran", "Karan"]

# 1. Ask for a new student and add it
new_student = input("Enter a new student's name: ")
students.append(new_student)

# 2. Display first and last student
print("\nFirst Student:", students[0])
print("Last Student:", students[-1])

# 3. Ask for an index and display student
index = int(input("\nEnter an index number: "))

if index >= 0 and index < len(students):
    print("Student at index", index, ":", students[index])
else:
    print("Invalid index.")

# 4. Change Rohit to Rahul
students[1] = "Rahul"

# 5. Remove Karan
students.remove("Karan")

# 6. Ask for another student and add
another_student = input("\nEnter another student's name: ")
students.append(another_student)

# 7. Display every student
print("\nStudents:")

for student in students:
    print(student)

# 8. Display total number of students
total_students = len(students)

print("\nTotal number of students:", total_students)

# 9. Check whether students are greater than 4
if total_students > 4:
    print("Number of students is greater than 4.")
else:
    print("Number of students is not greater than 4.")
```

### Concepts covered in these 5 tasks

| Task   | Main Concepts                                                                                |
| ------ | -------------------------------------------------------------------------------------------- |
| Task 1 | Variables, `input()`, type conversion, arithmetic, `if-else`, `type()`                       |
| Task 2 | Lists, indexing, negative indexing, updating, `append()`, `insert()`, `remove()`, `for` loop |
| Task 3 | `int()`, arithmetic operators, floor division, modulus, power                                |
| Task 4 | Lists, `append()`, `remove()`, indexing, `len()`, `for` loop, `if`                           |
| Task 5 | Lists, indexing, `append()`, `remove()`, `len()`, comparison operator, `for` loop            |
