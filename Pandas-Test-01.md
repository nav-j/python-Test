Sure. Here is a **50-mark Pandas Practical Test with exactly 5 questions**, covering all the topics you listed.

# 🐼 Pandas Practical Test

**Total Marks: 50**
**Time: 90 Minutes**
**Level: Intermediate**

### Topics Covered

* Pandas Series
* Reading CSV files
* Data analysis
* Cleaning empty cells
* Cleaning wrong formats
* Cleaning wrong data
* Removing duplicates
* Correlation
* Data visualization / plotting

---

## Q1. Pandas Series — 10 Marks

Create the following Pandas Series:

```python
marks = [85, 72, 90, 65, 78, 95, 88]
```

Perform the following tasks:

**a)** Create a Pandas Series named `marks`. **(2 marks)**

**b)** Display the Series and its index. **(2 marks)**

**c)** Find the maximum, minimum, and average marks. **(3 marks)**

**d)** Display students/values having marks greater than 80. **(2 marks)**

**e)** Change the index of the Series to:

```text
A, B, C, D, E, F, G
```

**(1 mark)**

---

# Q2. Reading CSV and Analyzing Data — 10 Marks

Create a file named **`employees.csv`** with the following data:

```csv
Name,Age,Department,Salary,Experience
Aman,25,IT,45000,2
Simran,28,HR,52000,4
Raj,24,IT,40000,1
Neha,30,Finance,65000,6
Karan,27,HR,48000,3
Priya,32,IT,72000,8
Ravi,29,Finance,58000,5
```

Read the CSV file using Pandas and perform the following:

**a)** Display the complete DataFrame. **(2 marks)**

**b)** Display the first 5 rows and last 3 rows. **(2 marks)**

**c)** Display the shape, column names, and data types. **(2 marks)**

**d)** Find the average salary and maximum salary. **(2 marks)**

**e)** Display employees having salary greater than `50000`. **(2 marks)**

---

# Q3. Data Cleaning — 10 Marks

Create the following DataFrame:

```python
data = {
    "Name": ["Aman", "Simran", "Raj", "Neha", "Karan", "Priya"],
    "Age": [25, None, 24, 30, None, 32],
    "Salary": [45000, 52000, None, 65000, 48000, None],
    "Joining_Date": [
        "2024-01-15",
        "2024-02-20",
        "March 10, 2024",
        "2024-04-05",
        "2024/05/12",
        "2024-06-18"
    ]
}

df = pd.DataFrame(data)
```

Perform the following:

**a)** Identify the empty/missing cells. **(2 marks)**

**b)** Replace missing `Age` values with the average age. **(2 marks)**

**c)** Replace missing `Salary` values with the average salary. **(2 marks)**

**d)** Convert `Joining_Date` into proper Pandas datetime format. **(2 marks)**

**e)** Display the cleaned DataFrame. **(2 marks)**

---

# Q4. Wrong Data and Duplicate Data — 10 Marks

Consider the following DataFrame:

```python
data = {
    "Name": ["Aman", "Simran", "Raj", "Neha", "Karan", "Raj"],
    "Age": [25, 28, 24, 130, 27, 24],
    "Salary": [45000, 52000, 40000, 65000, -5000, 40000],
    "Department": ["IT", "HR", "IT", "Finance", "HR", "IT"]
}

df = pd.DataFrame(data)
```

Perform the following cleaning operations:

**a)** Identify the duplicate rows. **(2 marks)**

**b)** Remove the duplicate rows. **(2 marks)**

**c)** Identify the wrong age value. Assume that an employee's age cannot be greater than 60. Replace the wrong age with the average valid age. **(3 marks)**

**d)** Identify the wrong salary value. Assume salary cannot be negative. Replace the negative salary with the average valid salary. **(3 marks)**

---

# Q5. Correlation and Pandas Plotting — 10 Marks

Use the following DataFrame:

```python
data = {
    "Hours_Studied": [2, 3, 4, 5, 6, 7, 8, 9],
    "Attendance": [60, 65, 70, 72, 78, 82, 88, 92],
    "Marks": [45, 50, 55, 62, 68, 75, 82, 90]
}

df = pd.DataFrame(data)
```

Perform the following:

**a)** Calculate the correlation between `Hours_Studied` and `Marks`. **(2 marks)**

**b)** Calculate the complete correlation matrix. **(2 marks)**

**c)** Create a **line plot** showing `Hours_Studied` vs `Marks`. **(2 marks)**

**d)** Create a **scatter plot** showing `Attendance` vs `Marks`. **(2 marks)**

**e)** Write one or two sentences explaining the relationship between study hours, attendance, and marks based on the correlation values. **(2 marks)**

genui{"learning_viz":{"type_id":"CORRELATION","locale_override":"en-US"}}

---

# 📊 Marks Distribution

| Q.No.     | Practical Topic            |  Marks |
| --------- | -------------------------- | -----: |
| **Q1**    | Pandas Series              |     10 |
| **Q2**    | CSV + Data Analysis        |     10 |
| **Q3**    | Empty Cells + Wrong Format |     10 |
| **Q4**    | Wrong Data + Duplicates    |     10 |
| **Q5**    | Correlation + Plotting     |     10 |
| **Total** |                            | **50** |

### Skills tested

**Series → CSV → DataFrame → Analysis → Missing values → `fillna()` → Datetime conversion → Wrong data → Duplicates → `drop_duplicates()` → Correlation → Line plot → Scatter plot**
