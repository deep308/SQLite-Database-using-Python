
# 🧾 Task 7 – SQLite Sales Summary Using Python

This project demonstrates how to use SQL inside Python to pull basic sales information from a tiny SQLite database, summarize it, and visualize the results using a bar chart.

---

## 📌 Objective

- Connect Python to a SQLite database.
- Run basic SQL to calculate:
  - Total quantity sold per product
  - Total revenue per product
- Display the results using:
  - `print()` for tabular summary
  - `matplotlib` for bar chart

---

## 📁 Dataset

A single SQLite database file: `sales_data.db`  
Containing one table: `sales`

### Table Structure:
| Column        | Type     |
|---------------|----------|
| product       | TEXT     |
| quantity      | INTEGER  |
| unit_price    | REAL     |
| total_revenue | REAL     |

---

## 🛠️ Tools Used

- Python 3.x
- SQLite3 (built-in)
- Pandas
- Matplotlib

---

## 💡 SQL Query Used

```sql
SELECT 
  product, 
  SUM(quantity) AS total_qty, 
  SUM(total_revenue) AS revenue 
FROM sales 
GROUP BY product;
```

---

## 📊 Output

- A printed DataFrame showing product-wise quantity and revenue
- A bar chart saved as `sales_chart.png` visualizing revenue by product

---

## 🗂️ Project Structure

```
task7-sales-summary/
├── sales_data.db            # SQLite database with product sales
├── task7- SQLite Sales Summary Using Python.py          # Python script to run SQL + visualize
├── sales_chart.png          # Output bar chart
└── README.md                # This file
```

---


