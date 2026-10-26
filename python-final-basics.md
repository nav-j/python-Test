# Python Practical Test – Intermediate Basics

Total Marks: 40 · 

## Practical Questions

### Q1 Student Result Management

Input a student's name and marks in five subjects.

- Calculate total marks and percentage.
- Display the grade using these rules: 90% or above = A, 75–89% = B, 60–74% = C, 40–59% = D, below 40% = Fail.
- If the student scores below 33 in any subject, display `Fail` regardless of the percentage.
  
### Q2 Number Analysis

Input a positive integer and perform the following operations:

- Count the number of digits.
- Calculate the sum of its digits.
- Reverse the number.
- Count how many digits are even and how many are odd.

### Q3 List Processing

Given the list:

`numbers = [12, 5, 18, 7, 12, 25, 5, 30, 18, 9]`

- Sort the unique values in descending order.
- Create separate lists of even and odd numbers.
- Calculate the average of the original list.

### Q4 Dictionary-Based Sales Report

Use the following data:

```
sales = {    "Laptop": 45000,    "Mouse": 800,    "Keyboard": 1500,    "Monitor": 12000,    "Headphones": 2500}
```

- Display each product and its price.
- Find the most expensive product.
- Calculate the total inventory value.
- Increase every product's price by 10% and store the updated prices in a new dictionary.
- Display products priced above ₹5,000 after the increase.

### Q5 Function with Multiple Conditions

Create a function `check_number(n)` that:

- Returns `"Invalid"` if the number is zero or negative.
- Returns `"Prime"` if it is a prime number.
- Returns `"Perfect Square"` if it is a perfect square but not prime.
- Otherwise, returns `"Neither"`.

Test the function with at least five different numbers.


### Q6 Mini ATM Program

Write a menu-driven program with an initial balance of ₹10,000.

1. Check balance.
2. Deposit money.
3. Withdraw money.
4. Exit.

Requirements:

- Use a loop to keep showing the menu until Exit is selected.
- Use conditional statements to process the selected option.
- Reject deposits or withdrawals that are zero or negative.
- Do not allow withdrawals exceeding the available balance.
- Handle invalid menu choices and non-numeric amounts.
