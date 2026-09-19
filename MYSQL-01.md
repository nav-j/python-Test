
## MySQL Practical Task – Product Management System

**Topics:** `CREATE DATABASE`, `CREATE TABLE`, `INSERT`, `SELECT`, `WHERE`, `ORDER BY`, `UPDATE`, `DELETE`, `LIMIT`

### Q1. Create Database and Table — 10 Marks

1. Create a database named **`shop_db`**.
2. Select the database.
3. Create a table named **`products`** with the following columns:

| Column       | Data Type     | Description        |
| ------------ | ------------- | ------------------ |
| product_id   | INT           | Primary Key        |
| product_name | VARCHAR(50)   | Product name       |
| category     | VARCHAR(50)   | Product category   |
| price        | DECIMAL(10,2) | Product price      |
| quantity     | INT           | Available quantity |
| city         | VARCHAR(50)   | Store city         |

---

### Q2. Insert Data — 10 Marks

Insert the following **8 records** into the `products` table:

| ID | Product Name | Category    | Price | Quantity | City       |
| -: | ------------ | ----------- | ----: | -------: | ---------- |
|  1 | Laptop       | Electronics | 55000 |       10 | Ludhiana   |
|  2 | Smartphone   | Electronics | 28000 |       15 | Chandigarh |
|  3 | Office Chair | Furniture   |  7500 |        8 | Amritsar   |
|  4 | Headphones   | Electronics |  2500 |       25 | Ludhiana   |
|  5 | Study Table  | Furniture   |  6500 |       12 | Delhi      |
|  6 | Keyboard     | Accessories |  1800 |       30 | Jalandhar  |
|  7 | Monitor      | Electronics | 15000 |        7 | Delhi      |
|  8 | Mouse        | Accessories |   900 |       40 | Amritsar   |

---

### Q3. SELECT and WHERE — 10 Marks

Write SQL queries to:

1. Display **all products**.
2. Display only `product_name`, `price`, and `quantity`.
3. Display products whose price is **greater than 5000**.
4. Display products from **Ludhiana**.
5. Display products belonging to the **Electronics** category.
6. Display products whose quantity is **less than 15**.

---

### Q4. ORDER BY and LIMIT — 10 Marks

Write SQL queries to:

1. Display products in **ascending order of price**.
2. Display products in **descending order of price**.
3. Display products in alphabetical order of `product_name`.
4. Display the **3 most expensive products**.
5. Display the **first 5 products** from the table.

---

### Q5. UPDATE and DELETE — 10 Marks

Write SQL queries to:

1. Update the price of **Laptop** from `55000` to `58000`.
2. Change the quantity of **Monitor** from `7` to `10`.
3. Change the city of **Study Table** from `Delhi` to `Ludhiana`.
4. Delete the product whose `product_id = 8`.
5. Delete all products whose price is **less than 2000**.

**Total: 50 Marks**
