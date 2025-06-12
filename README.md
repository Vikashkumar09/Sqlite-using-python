# Sales-Summary-Using-SQLite-and-Python
---
# 🧾 Task 7 - Sales Summary Using SQLite and Python

## 📌 Overview

This task demonstrates how to extract and visualise basic sales data from a SQLite database using Python. We use SQL queries to calculate **total quantity sold** and **total revenue** for each product, then display the results using `print()` and a `matplotlib` bar chart.

---

## 🧰 Tools & Technologies Used

- **Python 3**
- **SQLite** (`sales_data.db`)
- **pandas** – for reading and handling SQL query results
- **matplotlib** – for creating a bar chart

---

## 🗃️ Dataset

The data is stored in a local SQLite file: **`sales_data.db`**

It contains a single table: **`sales`**  
| Column   | Type    | Description              |
|----------|---------|--------------------------|
| id       | INTEGER | Primary key              |
| product  | TEXT    | Product name             |
| quantity | INTEGER | Quantity sold            |
| price    | REAL    | Unit price of product    |

---

## 🧪 Sample Data Inserted

```sql
INSERT INTO sales (product, quantity, price) VALUES ('Wireless Mouse', 12, 15.99);
INSERT INTO sales (product, quantity, price) VALUES ('USB-C Charger', 8, 19.99);
INSERT INTO sales (product, quantity, price) VALUES ('Bluetooth Headphones', 5, 49.99);
INSERT INTO sales (product, quantity, price) VALUES ('Laptop Stand', 7, 29.99);
INSERT INTO sales (product, quantity, price) VALUES ('HDMI Cable', 15, 9.99);
INSERT INTO sales (product, quantity, price) VALUES ('Wireless Mouse', 10, 15.99);
INSERT INTO sales (product, quantity, price) VALUES ('USB-C Charger', 5, 19.99);
INSERT INTO sales (product, quantity, price) VALUES ('Keyboard', 6, 39.99);
INSERT INTO sales (product, quantity, price) VALUES ('Bluetooth Headphones', 3, 49.99);
INSERT INTO sales (product, quantity, price) VALUES ('Laptop Stand', 4, 29.99);
```
---
# SQL Query Used
```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
```
---
# 🐍 Python Script Summary

- Connect to `sales_data.db`
- Execute the SQL query above using `sqlite3`
- Load the result into a pandas DataFrame
- Print the summarised table
- Plot revenue by product as a bar chart
---
#📁 Files Included
-sales_data.db – SQLite database
-sales_summary.ipynb – Python script for this task
-sales_chart.png – Bar chart output
-Readme.md – This file
---

## Author

👤 **Abhishek Verma**  

## Contact

📧 Email: [abhisehekverma6290@gmail.com]

## LinkedIn

🔗 Connect with me on [LinkedIn](https://www.linkedin.com/in/abhishek-verma-52603a313/)





