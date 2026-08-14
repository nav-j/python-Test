# Solutions — Intermediate NumPy Mixed Practical Task

```python
import numpy as np
```

### 1. Student Marks Array

```python
import numpy as np

marks = np.array([78, 85, 92, 67, 88, 73, 95, 81])

print("Array:", marks)
print("Data type:", marks.dtype)
print("Shape:", marks.shape)

print("2nd student:", marks[1])
print("5th student:", marks[4])
print("Last student:", marks[-1])
```

**Output:**

```text
Array: [78 85 92 67 88 73 95 81]
Data type: int64
Shape: (8,)
2nd student: 85
5th student: 88
Last student: 81
```

---

### 2. Slicing and Data Type

```python
arr = np.array([10, 20, 30, 40, 50, 60, 70, 80], dtype=np.int32)

print("First 4:", arr[:4])
print("Index 2 to 6:", arr[2:7])
print("Every second element:", arr[::2])
print("Data type:", arr.dtype)
```

**Output:**

```text
First 4: [10 20 30 40]
Index 2 to 6: [30 40 50 60 70]
Every second element: [10 30 50 70]
Data type: int32
```

---

### 3. Reshape and Indexing

```python
arr = np.arange(1, 21)

matrix = arr.reshape(4, 5)

print("Matrix:")
print(matrix)

print("Second row:", matrix[1])
print("Row 3, Column 4:", matrix[2, 3])
print("First two rows:")
print(matrix[:2])
print("Last three columns:")
print(matrix[:, -3:])
```

**Output:**

```text
Matrix:
[[ 1  2  3  4  5]
 [ 6  7  8  9 10]
 [11 12 13 14 15]
 [16 17 18 19 20]]

Second row: [ 6  7  8  9 10]
Row 3, Column 4: 14

First two rows:
[[ 1  2  3  4  5]
 [ 6  7  8  9 10]]

Last three columns:
[[ 3  4  5]
 [ 8  9 10]
 [13 14 15]
 [18 19 20]]
```

---

### 4. Copy vs View

```python
arr = np.array([10, 20, 30, 40, 50])

copy_arr = arr.copy()
view_arr = arr.view()

copy_arr[0] = 100
view_arr[1] = 200

print("Original:", arr)
print("Copy:", copy_arr)
print("View:", view_arr)
```

**Output:**

```text
Original: [ 10 200  30  40  50]
Copy: [100  20  30  40  50]
View: [ 10 200  30  40  50]
```

**Explanation:**
`copy()` creates an independent array, so changing `copy_arr` does not affect `arr`.

`view()` shares the same underlying data, so changing `view_arr` also changes `arr`.

---

### 5. 3D Array

```python
arr = np.arange(1, 25)

arr3d = arr.reshape(2, 3, 4)

print("Array:")
print(arr3d)

print("Shape:", arr3d.shape)

print("Element at [1, 2, 3]:", arr3d[1, 2, 3])

print("First 2D block:")
print(arr3d[0])
```

**Output:**

```text
Shape: (2, 3, 4)

Element at [1, 2, 3]: 24

First 2D block:
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]]
```

---

### 6. Iterating Through a Matrix

```python
marks = np.array([
    [78, 85, 90],
    [67, 72, 80],
    [88, 91, 95]
])

for row in marks:
    print("Row:", row)

print("\nEvery mark:")

for row in marks:
    for mark in row:
        print(mark)

print("Shape:", marks.shape)
```

**Output:**

```text
Row: [78 85 90]
Row: [67 72 80]
Row: [88 91 95]

Every mark:
78
85
90
67
72
80
88
91
95

Shape: (3, 3)
```

---

### 7. Mixed Slicing and Reshaping

```python
arr = np.arange(10, 41)

extracted = arr[5:17]

print("Original:", arr)
print("Extracted:", extracted)

reshaped = extracted.reshape(3, 4)

print("Reshaped array:")
print(reshaped)

print("Shape:", reshaped.shape)

print("Element:", reshaped[1, 2])
```

**Output:**

```text
Extracted: [15 16 17 18 19 20 21 22 23 24 25 26]

Reshaped array:
[[15 16 17 18]
 [19 20 21 22]
 [23 24 25 26]]

Shape: (3, 4)

Element: 21
```

> Note: `arr[5:17]` is used because we need **12 elements** to create a `3 × 4` array.

---

### 8. Copy, View and Slicing

```python
arr = np.array([
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
])

view_arr = arr[:2]
copy_arr = arr[1:].copy()

view_arr[0, 0] = 100
copy_arr[0, 0] = 500

print("Original:")
print(arr)

print("\nView:")
print(view_arr)

print("\nCopy:")
print(copy_arr)
```

**Output:**

```text
Original:
[[100  20  30]
 [ 40  50  60]
 [ 70  80  90]]

View:
[[100  20  30]
 [ 40  50  60]]

Copy:
[[500  50  60]
 [ 70  80  90]]
```

**Explanation:**

* `view_arr` shares data with `arr`, so changing it changes the original.
* `copy_arr` has independent data, so changing it does **not** change the original.

---

### 9. Employee Data

```python
salary = np.array([25000, 32000, 28000, 45000, 39000, 52000])

print("Shape:", salary.shape)
print("Data type:", salary.dtype)

print("Salaries greater than 30000:")
print(salary[salary > 30000])

salary_copy = salary.copy()

reshaped = salary.reshape(2, 3)

print("\nReshaped array:")
print(reshaped)

print("\nIterating:")

for row in reshaped:
    for value in row:
        print(value)
```

**Output:**

```text
Shape: (6,)
Data type: int64

Salaries greater than 30000:
[32000 45000 39000 52000]

Reshaped array:
[[25000 32000 28000]
 [45000 39000 52000]]

Iterating:
25000
32000
28000
45000
39000
52000
```

---

### 10. Comprehensive Challenge

```python
data = np.array([
    [10, 20, 30, 40],
    [50, 60, 70, 80],
    [90, 100, 110, 120]
])

# 1. Shape and data type
print("Shape:", data.shape)
print("Data type:", data.dtype)

# 2. Access 70
print("70:", data[1, 2])

# 3. Extract [20, 30, 40]
print("Sliced elements:", data[0, 1:4])

# 4. Last two rows
print("Last two rows:")
print(data[1:])

# 5. Create copy and view
copy_data = data.copy()
view_data = data.view()

# 6. Modify copy and view
copy_data[0, 0] = 500
view_data[1, 1] = 600

print("\nOriginal:")
print(data)

print("\nCopy:")
print(copy_data)

print("\nView:")
print(view_data)

# 7. Reshape original
reshaped = data.reshape(2, 6)

print("\nReshaped:")
print(reshaped)

# 8. Iterate
print("\nIterating:")

for row in reshaped:
    for value in row:
        print(value)
```

**Important observation:**

After:

```python
view_data[1, 1] = 600
```

the original `data` also changes because `view_data` is a **view**.

But:

```python
copy_data[0, 0] = 500
```

does **not** change the original because `copy_data` is an independent **copy**.

**Key concepts students should understand from this task:**

| Concept           | Example             |
| ----------------- | ------------------- |
| Creating array    | `np.array()`        |
| Creating sequence | `np.arange()`       |
| Indexing          | `arr[1, 2]`         |
| Slicing           | `arr[0, 1:4]`       |
| Data type         | `arr.dtype`         |
| Shape             | `arr.shape`         |
| Reshape           | `arr.reshape(2, 6)` |
| Copy              | `arr.copy()`        |
| View              | `arr.view()`        |
| Iterating         | `for row in arr`    |
