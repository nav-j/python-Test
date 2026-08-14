# Python Test — Solutions

## Section A — Theory Solutions

### Q1.

A variable is a name used to store a value in Python.

```python
name = "Rahul"
age = 18
```

### Q2.

| Value      | Data Type |
| ---------- | --------- |
| `25`       | `int`     |
| `25.5`     | `float`   |
| `"Python"` | `str`     |
| `True`     | `bool`    |

### Q3.

Comments are used to explain code. Python ignores comments while executing the program.

```python
# This is a comment
name = "Rahul"  # Storing student's name
```

### Q4.

`int` stores whole numbers, while `float` stores decimal numbers.

```python
age = 20        # int
percentage = 85.5   # float
```

### Q5.

```python
text = "Python"

print(text[0])
print(text[-1])
print(text[1:4])
```

**Output:**

```text
P
n
yth
```

### Q6.

* `strip()` removes spaces from the beginning and end.
* `split()` converts a string into a list.
* `join()` combines list/string elements into one string.

Example:

```python
text = "  Python is easy  "

cleaned = text.strip()
words = cleaned.split()
result = "-".join(words)

print(cleaned)
print(words)
print(result)
```

**Output:**

```text
Python is easy
['Python', 'is', 'easy']
Python-is-easy
```

### Q7.

```python
name = "Python Programming"

print(len(name))
print(name.upper())
print(name.lower())
```

**Output:**

```text
18
PYTHON PROGRAMMING
python programming
```

### Q8.

`count()` returns how many times a particular character or substring occurs.

```python
text = "banana"
print(text.count("a"))
```

**Output:**

```text
3
```

### Q9.

String slicing is used to extract a part of a string.

```python
word = "Programming"

print(word[:5])
print(word[-3:])
```

**Output:**

```text
Progr
ing
```

### Q10.

```python
marks = 80
bonus = 5

total = marks + bonus
print(total)
print(type(total))
```

**Output:**

```text
85
<class 'int'>
```

---

# Section B — Practical Solutions

### Q11.

```python
name = "Aman"
age = 18
percentage = 87.5
is_present = True

print(name, type(name))
print(age, type(age))
print(percentage, type(percentage))
print(is_present, type(is_present))
```

**Output:**

```text
Aman <class 'str'>
18 <class 'int'>
87.5 <class 'float'>
True <class 'bool'>
```

---

### Q12.

```python
num1 = 20
num2 = 6

print("Sum:", num1 + num2)
print("Difference:", num1 - num2)
print("Product:", num1 * num2)
print("Division:", num1 / num2)
print("Remainder:", num1 % num2)
```

**Output:**

```text
Sum: 26
Difference: 14
Product: 120
Division: 3.3333333333333335
Remainder: 2
```

---

### Q13.

```python
message = "   Python Programming is Easy   "

cleaned = message.strip()

print(cleaned)
print(cleaned.upper())
print(cleaned.lower())
print(len(cleaned))
```

**Output:**

```text
Python Programming is Easy
PYTHON PROGRAMMING IS EASY
python programming is easy
27
```

---

### Q14.

```python
word = "COMPUTER"

print(word[0])
print(word[-1])
print(word[:3])
print(word[3:6])
print(word[-2:])
```

**Output:**

```text
C
R
COM
PUT
ER
```

---

### Q15.

```python
sentence = "Python is easy and Python is powerful"

print("Python:", sentence.count("Python"))
print("is:", sentence.count("is"))
print("Length:", len(sentence))
print(sentence.lower())
```

**Output:**

```text
Python: 2
is: 2
Length: 40
python is easy and python is powerful
```

---

### Q16.

```python
sentence = "Python is a programming language"

words = sentence.split()

print(words)

result = "-".join(words)

print(result)
```

**Output:**

```text
['Python', 'is', 'a', 'programming', 'language']
Python-is-a-programming-language
```

---

### Q17.

```python
name = "   Rahul Kumar   "
course = "Python Programming"

name = name.strip()

print("Name:", name)

space = name.index(" ")

print("First Name:", name[:space])
print("Last Name:", name[space + 1:])

print("First 6 characters:", course[:6])
print("Last 11 characters:", course[-11:])
```

**Output:**

```text
Name: Rahul Kumar
First Name: Rahul
Last Name: Kumar
First 6 characters: Python
Last 11 characters: Programming
```

---

### Q18.

```python
student = "  Aman Sharma  "
marks = 85
subject = "Python"

student = student.strip()

print("Student:", student)
print("Subject:", subject.upper())
print("Marks:", marks)
print("Name Length:", len(student))
```

**Output:**

```text
Student: Aman Sharma
Subject: PYTHON
Marks: 85
Name Length: 11
```

---

### Q19.

```python
text = "apple,banana,mango,apple,orange"

fruits = text.split(",")

print(fruits)
print("Apple count:", fruits.count("apple"))

result = " | ".join(fruits)

print(result)
```

**Output:**

```text
['apple', 'banana', 'mango', 'apple', 'orange']
Apple count: 2
apple | banana | mango | apple | orange
```

---

# Q20. Student Information Program

```python
# Student information
name = "   Neha Singh   "
age = 18
course = "Python Programming"
skills = "Python,HTML,CSS"
marks = 92

# Remove extra spaces
clean_name = name.strip()

# Convert skills into a list
skill_list = skills.split(",")

# Join skills using |
skills_result = " | ".join(skill_list)

# Display information
print("Student Name:", clean_name)
print("Age:", age)
print("Course:", course.upper())
print("Course Length:", len(course))
print("First 6 Characters:", course[:6])
print("Number of Skills:", len(skill_list))
print("Skills:", skills_result)
print("Python Count:", skills.count("Python"))
```

**Output:**

```text
Student Name: Neha Singh
Age: 18
Course: PYTHON PROGRAMMING
Course Length: 18
First 6 Characters: Python
Number of Skills: 3
Skills: Python | HTML | CSS
Python Count: 1
```

**Note:** In Q20, `skills.count("Python")` counts `"Python"` only inside the `skills` string. This keeps the question focused on the `count()` function.
