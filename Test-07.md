Sure. Here is a **beginner-level Python test focused specifically on Dates, Regex, and Try-Except**, with a few basic Python concepts included.

# PYTHON BEGINNER TEST

## Topics: Dates, Regex & Try-Except

**Duration:** 1 Hour
**Total Marks:** 40
**Level:** Beginner

---

## Section A — Basic Theory

### 8 Marks

**Answer all questions. Each question carries 1 mark.**

### Q1.

Which module is used to work with dates and times in Python?

### Q2.

What is the purpose of the `datetime.now()` function?

### Q3.

Which Python module is used for Regular Expressions?

### Q4.

What does `\d` represent in Regex?

### Q5.

What is the purpose of `re.findall()`?

### Q6.

What is the purpose of `try-except`?

### Q7.

Which error occurs when we try to divide a number by zero?

### Q8.

Which error generally occurs when `int("hello")` is executed?

---

# Section B — Python Dates

## 12 Marks

### Q9. Display Current Date — 3 Marks

Write a Python program to display today's date.

**Expected output:**

```text
Today's date: 2026-10-08
```

---

### Q10. Display Current Date and Time — 3 Marks

Write a program to display the current date and current time.

**Expected output:**

```text
Date: 2026-10-08
Time: 15:30:25
```

---

### Q11. Extract Date Information — 3 Marks

Write a program to display:

* Current year
* Current month
* Current day

**Expected output:**

```text
Year: 2026
Month: 10
Day: 8
```

---

### Q12. Calculate Age — 3 Marks

Ask the user to enter their birth year and calculate their approximate age.

**Example:**

```text
Enter your birth year: 2000
Your age is approximately 26 years.
```

**Hint:**

```python
from datetime import datetime
```

---

# Section C — Regular Expressions

## 12 Marks

Use Python's `re` module.

### Q13. Find Numbers — 3 Marks

Write a program to find all numbers from this string:

```python
text = "I bought 5 apples, 10 bananas and 15 oranges."
```

**Expected output:**

```text
['5', '10', '15']
```

---

### Q14. Check Mobile Number — 3 Marks

Write a program using Regex to check whether a mobile number contains exactly **10 digits**.

**Example 1:**

```text
Enter mobile number: 9876543210
Valid mobile number
```

**Example 2:**

```text
Enter mobile number: 98765
Invalid mobile number
```

**Hint:**

```text
^\d{10}$
```

---

### Q15. Check Email — 3 Marks

Write a program to check whether an email address has a basic valid format.

**Example:**

```text
Enter email: student@gmail.com
Valid Email
```

```text
Enter email: student@gmail
Invalid Email
```

You may use a pattern similar to:

```text
^[\w.-]+@[\w.-]+\.\w+$
```

---

### Q16. Find Words Starting With "P" — 3 Marks

Given:

```python
text = "Python is a popular programming language."
```

Use Regex to find words starting with the letter `P`.

**Expected output:**

```text
['Python', 'popular', 'programming']
```

**Hint:**

```python
re.findall()
```

---

# Section D — Try-Except

## 8 Marks

### Q17. Handle Invalid Number — 2 Marks

Write a program that asks the user to enter a number.

If the user enters a non-numeric value, handle the error using `try-except`.

**Example:**

```text
Enter a number: abc
Invalid input! Please enter a number.
```

---

### Q18. Handle Division by Zero — 3 Marks

Write a program that takes two numbers and divides the first number by the second.

Use `try-except` to handle division by zero.

**Example:**

```text
Enter first number: 20
Enter second number: 0

Error: Cannot divide by zero.
```

---

### Q19. Handle Multiple Errors — 3 Marks

Write a program that:

1. Takes two numbers from the user.
2. Divides the first number by the second.
3. Handles:

   * Invalid number input
   * Division by zero

**Example:**

```text
Enter first number: 10
Enter second number: abc

Invalid input! Please enter numbers only.
```

---

# Section E — Mini Practical

## Bonus: 5 Marks

### Q20. Student Information Program

Create a program that asks the user for:

```text
Name
Birth Year
Mobile Number
Email
```

The program should:

1. Calculate the user's approximate age.
2. Validate the mobile number using Regex.
3. Validate the email using Regex.
4. Display today's date.
5. Use `try-except` to handle an invalid birth year.

**Expected output:**

```text
Enter your name: Aman
Enter your birth year: 2000
Enter mobile number: 9876543210
Enter email: aman@gmail.com

----- Student Information -----

Name: Aman
Age: 26
Mobile: Valid
Email: Valid
Today's Date: 2026-10-08
```

---

## Marks Distribution

| Section   | Topic          |            Marks |
| --------- | -------------- | ---------------: |
| A         | Theory         |                8 |
| B         | Python Dates   |               12 |
| C         | Regex          |               12 |
| D         | Try-Except     |                8 |
| E         | Mini Practical |          5 Bonus |
| **Total** |                | **40 + 5 Bonus** |

### Required Modules

Students may use:

```python
from datetime import datetime
import re
```

**Main focus:** understanding `datetime`, basic Regular Expressions, `try-except`, user input, conditions, and simple Python logic.
