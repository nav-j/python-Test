Below are the complete solutions for all **5 questions**. Each solution is written at a beginner-friendly level and uses the concepts specified in the task.

# 🐍 Python Practical Test — Solutions

## Q1. Electricity Bill Calculator

```python
units = float(input("Enter electricity units consumed: "))

if units < 0:
    print("Invalid units. Units cannot be negative.")

else:
    if units <= 100:
        bill = units * 5

    elif units <= 200:
        bill = (100 * 5) + ((units - 100) * 7)

    else:
        bill = (100 * 5) + (100 * 7) + ((units - 200) * 10)

    if bill > 2000:
        surcharge = bill * 5 / 100
    else:
        surcharge = 0

    final_bill = bill + surcharge

    print("\n----- Electricity Bill -----")
    print("Units Consumed:", units)
    print("Basic Bill: ₹", bill)
    print("Surcharge: ₹", surcharge)
    print("Final Bill: ₹", final_bill)
```

### Example Output

```text
Enter electricity units consumed: 250

----- Electricity Bill -----
Units Consumed: 250.0
Basic Bill: ₹ 2200.0
Surcharge: ₹ 110.0
Final Bill: ₹ 2310.0
```

---

# Q2. Guess the Number Game

```python
secret_number = 37

for attempt in range(1, 6):

    guess = int(input("Enter your guess: "))

    if guess == secret_number:
        print("Correct! You Won")
        print("You guessed it in", attempt, "attempt(s).")
        break

    elif guess > secret_number:
        print("Too High")

    else:
        print("Too Low")

else:
    print("Game Over")
    print("The correct number was:", secret_number)
```

### Example Output

```text
Enter your guess: 50
Too High

Enter your guess: 25
Too Low

Enter your guess: 37
Correct! You Won
You guessed it in 3 attempt(s).
```

**Important:** The `else` belonging to the `for` loop runs only when the loop finishes without executing `break`.

---

# Q3. Traffic Signal Simulator

```python
print("----- Traffic Signal -----")
print("1. Red")
print("2. Yellow")
print("3. Green")

choice = int(input("Enter your choice: "))

match choice:

    case 1:
        signal = "STOP"
        seconds = 60

    case 2:
        signal = "WAIT"
        seconds = 5

    case 3:
        signal = "GO"
        seconds = 30

    case _:
        print("Invalid Signal")
        seconds = 0
        signal = ""

if seconds > 0:
    minutes = seconds // 60
    remaining_seconds = seconds % 60

    print("\nSignal:", signal)
    print("Waiting Time:", minutes, "minute(s)", remaining_seconds, "second(s)")
```

### Example Output

```text
----- Traffic Signal -----
1. Red
2. Yellow
3. Green

Enter your choice: 1

Signal: STOP
Waiting Time: 1 minute(s) 0 second(s)
```

### Another Example

```text
Enter your choice: 3

Signal: GO
Waiting Time: 0 minute(s) 30 second(s)
```

Here:

* `//` gives the complete minutes.
* `%` gives the remaining seconds.

---

# Q4. Multiplication Table with Conditions

```python
number = int(input("Enter a number: "))

i = 1

while i <= 10:

    result = number * i

    if result % 2 == 0:
        status = "Even"
    else:
        status = "Odd"

    print(number, "x", i, "=", result, "→", status)

    i = i + 1
```

### Example Output

```text
Enter a number: 5

5 x 1 = 5 → Odd
5 x 2 = 10 → Even
5 x 3 = 15 → Odd
5 x 4 = 20 → Even
5 x 5 = 25 → Odd
5 x 6 = 30 → Even
5 x 7 = 35 → Odd
5 x 8 = 40 → Even
5 x 9 = 45 → Odd
5 x 10 = 50 → Even
```

---

# Q5. Shopping Bill System

```python
number_of_products = int(input("Enter number of products: "))

total = 0

for i in range(1, number_of_products + 1):

    print("\nProduct", i)

    price = float(input("Enter price: ₹"))
    quantity = int(input("Enter quantity: "))

    cost = price * quantity

    total = total + cost

print("\n----- Shopping Bill -----")
print("Total Amount: ₹", total)

if total >= 5000:
    discount = total * 20 / 100

elif total >= 3000:
    discount = total * 15 / 100

elif total >= 1000:
    discount = total * 10 / 100

else:
    discount = 0

final_amount = total - discount

print("Discount: ₹", discount)
print("Final Amount: ₹", final_amount)
```

### Example Output

```text
Enter number of products: 3

Product 1
Enter price: ₹1500
Enter quantity: 2

Product 2
Enter price: ₹800
Enter quantity: 1

Product 3
Enter price: ₹500
Enter quantity: 2

----- Shopping Bill -----
Total Amount: ₹ 5100.0
Discount: ₹ 1020.0
Final Amount: ₹ 4080.0
```

### Concepts Practiced

* `input()`
* Variables
* Arithmetic operators
* Comparison operators
* `if-elif-else`
* `for` loop
* `while` loop
* `match-case`
* `%` modulus
* `//` floor division
* `break`
* Calculations and real-world logic
