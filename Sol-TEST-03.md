Here is the **complete solution** for the 50-mark Sets and Dictionaries practical task.

# Python Practical Solution — Sets & Dictionaries

## Question 1 — Set Operations

```python
students_python = {"Aman", "Simran", "Ravi", "Neha", "Karan"}
students_java = {"Ravi", "Neha", "Pooja", "Karan", "Raj"}

# 1. Students in both Python and Java
both = students_python & students_java
print("Students in both courses:", both)

# 2. Students only in Python
python_only = students_python - students_java
print("Students only in Python:", python_only)

# 3. Students in at least one course
all_students = students_python | students_java
print("Students in at least one course:", all_students)

# 4. Students enrolled in both courses
both_courses = students_python.intersection(students_java)
print("Students in both courses:", both_courses)

# 5. Total number of unique students
print("Total unique students:", len(all_students))
```

### Important operators

```text
&  → Intersection
|  → Union
-  → Difference
```

---

# Question 2 — Set Methods

```python
fruits = {"apple", "banana", "mango", "orange"}

# 1. Add one fruit
fruits.add("grapes")
print("After adding grapes:", fruits)

# 2. Add multiple fruits
fruits.update(["kiwi", "papaya"])
print("After adding kiwi and papaya:", fruits)

# 3. Remove banana
fruits.remove("banana")
print("After removing banana:", fruits)

# 4. Check whether mango exists
if "mango" in fruits:
    print("Mango exists in the set")
else:
    print("Mango does not exist")

# 5. Find length
print("Number of fruits:", len(fruits))
```

### Explanation

`add()` adds **one item**:

```python
fruits.add("grapes")
```

`update()` adds **multiple items**:

```python
fruits.update(["kiwi", "papaya"])
```

`remove()` removes an item:

```python
fruits.remove("banana")
```

---

# Question 3 — Student Dictionary

```python
student = {
    "name": "Navjot",
    "age": 30,
    "course": "Python",
    "marks": 85
}

# 1. Print student's name
print("Name:", student["name"])

# 2. Print student's course
print("Course:", student["course"])

# 3. Update marks
student["marks"] = 90

# 4. Add city
student["city"] = "Ludhiana"

# 5. Print all keys and values
for key, value in student.items():
    print(key, ":", value)
```

### Output

The final dictionary will contain:

```text
name : Navjot
age : 30
course : Python
marks : 90
city : Ludhiana
```

### Important concept

To access a value:

```python
student["name"]
```

To update a value:

```python
student["marks"] = 90
```

To add a new key:

```python
student["city"] = "Ludhiana"
```

To loop through both keys and values:

```python
for key, value in student.items():
    print(key, value)
```

---

# Question 4 — Multiple Students Dictionary

```python
students = {
    "Aman": 78,
    "Simran": 92,
    "Ravi": 65,
    "Neha": 88,
    "Karan": 55
}

# 1. Print all student names
print("Student Names:")

for name in students.keys():
    print(name)

# 2. Print all marks
print("\nMarks:")

for mark in students.values():
    print(mark)

# 3. Find student with highest marks
highest_student = max(students, key=students.get)
print("\nHighest Marks:")
print(highest_student, students[highest_student])

# 4. Find student with lowest marks
lowest_student = min(students, key=students.get)
print("\nLowest Marks:")
print(lowest_student, students[lowest_student])

# 5. Calculate average marks
total = sum(students.values())
average = total / len(students)

print("\nAverage Marks:", average)
```

### Expected Output

```text
Highest Marks:
Simran 92

Lowest Marks:
Karan 55

Average Marks: 75.6
```

### Important concept

This line:

```python
max(students, key=students.get)
```

finds the **key whose value is highest**.

Similarly:

```python
min(students, key=students.get)
```

finds the key whose value is lowest.

---

# Question 5 — Sets + Dictionary

```python
batch1 = {"Aman", "Ravi", "Neha", "Simran", "Karan"}

batch2 = {"Neha", "Karan", "Pooja", "Raj", "Simran"}

marks = {
    "Aman": 75,
    "Ravi": 82,
    "Neha": 90,
    "Simran": 88,
    "Karan": 65,
    "Pooja": 79,
    "Raj": 72
}

# 1. Students present in both batches
both_batches = batch1 & batch2

print("Students in both batches:", both_batches)


# 2. Students only in Batch 1
batch1_only = batch1 - batch2

print("Students only in Batch 1:", batch1_only)


# 3. Students only in Batch 2
batch2_only = batch2 - batch1

print("Students only in Batch 2:", batch2_only)


# 4. Marks of students present in both batches
print("\nMarks of students in both batches:")

for student in both_batches:
    print(student, ":", marks[student])


# 5. Highest-scoring student among both batches
highest_student = max(both_batches, key=marks.get)

print("\nHighest-scoring student:")
print(highest_student, ":", marks[highest_student])
```

### Expected Results

Students in both batches:

```text
{"Neha", "Simran", "Karan"}
```

Students only in Batch 1:

```text
{"Aman", "Ravi"}
```

Students only in Batch 2:

```text
{"Pooja", "Raj"}
```

Marks of students in both batches:

```text
Neha : 90
Simran : 88
Karan : 65
```

Highest-scoring student:

```text
Neha : 90
```

### ⭐ Key Concept

The most important part of this question is combining a **set** with a **dictionary**:

```python
both_batches = batch1 & batch2

for student in both_batches:
    print(student, marks[student])
```

The set determines **which students** we want, while the dictionary gives us **their marks**.
