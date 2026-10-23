# Python Practical Test – Intermediate Basics

Total Marks: 40 · Duration: 60 Minutes · Level: Beginner to Intermediate

Instructions:

- Attempt all 8 questions.
- Use functions, loops, conditional statements, strings, lists, dictionaries, and exception handling where appropriate.
- Write complete, executable Python programs.
- Do not use external libraries.

## Practical Questions

## Q1

5 marks

Student Result Management

Input a student's name and marks in five subjects.

- Calculate total marks and percentage.
- Display the grade using these rules: 90% or above = A, 75–89% = B, 60–74% = C, 40–59% = D, below 40% = Fail.
- If the student scores below 33 in any subject, display `Fail` regardless of the percentage.
- Validate that each subject's marks are between 0 and 100.

## Q2

5 marks

Number Analysis

Input a positive integer and perform the following operations:

- Count the number of digits.
- Calculate the sum of its digits.
- Reverse the number.
- Check whether it is a palindrome.
- Count how many digits are even and how many are odd.

Example: Input: `1221` → Reverse: `1221`, Palindrome: Yes.

## Q3

5 marks

List Processing

Given the list:

`numbers = [12, 5, 18, 7, 12, 25, 5, 30, 18, 9]`

- Remove duplicate values without using `set()`.
- Sort the unique values in descending order.
- Find the second-largest unique number.
- Create separate lists of even and odd numbers.
- Calculate the average of the original list.

## Q4

5 marks

String Analysis

Input a sentence and:

- Count the vowels, consonants, digits, and spaces.
- Find the longest word.
- Check whether the sentence is a palindrome after ignoring spaces, punctuation, and letter case.

Example: `Never odd or even` is a palindrome after normalization.

## Q5

5 marks

Dictionary-Based Sales Report

Use the following data:

```
sales = {    "Laptop": 45000,    "Mouse": 800,    "Keyboard": 1500,    "Monitor": 12000,    "Headphones": 2500}
```

- Display each product and its price.
- Find the most expensive product.
- Calculate the total inventory value.
- Increase every product's price by 10% and store the updated prices in a new dictionary.
- Display products priced above ₹5,000 after the increase.

## Q6

5 marks

Function with Multiple Conditions

Create a function `check_number(n)` that:

- Returns `"Invalid"` if the number is zero or negative.
- Returns `"Prime"` if it is a prime number.
- Returns `"Perfect Square"` if it is a perfect square but not prime.
- Otherwise, returns `"Neither"`.

Test the function with at least five different numbers.

## Q7

5 marks

Exception Handling and Input Validation

Create a program that repeatedly asks the user to enter a number until a valid positive integer is entered.

- Handle non-numeric input using `try-except`.
- Reject zero and negative numbers.
- Print the factorial of the accepted number.
- Prevent invalid input from crashing the program.

## Q8

5 marks

Mini ATM Program

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

## Evaluation Scheme

| Criteria                            | Marks |
| ----------------------------------- | ----- |
| Correct logic and approach          | 16    |
| Proper use of Python concepts       | 8     |
| Correct output and edge cases       | 8     |
| Input validation and error handling | 4     |
| Code readability and execution      | 4     |
| Total                               | 40    |

Teacher's note: This version tests problem-solving rather than just basic syntax. It is suitable for students who have completed variables, operators, conditionals, loops, strings, lists, dictionaries, functions, and `try-except`.
