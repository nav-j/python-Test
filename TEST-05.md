Here is the complete **50-mark Python practical test**, with the five mixed questions you selected.

# 🐍 Python Practical Test

**Topics:** Operators, Conditional Statements, Loops, `match-case`
**Total Questions:** 5
**Total Marks:** 50
**Marks per Question:** 10

---

### Q1. Electricity Bill Calculator — 10 Marks

Write a Python program to calculate an electricity bill based on the units consumed.

**Requirements:**

* Take the number of electricity units from the user.
* Calculate the bill according to these slabs:

  * First 100 units → ₹5 per unit
  * Next 100 units → ₹7 per unit
  * Above 200 units → ₹10 per unit
* If the calculated bill is more than ₹2,000, add a **5% surcharge**.
* Display:

  * Units consumed
  * Basic bill
  * Surcharge
  * Final bill
* Display an appropriate message if the user enters negative units.

**Concepts:** `if-elif-else`, arithmetic operators, comparison operators

---

### Q2. Guess the Number Game — 10 Marks

Write a Python program to create a **number guessing game**.

**Requirements:**

* Store a secret number in the program, for example `37`.
* Give the user a maximum of **5 attempts**.
* After each guess:

  * If the guess is greater than the secret number, display **"Too High"**.
  * If the guess is smaller, display **"Too Low"**.
  * If the guess is correct, display **"Correct! You Won"**.
* Stop the loop immediately when the user guesses correctly.
* If the user cannot guess the number within 5 attempts, display **"Game Over"**.

**Concepts:** `for`/`while` loop, `if-elif-else`, comparison operators, `break`

---

### Q3. Traffic Signal Simulator — 10 Marks

Create a Python program using **`match-case`** to simulate a traffic signal.

Display the following menu:

```text
1. Red
2. Yellow
3. Green
```

**Requirements:**

* Ask the user to enter a signal number.
* Use `match-case` to perform the appropriate action:

  * Red → Display `"STOP"` and waiting time **60 seconds**
  * Yellow → Display `"WAIT"` and waiting time **5 seconds**
  * Green → Display `"GO"` and waiting time **30 seconds**
* Use an operator to convert the waiting time into **minutes and remaining seconds**.
* Display **"Invalid Signal"** for an incorrect choice.

**Concepts:** `match-case`, operators, input, conditional logic

---

### Q4. Multiplication Table with Conditions — 10 Marks

Write a Python program that takes a number from the user and prints its multiplication table from **1 to 10** using a loop.

For each result, also display whether the result is **Even or Odd**.

**Example:**

```text
Enter a number: 5

5 × 1 = 5 → Odd
5 × 2 = 10 → Even
5 × 3 = 15 → Odd
5 × 4 = 20 → Even
...
5 × 10 = 50 → Even
```

**Requirements:**

* Use a `while` loop.
* Use the `%` operator to check whether the result is even or odd.
* Display the complete table from 1 to 10.

**Concepts:** `while` loop, `if-else`, arithmetic operators, modulus operator

---

### Q5. Shopping Bill System — 10 Marks

Write a Python program to create a simple **shopping bill system**.

**Requirements:**

* Ask the user how many products they want to purchase.
* Use a loop to enter the **price and quantity** of each product.
* Calculate the cost of each product and the total bill.
* Apply a discount according to the following rules:

| Total Amount    |    Discount |
| --------------- | ----------: |
| ₹5,000 or above |         20% |
| ₹3,000–₹4,999   |         15% |
| ₹1,000–₹2,999   |         10% |
| Below ₹1,000    | No discount |

* Display:

  * Total amount
  * Discount amount
  * Final payable amount

**Concepts:** loops, `if-elif-else`, arithmetic operators, multiplication, addition, percentage calculation

---

## 📌 Topics Covered

| Topic                  | Questions      |
| ---------------------- | -------------- |
| Arithmetic Operators   | Q1, Q3, Q4, Q5 |
| Comparison Operators   | Q1, Q2         |
| Conditional Statements | Q1, Q2, Q4, Q5 |
| `match-case`           | Q3             |
| `for` / `while` Loop   | Q2, Q4, Q5     |
| Modulus `%` Operator   | Q4             |
| `break`                | Q2             |
| User Input             | All Questions  |
