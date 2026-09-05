Below is the **complete solution** for the 50-mark Pandas practical test, with exactly 5 questions.

# 🐼 Pandas Practical Test — Solution

## Q1. Pandas Series — 10 Marks

### Solution

```python
import pandas as pd

marks = [85, 72, 90, 65, 78, 95, 88]

# a) Create Series
s = pd.Series(marks, name="Marks")

print(s)
```

### b) Display Series and its index

```python
print("Series:")
print(s)

print("\nIndex:")
print(s.index)
```

### c) Maximum, minimum, and average

```python
print("Maximum:", s.max())
print("Minimum:", s.min())
print("Average:", s.mean())
```

**Output:**

```text
Maximum: 95
Minimum: 65
Average: 81.85714285714286
```

### d) Values greater than 80

```python
print(s[s > 80])
```

**Output:**

```text
0    85
2    90
5    95
6    88
```

### e) Change the index

```python
s.index = ["A", "B", "C", "D", "E", "F", "G"]

print(s)
```

**Complete solution:**

```python
import pandas as pd

marks = [85, 72, 90, 65, 78, 95, 88]

s = pd.Series(marks, name="Marks")

print("Series:")
print(s)

print("\nIndex:")
print(s.index)

print("\nMaximum:", s.max())
print("Minimum:", s.min())
print("Average:", s.mean())

print("\nMarks greater than 80:")
print(s[s > 80])

s.index = ["A", "B", "C", "D", "E", "F", "G"]

print("\nUpdated Series:")
print(s)
```

---

# Q2. Reading CSV and Analyzing Data — 10 Marks

First create **`employees.csv`**:

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

### a) Read and display CSV

```python
import pandas as pd

df = pd.read_csv("employees.csv")

print(df)
```

### b) First 5 and last 3 rows

```python
print("First 5 rows:")
print(df.head())

print("\nLast 3 rows:")
print(df.tail(3))
```

### c) Shape, columns, and data types

```python
print("Shape:", df.shape)

print("\nColumns:")
print(df.columns)

print("\nData Types:")
print(df.dtypes)
```

### d) Average and maximum salary

```python
print("Average Salary:", df["Salary"].mean())

print("Maximum Salary:", df["Salary"].max())
```

### e) Salary greater than 50,000

```python
result = df[df["Salary"] > 50000]

print(result)
```

### Complete solution

```python
import pandas as pd

df = pd.read_csv("employees.csv")

print("Complete DataFrame:")
print(df)

print("\nFirst 5 rows:")
print(df.head())

print("\nLast 3 rows:")
print(df.tail(3))

print("\nShape:")
print(df.shape)

print("\nColumns:")
print(df.columns)

print("\nData Types:")
print(df.dtypes)

print("\nAverage Salary:")
print(df["Salary"].mean())

print("\nMaximum Salary:")
print(df["Salary"].max())

print("\nEmployees with salary greater than 50000:")
print(df[df["Salary"] > 50000])
```

---

# Q3. Data Cleaning — 10 Marks

### Given DataFrame

```python
import pandas as pd

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

### a) Identify missing values

```python
print(df.isnull())
```

To count missing values:

```python
print(df.isnull().sum())
```

**Output:**

```text
Name            0
Age             2
Salary          2
Joining_Date    0
dtype: int64
```

---

### b) Replace missing Age with average age

```python
df["Age"] = df["Age"].fillna(df["Age"].mean())
```

The average valid age is:

```text
27.8
```

---

### c) Replace missing Salary with average salary

```python
df["Salary"] = df["Salary"].fillna(df["Salary"].mean())
```

The average valid salary is:

```text
52500
```

---

### d) Convert Joining_Date to datetime

```python
df["Joining_Date"] = pd.to_datetime(
    df["Joining_Date"],
    format="mixed"
)
```

`format="mixed"` is useful here because the dates are written in different formats.

---

### e) Display cleaned DataFrame

```python
print(df)
```

### Complete solution

```python
import pandas as pd

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

print("Missing values:")
print(df.isnull().sum())

# Fill missing Age
df["Age"] = df["Age"].fillna(df["Age"].mean())

# Fill missing Salary
df["Salary"] = df["Salary"].fillna(df["Salary"].mean())

# Convert dates
df["Joining_Date"] = pd.to_datetime(
    df["Joining_Date"],
    format="mixed"
)

print("\nCleaned DataFrame:")
print(df)
```

---

# Q4. Wrong Data and Duplicate Data — 10 Marks

### Given DataFrame

```python
import pandas as pd

data = {
    "Name": ["Aman", "Simran", "Raj", "Neha", "Karan", "Raj"],
    "Age": [25, 28, 24, 130, 27, 24],
    "Salary": [45000, 52000, 40000, 65000, -5000, 40000],
    "Department": ["IT", "HR", "IT", "Finance", "HR", "IT"]
}

df = pd.DataFrame(data)
```

### a) Identify duplicate rows

```python
print(df.duplicated())
```

Or display the actual duplicate:

```python
print(df[df.duplicated()])
```

The second `Raj` row is a duplicate.

---

### b) Remove duplicates

```python
df.drop_duplicates(inplace=True)

print(df)
```

---

### c) Identify and correct wrong age

Age `130` is invalid because the question specifies that age cannot be greater than 60.

First identify it:

```python
print(df[df["Age"] > 60])
```

Calculate average of valid ages:

```python
valid_age_average = df.loc[df["Age"] <= 60, "Age"].mean()

