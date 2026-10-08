Below is the **complete solution** for the 40-mark beginner Python test, including the **bonus question**.

# PYTHON BEGINNER TEST — SOLUTIONS

## Section A — Basic Theory

### Q1. Which module is used to work with dates and times?

**Answer:**

```python
datetime
```

It can be imported using:

```python
from datetime import datetime
```

---

### Q2. What is the purpose of `datetime.now()`?

It returns the **current date and current time**.

Example:

```python
from datetime import datetime

print(datetime.now())
```

---

### Q3. Which Python module is used for Regular Expressions?

**Answer:**

```python
re
```

Import it using:

```python
import re
```

---

### Q4. What does `\d` represent in Regex?

`\d` represents **any digit from 0 to 9**.

Example:

```text
\d
```

matches:

```text
0 1 2 3 4 5 6 7 8 9
```

---

### Q5. What is the purpose of `re.findall()`?

`re.findall()` finds **all occurrences** that match a particular pattern and returns them as a list.

Example:

```python
import re

text = "I have 10 apples and 20 bananas."

result = re.findall(r"\d+", text)

print(result)
```

Output:

```text
['10', '20']
```

---

### Q6. What is the purpose of `try-except`?

`try-except` is used for **handling errors/exceptions** so that the program does not stop unexpectedly.

Example:

```python
try:
    x = int(input("Enter number: "))
except ValueError:
    print("Invalid input")
```

---

### Q7. Which error occurs when dividing by zero?

**Answer:**

```text
ZeroDivisionError
```

---

### Q8. Which error occurs when `int("hello")` is executed?

**Answer:**

```text
ValueError
```

---

# Section B — Python Dates

## Q9. Display Current Date

```python
from datetime import datetime

today = datetime.now()

print("Today's date:", today.strftime("%Y-%m-%d"))
```

**Example output:**

```text
Today's date: 2026-10-08
```

### Explanation

* `%Y` → Year
* `%m` → Month
* `%d` → Day

---

# Q10. Display Current Date and Time

```python
from datetime import datetime

now = datetime.now()

print("Date:", now.strftime("%Y-%m-%d"))
print("Time:", now.strftime("%H:%M:%S"))
```

**Example output:**

```text
Date: 2026-10-08
Time: 15:30:25
```

---

# Q11. Extract Date Information

```python
from datetime import datetime

today = datetime.now()

print("Year:", today.year)
print("Month:", today.month)
print("Day:", today.day)
```

**Example output:**

```text
Year: 2026
Month: 10
Day: 8
```

---

# Q12. Calculate Age

```python
from datetime import datetime

birth_year = int(input("Enter your birth year: "))

current_year = datetime.now().year

age = current_year - birth_year

print("Your age is approximately", age, "years.")
```

**Example:**

```text
Enter your birth year: 2000
Your age is approximately 26 years.
```

### Better version using `try-except`

```python
from datetime import datetime

try:
    birth_year = int(input("Enter your birth year: "))

    current_year = datetime.now().year
    age = current_year - birth_year

    print("Your age is approximately", age, "years.")

except ValueError:
    print("Please enter a valid year.")
```

---

# Section C — Regular Expressions

## Q13. Find Numbers

```python
import re

text = "I bought 5 apples, 10 bananas and 15 oranges."

result = re.findall(r"\d+", text)

print(result)
```

**Output:**

```text
['5', '10', '15']
```

### Explanation

```text
\d+
```

means one or more digits.

---

# Q14. Check Mobile Number

```python
import re

mobile = input("Enter mobile number: ")

pattern = r"^\d{10}$"

if re.match(pattern, mobile):
    print("Valid mobile number")
else:
    print("Invalid mobile number")
```

### Example 1

```text
Enter mobile number: 9876543210
Valid mobile number
```

### Example 2

```text
Enter mobile number: 98765
Invalid mobile number
```

### Explanation

```text
^
```

means beginning of the string.

```text
\d{10}
```

means exactly 10 digits.

```text
$
```

means end of the string.

---

# Q15. Check Email

```python
import re

email = input("Enter email: ")

pattern = r"^[\w.-]+@[\w.-]+\.\w+$"

if re.match(pattern, email):
    print("Valid Email")
else:
    print("Invalid Email")
```

