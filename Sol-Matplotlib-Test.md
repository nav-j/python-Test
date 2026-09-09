Absolutely. Below is the **complete solution** for the 50-mark Matplotlib practical task.

## Solution

### Common Dataset

```python
import numpy as np
import matplotlib.pyplot as plt

months = np.array(["Jan", "Feb", "Mar", "Apr", "May", "Jun"])
sales = np.array([120, 150, 180, 140, 200, 230])
expenses = np.array([80, 90, 100, 95, 110, 120])
students = np.array([25, 30, 28, 35, 40, 45])
marks = np.array([65, 72, 80, 55, 90, 68, 75, 88, 60, 95])
```

---

## Question 1 — Line Plot

```python
import numpy as np
import matplotlib.pyplot as plt

months = np.array(["Jan", "Feb", "Mar", "Apr", "May", "Jun"])
sales = np.array([120, 150, 180, 140, 200, 230])
expenses = np.array([80, 90, 100, 95, 110, 120])

plt.plot(months, sales, label="Sales", marker="o")
plt.plot(months, expenses, label="Expenses", marker="o")

plt.title("Monthly Sales and Expenses")
plt.xlabel("Month")
plt.ylabel("Amount")

plt.legend()
plt.show()
```

### Explanation

* `plt.plot()` creates a line graph.
* `label` gives a name to each line.
* `marker="o"` displays points on the lines.
* `plt.legend()` displays Sales and Expenses.

---

## Question 2 — Bar Chart

```python
import numpy as np
import matplotlib.pyplot as plt

months = np.array(["Jan", "Feb", "Mar", "Apr", "May", "Jun"])
students = np.array([25, 30, 28, 35, 40, 45])

plt.bar(months, students)

plt.title("Number of Students per Month")
plt.xlabel("Month")
plt.ylabel("Number of Students")

plt.show()
```

### Bonus — Display Values Above Bars

```python
plt.bar(months, students)

for i in range(len(students)):
    plt.text(i, students[i], students[i], ha="center", va="bottom")

plt.title("Number of Students per Month")
plt.xlabel("Month")
plt.ylabel("Number of Students")

plt.show()
```

Here:

```python
plt.text(i, students[i], students[i])
```

places the value above each bar.

---

## Question 3 — Scatter Plot

```python
import numpy as np
import matplotlib.pyplot as plt

students = np.array([25, 30, 28, 35, 40, 45])
sales = np.array([120, 150, 180, 140, 200, 230])

plt.scatter(students, sales, label="Students vs Sales")

plt.title("Students vs Sales")
plt.xlabel("Number of Students")
plt.ylabel("Sales")

plt.legend()
plt.show()
```

### Answer

There appears to be a **positive relationship** between students and sales.

Generally, when the number of students increases, sales also tend to increase.

However, the relationship is not perfectly consistent—for example, the data for April does not follow the general pattern exactly.

---

## Question 4 — Histogram

```python
import numpy as np
import matplotlib.pyplot as plt

marks = np.array([65, 72, 80, 55, 90, 68, 75, 88, 60, 95])

plt.hist(marks, bins=5)

plt.title("Distribution of Marks")
plt.xlabel("Marks")
plt.ylabel("Number of Students")

plt.show()
```

### Explanation

```python
plt.hist(marks, bins=5)
```

creates a histogram using **5 intervals (bins)**.

The histogram shows how the marks are distributed among different ranges.

### Answer

The exact highest range depends on the bin boundaries Matplotlib creates from the minimum to maximum mark. With these values, the range around **63–71** contains the most observations.

---

# Question 5 — Subplots

```python
import numpy as np
import matplotlib.pyplot as plt

months = np.array(["Jan", "Feb", "Mar", "Apr", "May", "Jun"])
sales = np.array([120, 150, 180, 140, 200, 230])
expenses = np.array([80, 90, 100, 95, 110, 120])
students = np.array([25, 30, 28, 35, 40, 45])
marks = np.array([65, 72, 80, 55, 90, 68, 75, 88, 60, 95])

# Plot 1 - Line Plot
plt.subplot(2, 2, 1)
plt.plot(months, sales, marker="o")
plt.title("Monthly Sales")
plt.xlabel("Month")
plt.ylabel("Sales")

# Plot 2 - Bar Chart
plt.subplot(2, 2, 2)
plt.bar(months, expenses)
plt.title("Monthly Expenses")
plt.xlabel("Month")
plt.ylabel("Expenses")

# Plot 3 - Scatter Plot
plt.subplot(2, 2, 3)
plt.scatter(students, sales)
plt.title("Students vs Sales")
plt.xlabel("Students")
plt.ylabel("Sales")

# Plot 4 - Histogram
plt.subplot(2, 2, 4)
plt.hist(marks, bins=5)
plt.title("Marks Distribution")
plt.xlabel("Marks")
plt.ylabel("Students")

plt.tight_layout()
plt.show()
```

### Understanding `subplot()`

```python
plt.subplot(2, 2, 1)
```

means:

* `2` → 2 rows
* `2` → 2 columns
* `1` → first position

So the layout is:

```text
+-------------------+-------------------+
|    Plot 1         |     Plot 2        |
|   Line Plot       |    Bar Chart      |
+-------------------+-------------------+
|    Plot 3         |     Plot 4        |
|  Scatter Plot     |    Histogram      |
+-------------------+-------------------+
```

`plt.tight_layout()` automatically adjusts spacing so that titles and labels don't overlap.
