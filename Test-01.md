# Python Test — Variables, Data Types, Comments, Numbers & Strings

**Total Marks: 50**
**Total Questions: 20**
**Theory: 10 Questions × 2 Marks = 20 Marks**
**Practical: 10 Questions × 3 Marks = 30 Marks**

## Section A — Theory Questions

**10 Questions × 2 Marks = 20 Marks**

### Q1. [2 Marks]

What is a variable in Python? Write a Python statement to store your name and age in two different variables.

### Q2. [2 Marks]

Identify the data type of each value:

```python
25
25.5
"Python"
True
```

### Q3. [2 Marks]

What is the purpose of comments in Python? Write one single-line comment and one example of a statement containing a comment.

### Q4. [2 Marks]

What is the difference between an integer and a float? Give one example of each.

### Q5. [2 Marks]

Consider the following string:

```python
text = "Python"
```

What will be the output of:

```python
print(text[0])
print(text[-1])
print(text[1:4])
```

### Q6. [2 Marks]

What is the difference between `strip()`, `split()` and `join()`? Explain with a simple example.

### Q7. [2 Marks]

What will be the output of the following?

```python
name = "Python Programming"
print(len(name))
print(name.upper())
print(name.lower())
```

### Q8. [2 Marks]

What does the `count()` function do? Find the number of `"a"` characters in:

```python
text = "banana"
```

### Q9. [2 Marks]

What is string slicing? Write code to print the first 5 characters and last 3 characters of:

```python
word = "Programming"
```

### Q10. [2 Marks]

What will be the output of the following?

```python
marks = 80
bonus = 5

total = marks + bonus
print(total)
print(type(total))
```

---

# Section B — Practical Questions

**10 Questions × 3 Marks = 30 Marks**

### Q11. [3 Marks]

Create variables for a student's:

```text
name
age
percentage
is_present
```

Store suitable values and print all four values along with their data types using `type()`.

### Q12. [3 Marks]

Write a Python program using two numeric variables to calculate and display:

* Sum
* Difference
* Product
* Division
* Remainder

### Q13. [3 Marks]

Create:

```python
message = "   Python Programming is Easy   "
```

Write a program that:

* Removes the extra spaces.
* Converts the message to uppercase.
* Converts the message to lowercase.
* Displays the length of the cleaned message.

### Q14. [3 Marks]

Create:

```python
word = "COMPUTER"
```

Using indexing and slicing, print:

```text
C
R
COM
PUT
ER
```

### Q15. [3 Marks]

Create:

```python
sentence = "Python is easy and Python is powerful"
```

Write a program to:

* Count how many times `"Python"` appears.
* Count how many times `"is"` appears.
* Display the total number of characters.
* Convert the sentence to lowercase.

### Q16. [3 Marks]

Create:

```python
sentence = "Python is a programming language"
```

Use `split()` to convert it into a list of words. Then use `join()` to create the following output:

```text
Python-is-a-programming-language
```

### Q17. [3 Marks]

Create:

```python
name = "   Rahul Kumar   "
course = "Python Programming"
```

Write a program that:

* Removes spaces from `name`.
* Prints the first name using slicing/indexing.
* Prints the last name.
* Prints the first 6 characters of `course`.
* Prints the last 11 characters of `course`.

### Q18. [3 Marks]

Create variables:

```python
student = "  Aman Sharma  "
marks = 85
subject = "Python"
```

Write a program that displays a formatted result such as:

```text
Student: Aman Sharma
Subject: PYTHON
Marks: 85
Name Length: ______
```

Use `strip()`, `upper()` and `len()` in your program.

### Q19. [3 Marks]

Create:

```python
text = "apple,banana,mango,apple,orange"
```

Write a program that:

1. Converts the string into a list using `split()`.
2. Counts how many times `"apple"` appears.
3. Joins the list elements using `" | "`.
4. Prints the final joined string.

### Q20. [3 Marks]

Create a small **Student Information Program** using the following variables:

```python
name = "   Neha Singh   "
age = 18
course = "Python Programming"
skills = "Python,HTML,CSS"
marks = 92
```

Using a combination of the topics taught, write a program that displays:

* Cleaned student name
* Student age
* Course in uppercase
* Number of characters in the course
* First 6 characters of the course
* Number of skills
* Skills separated using `|`
* Number of times `"Python"` occurs in the student's information

**You must use comments, variables, appropriate data types, indexing/slicing and suitable string functions in your solution.**

---

## Marks Summary

| Section   | Questions |  Marks |
| --------- | --------: | -----: |
| Theory    |        10 |     20 |
| Practical |        10 |     30 |
| **Total** |    **20** | **50** |

**Topics Covered:** Variables, Data Types, Comments, Numbers, Strings, Indexing, Slicing, `strip()`, `split()`, `join()`, `count()`, `len()`, `upper()`, `lower()`.
