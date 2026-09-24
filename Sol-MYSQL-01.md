## MySQL Solution

### Q1. Create Database and Table

```sql
CREATE DATABASE shop_db;

USE shop_db;

CREATE TABLE products (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(50),
    category VARCHAR(50),
    price DECIMAL(10,2),
    quantity INT,
    city VARCHAR(50)
);
```

---

### Q2. Insert Data

```sql
INSERT INTO products
(product_id, product_name, category, price, quantity, city)
VALUES
(1, 'Laptop', 'Electronics', 55000, 10, 'Ludhiana'),
(2, 'Smartphone', 'Electronics', 28000, 15, 'Chandigarh'),
(3, 'Office Chair', 'Furniture', 7500, 8, 'Amritsar'),
(4, 'Headphones', 'Electronics', 2500, 25, 'Ludhiana'),
(5, 'Study Table', 'Furniture', 6500, 12, 'Delhi'),
(6, 'Keyboard', 'Accessories', 1800, 30, 'Jalandhar'),
(7, 'Monitor', 'Electronics', 15000, 7, 'Delhi'),
(8, 'Mouse', 'Accessories', 900, 40, 'Amritsar');
```

---

## Q3. SELECT and WHERE

### 1. Display all products

```sql
SELECT * FROM products;
```

### 2. Display product name, price and quantity

```sql
SELECT product_name, price, quantity
FROM products;
```

### 3. Products with price greater than 5000

```sql
SELECT * FROM products
WHERE price > 5000;
```

### 4. Products from Ludhiana

```sql
SELECT * FROM products
WHERE city = 'Ludhiana';
```

### 5. Products in Electronics category

```sql
SELECT * FROM products
WHERE category = 'Electronics';
```

### 6. Products with quantity less than 15

```sql
SELECT * FROM products
WHERE quantity < 15;
```

---

## Q4. ORDER BY and LIMIT

### 1. Products in ascending order of price

```sql
SELECT * FROM products
ORDER BY price ASC;
```

### 2. Products in descending order of price

```sql
SELECT * FROM products
ORDER BY price DESC;
```

### 3. Products in alphabetical order

```sql
SELECT * FROM products
ORDER BY product_name ASC;
```

### 4. Three most expensive products

```sql
SELECT * FROM products
ORDER BY price DESC
LIMIT 3;
```

### 5. First 5 products

```sql
SELECT * FROM products
LIMIT 5;
```

---

## Q5. UPDATE and DELETE

### 1. Update Laptop price to 58000

```sql
UPDATE products
SET price = 58000
WHERE product_name = 'Laptop';
```

### 2. Change Monitor quantity to 10

```sql
UPDATE products
SET quantity = 10
WHERE product_name = 'Monitor';
```

### 3. Change Study Table city to Ludhiana

```sql
UPDATE products
SET city = 'Ludhiana'
WHERE product_name = 'Study Table';
```

### 4. Delete product with ID 8

```sql
DELETE FROM products
WHERE product_id = 8;
```

### 5. Delete products with price less than 2000

```sql
DELETE FROM products
WHERE price < 2000;
```

### Important Note

When using `UPDATE` or `DELETE`, be careful with the `WHERE` condition.

For example:

```sql
UPDATE products
SET price = 1000;
```

This would change the price of **every product**. Using `WHERE` limits the operation to the intended records.
