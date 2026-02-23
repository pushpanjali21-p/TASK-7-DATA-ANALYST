# TASK-7-DATA-ANALYST
# Task 7 – Basic Sales Summary using SQLite and Python

## Objective
The objective of this task is to use SQL inside Python to retrieve basic sales information such as total quantity sold and total revenue, and display the result using print statements and a simple bar chart.

---

## Tools Used
- Python
- SQLite (sqlite3 module)
- Pandas
- Matplotlib

---

## Dataset
A small SQLite database file named `sales_data.db` was created.
It contains one table named `sales` with the following columns:

- id
- product
- quantity
- price

---

##  SQL Query Used

```sql
SELECT product,
       SUM(quantity) AS total_quantity,
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
