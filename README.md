# 📊 Sales Insight Dashboard – Power BI

A comprehensive sales analytics dashboard built with Power BI and MySQL. This project provides interactive visual insights into revenue, sales quantity, customer behavior, and product performance to support strategic decision-making.

---

## 📌 Project Summary

This dashboard was created for a retail sales dataset stored in a MySQL database. It addresses key business challenges related to sales tracking, customer targeting, and performance comparison across different markets and time periods.

---

## 🎯 Business Problem

Sales managers lacked a centralized tool to:
- Monitor total sales revenue and volume over time
- Identify top-performing customers and products
- Compare performance across different markets
- Filter sales by specific fiscal periods
- Make data-driven decisions with clear visual support

---

## ✅ Business Goals

- Track overall **revenue** and **sales quantity (units sold)**
- Visualize **sales trends over time**
- Analyze performance by **market** and **customer**
- Identify the **Top products** and **Top customers**
- Enable dynamic filtering by **calendar date** and **custom fiscal period (`cy_date`)**

---

## 🔧 Data & Tools

- **Database**: MySQL
- **Visualization Tool**: Microsoft Power BI
- **Connection**: MySQL connector (ODBC)

### 📁 Tables Used:
![Screenshot 2025-07-07 004200](https://github.com/user-attachments/assets/426809ec-61f6-4d60-ba75-50463c07a978)


---

## 📐 Data Model

A star schema model was built in Power BI:
- Central fact table: `transactions`
- Dimension tables: `customers`, `products`, `markets`, `date`
- Relationships were set up via foreign keys (e.g., `customer_id`, `product_id`)

---

## 🧹 Data Cleaning & Transformation

Before visualizing the data in Power BI, several data preparation steps were performed to ensure accuracy and consistency:

- ✅ **Removed duplicate rows** from the `transactions` table
- ✅ **Normalized currency values**:
  - Sales amounts were recorded in both **USD** and **INR**
  - A new column was added to **convert all values to INR** using consistent exchange rates
- ✅ **Filtered out invalid records**:
  - Removed rows where `sales_amount` was negative or null


---
## 📊 Dashboard Features

### 📌 Key Measures:
- `Revenue = SUM(price_per_unit * quantity)`
- `Sales Quantity = SUM(quantity)`

### 📌 Visualizations:
- **Bar Charts**:
  - Revenue by Market
  - Revenue by Customer
  - Sales Quantity by Market
  - Sales Quantity by Customer

- **Line Chart**:
  - Revenue Trend (time series)

- **Slicers**:
  - Standard Date Picker
  - `cy_date` filter (e.g., `Sep17`, `Oct17`)

- **Top-N Filters**:
  - Top 5 Customers by Revenue
  - Top 5 Products by Revenue

---

## 📈 Outcome

This dashboard enables users to:
- Get a high-level overview of total sales and trends
- Drill down into performance by market or customer
- Identify top revenue contributors
- Analyze sales over selected timeframes using dynamic filters

---

## 📸 Screenshots


![Screenshot 2025-07-06 230548](https://github.com/user-attachments/assets/109e416f-ab65-43b2-b9e0-786f8365116b)

---

