# Intermediate NumPy Mixed Practical Task — 10 Questions

**Topics:** Array Creation, Indexing, Slicing, Data Types, Copy, View, Shape, Reshape, and Iterating

**Instructions:** Use `import numpy as np`. Each question combines multiple NumPy concepts rather than testing them separately.

### 1. Student Marks Array

Create a NumPy array containing the marks of 8 students:

```python
[78, 85, 92, 67, 88, 73, 95, 81]
```

Print:

* The array
* Its data type
* Its shape
* The marks of the 2nd, 5th, and last student.
  **(5 Marks)**

### 2. Slicing and Data Type

Create the following array using `int32`:

```python
[10, 20, 30, 40, 50, 60, 70, 80]
```

Using slicing:

* Extract the first 4 elements.
* Extract elements from index 2 to 6.
* Extract every second element.
* Print the data type of the array.
  **(5 Marks)**

### 3. Reshape and Indexing

Create an array containing numbers from 1 to 20 and reshape it into a **4 × 5** matrix.

Using indexing and slicing, display:

* The complete second row.
* The element at row 3, column 4.
* The first two rows.
* The last three columns.
  **(5 Marks)**

### 4. Copy vs View

Create:

```python
arr = np.array([10, 20, 30, 40, 50])
```

Create both a **copy** and a **view** of `arr`.

Change one element in the copy and another element in the view. Print all three arrays and observe how the changes affect the original array.
**(5 Marks)**

### 5. 3D Array

Create a NumPy array containing numbers from 1 to 24 and reshape it into:

```text
2 × 3 × 4
```

Print:

* The array
* Its shape
* The element at `[1, 2, 3]`
* The first 2D block using indexing.
  **(5 Marks)**

### 6. Iterating Through a Matrix

Create:

```python
marks = np.array([
    [78, 85, 90],
    [67, 72, 80],
    [88, 91, 95]
])
```

Using nested loops:

* Print every mark individually.
* Print each row separately.
* Print the shape of the array.
  **(5 Marks)**

### 7. Mixed Slicing and Reshaping

Create an array containing numbers from 10 to 40.

* Extract elements from index 5 to 15.
* Reshape the extracted elements into a suitable 2D array.
* Print its shape.
* Access one element from the reshaped array using indexing.
  **(5 Marks)**

### 8. Copy, View and Slicing

Given:

```python
arr = np.array([
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
])
```

Create a **view** containing the first two rows and a **copy** containing the last two rows.

Modify one element in each and print the original array, view, and copy. Explain which modification affects the original array and why.
**(5 Marks)**

### 9. Employee Data

Create a NumPy array:

```python
salary = np.array([25000, 32000, 28000, 45000, 39000, 52000])
```

Perform the following:

* Print the shape and data type.
* Extract salaries greater than `30000` using slicing/indexing.
* Create a copy of the array.
* Reshape the original array into `2 × 3`.
* Iterate through the reshaped array and print each salary.
  **(5 Marks)**

### 10. Comprehensive Challenge

Create the following array:

```python
data = np.array([
    [10, 20, 30, 40],
    [50, 60, 70, 80],
    [90, 100, 110, 120]
])
```

Perform all of the following in one program:

1. Print its shape and data type.
2. Access `70` using indexing.
3. Extract `[20, 30, 40]` using slicing.
4. Extract the last two rows.
5. Create a **copy** and a **view**.
6. Modify one element in each.
7. Reshape the original array into `2 × 6`.
8. Iterate through the reshaped array and print each element.

**(5 Marks)**

**Total: 50 Marks**
