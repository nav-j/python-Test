Sure. Below is the **complete solution** for the intermediate-level Python test.

# 🐍 Python Test – Complete Solutions

## Q1. MCQs

1. **B. `4`**

```python
x = 10
y = 3
print(x // y + x % y)
```

`10 // 3 = 3` and `10 % 3 = 1`

Therefore:

```text
3 + 1 = 4
```

2. **B. `False`**

3. **C. Skips the current iteration**

4. **B. `20`**

5. **D. `break`**

---

# Q2. Theory Answers

### 1. `break` vs `continue`

* `break` completely terminates the loop.
* `continue` skips the current iteration and moves to the next iteration.

### 2. Parameter vs Argument

A **parameter** is a variable defined in a function:

```python
def add(a, b):
```

Here `a` and `b` are parameters.

An **argument** is the actual value passed to the function:

```python
add(5, 10)
```

Here `5` and `10` are arguments.

### 3. Purpose of `return`

`return` sends a value back from a function.

```python
def add(a, b):
    return a + b
```

### 4. Nested loop

A loop inside another loop is called a **nested loop**.

```python
for i in range(3):
    for j in range(3):
        print(i, j)
```

### 5. `=` vs `==`

`=` is the **assignment operator**:

```python
x = 10
```

`==` is the **comparison operator**:

```python
x == 10
```

---

# Q3. Number Analyzer

```python
num = int(input("Enter number: "))

original = num
digit_count = 0
digit_sum = 0
even_count = 0
odd_count = 0

while num > 0:
    digit = num % 10

    digit_count += 1
    digit_sum += digit

    if digit % 2 == 0:
        even_count += 1
    else:
        odd_count += 1

    num = num // 10

print("Number of digits:", digit_count)
print("Sum of digits:", digit_sum)
print("Even digits:", even_count)
print("Odd digits:", odd_count)

if original % 5 == 0:
    print("Divisible by 5: Yes")
else:
    print("Divisible by 5: No")
```

### Example

```text
Enter number: 25481
Number of digits: 5
Sum of digits: 20
Even digits: 3
Odd digits: 2
Divisible by 5: No
```

---

# Q4. Electricity Bill Calculator

```python
def calculate_bill(units):

    if units <= 100:
        bill = units * 5

    elif units <= 200:
        bill = (100 * 5) + ((units - 100) * 7)

    elif units <= 300:
        bill = (100 * 5) + (100 * 7) + ((units - 200) * 10)

    else:
        bill = (100 * 5) + (100 * 7) + (100 * 10) + ((units - 300) * 15)

    if bill > 2000:
        bill = bill + (bill * 0.05)

    return bill


units = int(input("Enter electricity units: "))

if units < 0:
    print("Invalid units")
else:
    bill = calculate_bill(units)
    print("Electricity Bill = ₹", bill)
```

### Example

For:

```text
250 units
```

Calculation:

```text
100 × 5 = 500
100 × 7 = 700
50 × 10 = 500

Total = ₹1700
```

So:

```text
Electricity Bill = ₹1700
```

---

# Q5. Multiplication Table Challenge

```python
num = int(input("Enter number: "))
start = int(input("Enter starting value: "))
end = int(input("Enter ending value: "))

total = 0

for i in range(start, end + 1):

    if i % 3 == 0:
        continue

    result = num * i

    print(num, "x", i, "=", result)

    total += result

print("Sum =", total)
```

### Example

Input:

```text
Enter number: 5
Enter starting value: 1
Enter ending value: 10
```

Output:

```text
5 x 1 = 5
5 x 2 = 10
5 x 4 = 20
5 x 5 = 25
5 x 7 = 35
5 x 8 = 40
5 x 10 = 50
Sum = 185
```

Notice that `3`, `6`, and `9` are skipped because they are divisible by 3.

---

# Q6. Menu-Driven Calculator

```python
def calculator(a, b, choice):

    if choice == 1:
        return a + b

    elif choice == 2:
        return a - b

    elif choice == 3:
        return a * b

    elif choice == 4:
        if b == 0:
            return "Cannot divide by zero"
        return a / b

    elif choice == 5:
        if b == 0:
            return "Cannot calculate modulus with zero"
        return a % b

    else:
        return "Invalid choice"


while True:

    print("\n===== CALCULATOR =====")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")
    print("5. Modulus")
    print("6. Exit")

    choice = int(input("Enter your choice: "))

    if choice == 6:
        print("Calculator closed.")
        break

    if choice < 1 or choice > 5:
        print("Invalid choice!")
        continue

    a = float(input("Enter first number: "))
    b = float(input("Enter second number: "))

    result = calculator(a, b, choice)

    print("Result:", result)
```

### Example

```text
===== CALCULATOR =====
1. Addition
2. Subtraction
3. Multiplication
4. Division
5. Modulus
6. Exit

Enter your choice: 3
Enter first number: 10
Enter second number: 5
Result: 50
```

---

# Q7. Student Performance System

```python
def student_result(name, marks):

    total = sum(marks)
    percentage = total / len(marks)

    highest = max(marks)
    lowest = min(marks)

    print("\n===== STUDENT RESULT =====")
    print("Name:", name)
    print("Total:", total)
    print("Percentage:", percentage)
    print("Highest:", highest)
    print("Lowest:", lowest)

    # Check whether any subject has marks below 33
    if any(mark < 33 for mark in marks):
        print("Result: Fail")
        return

    if percentage >= 90:
        performance = "Excellent"

    elif percentage >= 75:
        performance = "Very Good"

    elif percentage >= 60:
        performance = "Good"

    elif percentage >= 50:
        performance = "Average"

    else:
        performance = "Needs Improvement"

    print("Result:", performance)


name = input("Enter student name: ")

marks = []

for i in range(5):

    mark = float(input(f"Enter marks for subject {i + 1}: "))

    if mark < 0 or mark > 100:
        print("Invalid marks!")
        break

    marks.append(mark)

else:
    student_result(name, marks)
```

### Example

```text
Enter student name: Riya

Enter marks for subject 1: 85
Enter marks for subject 2: 78
Enter marks for subject 3: 92
Enter marks for subject 4: 74
Enter marks for subject 5: 88

===== STUDENT RESULT =====
Name: Riya
Total: 417
Percentage: 83.4
Highest: 92
Lowest: 74
Result: Very Good
```

### Important concepts used in Q7

```python
sum(marks)
```

Calculates the total.

```python
max(marks)
```

Finds the highest mark.

```python
min(marks)
```

Finds the lowest mark.

```python
any(mark < 33 for mark in marks)
```

Checks whether **at least one subject** has marks below 33.

The `for-else` structure also provides an additional intermediate-level concept:

```python
for i in range(5):
    ...
else:
    student_result(name, marks)
```

The `else` executes only when the `for` loop finishes normally without encountering `break`.
