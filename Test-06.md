Sure. Here is a **slightly advanced Python test** that requires students to combine concepts rather than solve each topic separately.

# 🐍 Python Programming Test – Intermediate Level

**Topics:** Operators, `if-elif-else`, Loops, Functions
**Total Marks:** 50
**Time:** 2 Hours

---

## Section A – Theory

### 10 Marks

### Q1. MCQs

**5 × 1 = 5**

**1. What is the output?**

```python
x = 10
y = 3
print(x // y + x % y)
```

A. `3`
B. `4`
C. `5`
D. `6`

---

**2. What will this return?**

```python
5 > 3 and 10 < 5
```

A. `True`
B. `False`
C. `10`
D. Error

---

**3. What does `continue` do inside a loop?**

A. Stops the program
B. Stops the loop permanently
C. Skips the current iteration
D. Restarts the loop

---

**4. What is the output?**

```python
def calculate(a, b=5):
    return a * b

print(calculate(4))
```

A. `9`
B. `20`
C. `4`
D. Error

---

**5. Which statement is used to immediately stop a loop?**

A. `skip`
B. `continue`
C. `stop`
D. `break`

---

### Q2. Short Answer Questions

**5 × 1 = 5**

1. What is the difference between `break` and `continue`?
2. What is the difference between a parameter and an argument?
3. Why do we use `return` in a function?
4. What is a nested loop?
5. What is the difference between `=` and `==`?

---

# Section B – Practical

### 40 Marks

## Q3. Number Analyzer

### 8 Marks

Write a program that takes a positive integer from the user and determines:

* Number of digits
* Sum of digits
* Number of even digits
* Number of odd digits
* Whether the number is divisible by 5

**Example:**

```text
Enter number: 25481

Number of digits: 5
Sum of digits: 20
Even digits: 3
Odd digits: 2
Divisible by 5: No
```

**Requirement:** Use a loop. Do not convert the number into a string.

---

## Q4. Electricity Bill Calculator

### 8 Marks

Create a function:

```python
calculate_bill(units)
```

Calculate the electricity bill according to:

| Units     |     Rate |
| --------- | -------: |
| 0–100     |  ₹5/unit |
| 101–200   |  ₹7/unit |
| 201–300   | ₹10/unit |
| Above 300 | ₹15/unit |

For example:

```text
Enter units: 250
Electricity Bill = ₹1850
```

Also add a **5% surcharge** if the calculated bill is greater than ₹2000.

Use a function and conditional statements.

---

## Q5. Multiplication Table Challenge

### 8 Marks

Write a program that:

1. Takes a number from the user.
2. Takes a starting value and ending value.
3. Prints the multiplication table within that range.
4. Does **not print multiples that are divisible by 3**.
5. Calculates and displays the sum of the printed results.

**Example:**

```text
Enter number: 5
Enter starting value: 1
Enter ending value: 10

5 x 1 = 5
5 x 2 = 10
5 x 4 = 20
5 x 5 = 25
5 x 7 = 35
5 x 8 = 40
5 x 10 = 50

Sum = 185
```

Use:

* `for` loop
* `continue`
* Operators

---

## Q6. Menu-Driven Calculator

### 8 Marks

Create a function:

```python
calculator(a, b, choice)
```

Display the following menu repeatedly:

```text
===== CALCULATOR =====
1. Addition
2. Subtraction
3. Multiplication
4. Division
5. Modulus
6. Exit
```

The program should:

* Take the user's choice.
* Take two numbers.
* Perform the selected operation.
* Handle division by zero.
* Continue displaying the menu until the user selects **6**.

**Requirement:** Use a function, loop, `if-elif-else`, and operators.

---

## Q7. Student Performance System

### 8 Marks

Create a function:

```python
student_result(name, marks)
```

The program should:

1. Ask the user for the student's name.
2. Ask for marks in **5 subjects** using a loop.
3. Calculate:

   * Total marks
   * Percentage
   * Highest marks
   * Lowest marks
4. Determine the result:

| Percentage | Result            |
| ---------- | ----------------- |
| 90+        | Excellent         |
| 75–89      | Very Good         |
| 60–74      | Good              |
| 50–59      | Average           |
| Below 50   | Needs Improvement |

5. If marks in **any subject are below 33**, display:

```text
Result: Fail
```

Otherwise display the performance category.

**Example:**

```text
Enter student name: Riya

Enter marks for subject 1: 85
Enter marks for subject 2: 78
Enter marks for subject 3: 92
Enter marks for subject 4: 74
Enter marks for subject 5: 88

Total = 417
Percentage = 83.4%
Highest = 92
Lowest = 74
Result = Very Good
```

### Requirements

Students must use:

* Function
* `for` loop
* `if-elif-else`
* Comparison operators
* Arithmetic operators
* User input

---

# 📊 Final Marks Distribution

| Question  | Topic                        |  Marks |
| --------- | ---------------------------- | -----: |
| Q1        | MCQs                         |      5 |
| Q2        | Theory                       |      5 |
| Q3        | Loop + Operators             |      8 |
| Q4        | Function + If-Else           |      8 |
| Q5        | Loop + Continue + Operators  |      8 |
| Q6        | Function + Loop + Conditions |      8 |
| Q7        | **Mixed Advanced Problem**   |      8 |
| **Total** |                              | **50** |

This version is more suitable for an **intermediate Python practical test** because students have to combine multiple concepts in the same problem rather than writing isolated programs.
