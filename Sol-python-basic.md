# Python Practical Test – Solutions

## Q1. Student Result Management

```
name = input("Enter student name: ")marks = []for i in range(1, 6):    while True:        try:            mark = float(input(f"Enter marks for subject {i}: "))            if 0 <= mark <= 100:                marks.append(mark)                break            else:                print("Marks must be between 0 and 100.")        except ValueError:            print("Please enter valid numeric marks.")total = sum(marks)percentage = total / 5if min(marks) < 33:    grade = "Fail"elif percentage >= 90:    grade = "A"elif percentage >= 75:    grade = "B"elif percentage >= 60:    grade = "C"elif percentage >= 40:    grade = "D"else:    grade = "Fail"print("\n--- Student Result ---")print("Name:", name)print("Total Marks:", total, "/ 500")print("Percentage:", percentage, "%")print("Grade:", grade)
```

Explanation:

- `marks.append(mark)` stores each valid mark in the list.
- `sum(marks)` calculates the total.
- `min(marks) < 33` checks whether any subject mark is below 33.
- `try-except` handles non-numeric input.

## Q2. Number Analysis

```
while True:    try:        num = int(input("Enter a positive integer: "))        if num > 0:            break        else:            print("Enter a number greater than zero.")    except ValueError:        print("Please enter a valid integer.")original = numdigit_count = 0digit_sum = 0reverse = 0even_count = 0odd_count = 0while num > 0:    digit = num % 10    digit_count += 1    digit_sum += digit    reverse = reverse * 10 + digit    if digit % 2 == 0:        even_count += 1    else:        odd_count += 1    num = num // 10print("Original Number:", original)print("Number of Digits:", digit_count)print("Sum of Digits:", digit_sum)print("Reversed Number:", reverse)print("Even Digits:", even_count)print("Odd Digits:", odd_count)
```

Example output for `1234`:

```
Original Number: 1234
Number of Digits: 4
Sum of Digits: 10
Reversed Number: 4321
Even Digits: 2
Odd Digits: 2
```

Explanation:

- `% 10` extracts the last digit.
- `// 10` removes the last digit.
- `reverse * 10 + digit` builds the reversed number.

## Q3. List Processing

```
numbers = [12, 5, 18, 7, 12, 25, 5, 30, 18, 9]# Sort unique values in descending orderunique_numbers = sorted(set(numbers), reverse=True)# Separate even and odd numberseven_numbers = []odd_numbers = []for num in numbers:    if num % 2 == 0:        even_numbers.append(num)    else:        odd_numbers.append(num)# Calculate average of original listaverage = sum(numbers) / len(numbers)print("Original List:", numbers)print("Unique Numbers (Descending):", unique_numbers)print("Even Numbers:", even_numbers)print("Odd Numbers:", odd_numbers)print("Average:", average)
```

Output:

```
Original List: [12, 5, 18, 7, 12, 25, 5, 30, 18, 9]
Unique Numbers (Descending): [30, 25, 18, 12, 9, 7, 5]
Even Numbers: [12, 18, 12, 30, 18]
Odd Numbers: [5, 7, 25, 5, 9]
Average: 14.1
```

Explanation:

- `set(numbers)` removes duplicate values.
- `sorted(..., reverse=True)` sorts values from largest to smallest.
- `% 2 == 0` identifies even numbers.
- `sum(numbers) / len(numbers)` calculates the average.

## Q4. Dictionary-Based Sales Report

```
sales = {    "Laptop": 45000,    "Mouse": 800,    "Keyboard": 1500,    "Monitor": 12000,    "Headphones": 2500}# Display each product and priceprint("--- Product Prices ---")for product, price in sales.items():    print(product, ":", price)# Find the most expensive productexpensive_product = max(sales, key=sales.get)print("\nMost Expensive Product:", expensive_product)print("Price:", sales[expensive_product])# Calculate total inventory valuetotal_value = sum(sales.values())print("Total Inventory Value: ₹", total_value)# Increase prices by 10%updated_sales = {}for product, price in sales.items():    updated_sales[product] = price * 1.10print("\n--- Updated Prices ---")for product, price in updated_sales.items():    print(product, ":", round(price, 2))
```

Expected key results:

```
Most Expensive Product: Laptop
Price: 45000
Total Inventory Value: ₹ 61800

Products Above ₹5,000:
Laptop : 49500.0
Monitor : 13200.0
```

Explanation:

- `.items()` provides both keys and values.
- `max(sales, key=sales.get)` returns the product with the highest price.
- `.values()` provides all prices.
- `updated_sales` stores the increased prices without modifying the original dictionary.

## Q5. Function with Multiple Conditions

```
import mathdef check_number(n):    if n <= 0:        return "Invalid"    # Check whether the number is prime    is_prime = True    if n == 1:        is_prime = False    else:        for i in range(2, math.isqrt(n) + 1):            if n % i == 0:                is_prime = False                break    if is_prime:        return "Prime"    # Check whether the number is a perfect square    root = math.isqrt(n)    if root * root == n:        return "Perfect Square"    return "Neither"# Test with different numberstest_numbers = [0, -5, 7, 16, 12, 1, 25]for num in test_numbers:    print(num, ":", check_number(num))
```

Output:

```
0 : Invalid
-5 : Invalid
7 : Prime
16 : Perfect Square
12 : Neither
1 : Neither
25 : Perfect Square
```

Explanation:

- `math.isqrt(n)` calculates the integer square root.
- A prime number has exactly two positive factors: 1 and itself.
- A perfect square is an integer that can be written as \\(k^2\\), where \\(k\\) is an integer.
- The function checks for prime numbers first, as required.

## Q6. Mini ATM Program

```
balance = 10000while True:    print("\n===== MINI ATM =====")    print("1. Check Balance")    print("2. Deposit Money")    print("3. Withdraw Money")    print("4. Exit")    choice = input("Enter your choice: ")    if choice == "1":        print(f"Current Balance: ₹{balance:.2f}")    elif choice == "2":        try:            amount = float(input("Enter deposit amount: ₹"))            if amount <= 0:                print("Deposit amount must be greater than zero.")            else:                balance += amount                print(f"Deposit successful. New balance: ₹{balance:.2f}")        except ValueError:            print("Invalid amount. Please enter a number.")    elif choice == "3":        try:            amount = float(input("Enter withdrawal amount: ₹"))            if amount <= 0:                print("Withdrawal amount must be greater than zero.")            elif amount > balance:                print("Insufficient balance.")            else:
```

Explanation:

- `while True` keeps the menu running.
- `balance += amount` adds the deposit.
- `balance -= amount` subtracts the withdrawal.
- `try-except` prevents invalid amounts from crashing the program.
- `break` terminates the loop when the user selects Exit.

## Concepts covered in this test

| Question | Main Python concepts                                      |
| -------- | --------------------------------------------------------- |
| Q1       | Lists, loops, conditions, validation                      |
| Q2       | `while` loop, arithmetic operators, digit manipulation    |
| Q3       | Lists, sets, sorting, loops                               |
| Q4       | Dictionaries, `max()`, `sum()`, dictionary iteration      |
| Q5       | Functions, prime numbers, perfect squares, `math` module  |
| Q6       | Loops, conditions, exception handling, updating variables |

Teacher's suggestion: Ask students to explain why their code works after they execute it. This helps assess their understanding of Python logic rather than just their ability to copy a solution.