### Example

```text
Enter email: student@gmail.com
Valid Email
```

Another example:

```text
Enter email: student@gmail
Invalid Email
```

### Explanation

The pattern checks for a basic structure like:

```text
username@domain.extension
```

For example:

```text
student@gmail.com
```

---

# Q16. Find Words Starting With "P"

```python
import re

text = "Python is a popular programming language."

result = re.findall(r"\b[Pp]\w*", text)

print(result)
```

**Output:**

```text
['Python', 'popular', 'programming']
```

### Explanation

```text
\b
```

represents a word boundary.

```text
[Pp]
```

matches uppercase or lowercase `P`.

```text
\w*
```

matches the remaining characters of the word.

---

# Section D — Try-Except

## Q17. Handle Invalid Number

```python
try:
    number = int(input("Enter a number: "))
    print("You entered:", number)

except ValueError:
    print("Invalid input! Please enter a number.")
```

### Example

```text
Enter a number: abc
Invalid input! Please enter a number.
```

---

# Q18. Handle Division by Zero

```python
try:
    num1 = int(input("Enter first number: "))
    num2 = int(input("Enter second number: "))

    result = num1 / num2

    print("Result:", result)

except ZeroDivisionError:
    print("Error: Cannot divide by zero.")
```

### Example

```text
Enter first number: 20
Enter second number: 0
Error: Cannot divide by zero.
```

---

# Q19. Handle Multiple Errors

```python
try:
    num1 = int(input("Enter first number: "))
    num2 = int(input("Enter second number: "))

    result = num1 / num2

    print("Result:", result)

except ValueError:
    print("Invalid input! Please enter numbers only.")

except ZeroDivisionError:
    print("Error: Cannot divide by zero.")
```

### Example 1

```text
Enter first number: 10
Enter second number: abc
Invalid input! Please enter numbers only.
```

### Example 2

```text
Enter first number: 10
Enter second number: 0
Error: Cannot divide by zero.
```

---

# Section E — Bonus Practical

## Q20. Student Information Program

```python
from datetime import datetime
import re

# Name
name = input("Enter your name: ")

# Birth Year
try:
    birth_year = int(input("Enter your birth year: "))

    current_year = datetime.now().year
    age = current_year - birth_year

except ValueError:
    print("Invalid birth year.")
    age = "Unknown"

# Mobile Number
mobile = input("Enter mobile number: ")

mobile_pattern = r"^\d{10}$"

if re.match(mobile_pattern, mobile):
    mobile_status = "Valid"
else:
    mobile_status = "Invalid"

# Email
email = input("Enter email: ")

email_pattern = r"^[\w.-]+@[\w.-]+\.\w+$"

if re.match(email_pattern, email):
    email_status = "Valid"
else:
    email_status = "Invalid"

# Today's date
today = datetime.now().strftime("%Y-%m-%d")

# Display information
print("\n----- Student Information -----")

print("Name:", name)
print("Age:", age)
print("Mobile:", mobile_status)
print("Email:", email_status)
print("Today's Date:", today)
```

### Example Output

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

# Quick Revision

### Date

```python
from datetime import datetime

now = datetime.now()

print(now)
print(now.year)
print(now.month)
print(now.day)
```

### Date Formatting

```python
now.strftime("%Y-%m-%d")
```

### Regex

```python
import re

re.findall()
re.match()
```

### Common Regex Patterns

```text
\d       → digit
\d+      → one or more digits
\d{10}   → exactly 10 digits
\w       → word character
^        → beginning
$        → end
```

### Try-Except

```python
try:
    # code that may produce an error

except ValueError:
    # handle invalid value

except ZeroDivisionError:
    # handle division by zero
```

### Important Errors

| Error               | Example                            |
| ------------------- | ---------------------------------- |
| `ValueError`        | `int("abc")`                       |
| `ZeroDivisionError` | `10 / 0`                           |
| `TypeError`         | `"10" + 5`                         |
| `IndexError`        | Accessing an invalid list index    |
| `KeyError`          | Accessing a missing dictionary key |