print(valid_age_average)
```

Replace the invalid age:

```python
df.loc[df["Age"] > 60, "Age"] = valid_age_average
```

The valid ages are:

```text
25, 28, 24, 27
```

Average:

```text
26
```

So `130` becomes `26`.

---

### d) Identify and correct wrong salary

Find negative salary:

```python
print(df[df["Salary"] < 0])
```

Calculate average of valid salaries:

```python
valid_salary_average = df.loc[df["Salary"] >= 0, "Salary"].mean()

print(valid_salary_average)
```

Replace negative salary:

```python
df.loc[df["Salary"] < 0, "Salary"] = valid_salary_average
```

### Complete solution

```python
import pandas as pd

data = {
    "Name": ["Aman", "Simran", "Raj", "Neha", "Karan", "Raj"],
    "Age": [25, 28, 24, 130, 27, 24],
    "Salary": [45000, 52000, 40000, 65000, -5000, 40000],
    "Department": ["IT", "HR", "IT", "Finance", "HR", "IT"]
}

df = pd.DataFrame(data)

# a) Identify duplicates
print("Duplicate rows:")
print(df[df.duplicated()])

# b) Remove duplicates
df.drop_duplicates(inplace=True)

# c) Correct wrong age
valid_age_average = df.loc[df["Age"] <= 60, "Age"].mean()

df.loc[df["Age"] > 60, "Age"] = valid_age_average

# d) Correct wrong salary
valid_salary_average = df.loc[df["Salary"] >= 0, "Salary"].mean()

df.loc[df["Salary"] < 0, "Salary"] = valid_salary_average

print("\nCleaned DataFrame:")
print(df)
```

---

# Q5. Correlation and Pandas Plotting — 10 Marks

### Given DataFrame

```python
import pandas as pd
import matplotlib.pyplot as plt

data = {
    "Hours_Studied": [2, 3, 4, 5, 6, 7, 8, 9],
    "Attendance": [60, 65, 70, 72, 78, 82, 88, 92],
    "Marks": [45, 50, 55, 62, 68, 75, 82, 90]
}

df = pd.DataFrame(data)
```

---

### a) Correlation between Hours Studied and Marks

```python
correlation = df["Hours_Studied"].corr(df["Marks"])

print("Correlation:", correlation)
```

The value will be very close to **+1**, indicating a strong positive relationship.

---

### b) Complete correlation matrix

```python
print(df.corr())
```

This calculates the correlation between:

* Hours Studied and Attendance
* Hours Studied and Marks
* Attendance and Marks
* Each column with itself

---

### c) Line plot — Hours Studied vs Marks

```python
df.plot(
    x="Hours_Studied",
    y="Marks",
    kind="line",
    marker="o"
)

plt.title("Hours Studied vs Marks")
plt.xlabel("Hours Studied")
plt.ylabel("Marks")
plt.show()
```

---

### d) Scatter plot — Attendance vs Marks

```python
df.plot(
    x="Attendance",
    y="Marks",
    kind="scatter"
)

plt.title("Attendance vs Marks")
plt.xlabel("Attendance")
plt.ylabel("Marks")
plt.show()
```

---

### e) Interpretation

The correlation between **Hours Studied and Marks** is strongly positive. This means that, in this dataset, students who study more hours tend to have higher marks.

Similarly, **Attendance and Marks** have a strong positive correlation, meaning higher attendance is associated with higher marks in this dataset.

> Remember: correlation shows an association; it does not by itself prove that one variable causes the other.

---

## Complete Q5 Solution

```python
import pandas as pd
import matplotlib.pyplot as plt

data = {
    "Hours_Studied": [2, 3, 4, 5, 6, 7, 8, 9],
    "Attendance": [60, 65, 70, 72, 78, 82, 88, 92],
    "Marks": [45, 50, 55, 62, 68, 75, 82, 90]
}

df = pd.DataFrame(data)

# a) Correlation
correlation = df["Hours_Studied"].corr(df["Marks"])

print("Correlation between Hours Studied and Marks:")
print(correlation)

# b) Correlation matrix
print("\nCorrelation Matrix:")
print(df.corr())

# c) Line plot
df.plot(
    x="Hours_Studied",
    y="Marks",
    kind="line",
    marker="o"
)

plt.title("Hours Studied vs Marks")
plt.xlabel("Hours Studied")
plt.ylabel("Marks")
plt.show()

# d) Scatter plot
df.plot(
    x="Attendance",
    y="Marks",
    kind="scatter"
)

plt.title("Attendance vs Marks")
plt.xlabel("Attendance")
plt.ylabel("Marks")
plt.show()
```

---

# ✅ Final Topic Coverage

| Question | Main Concepts                                                            |
| -------- | ------------------------------------------------------------------------ |
| **Q1**   | `Series`, index, `max()`, `min()`, `mean()`, filtering                   |
| **Q2**   | `read_csv()`, `head()`, `tail()`, `shape`, `columns`, `dtypes`, analysis |
| **Q3**   | Missing values, `isnull()`, `fillna()`, datetime/wrong format            |
| **Q4**   | Wrong data, `loc[]`, `drop_duplicates()`, data validation                |
| **Q5**   | `corr()`, correlation matrix, line plot, scatter plot                    |

**Total = 50 Marks**.
