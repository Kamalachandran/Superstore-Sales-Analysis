# Overview

This repository contains everything you need to build a production-ready **Sales Analysis Report** in Power BI.  
The focus areas are:

- **Importing and shaping sales data (Power Query)**  
  Transform raw sales data into a clean, structured format ready for analysis.  

- **Designing a clean data model (Star Schema)**  
  Organize fact and dimension tables for performance and clarity.  

- **Building core DAX measures for business KPIs**  
  Define metrics such as Total Sales, Profit, Average Order Value, and YoY Growth.  

- **Creating an actionable multi-page report with exportable visuals**  
  Deliver interactive dashboards that provide insights and allow CSV/Excel exports.

   
## Expected Dataset(s)

The following primary tables are required for building the Power BI Sales Analysis report:

### 1. Sales (Transactional Data)
- **order_id** (text)  
- **order_date** (date)  
- **ship_date** (date)  
- **customer_id** (text)  
- **product_id** (text)  
- **quantity** (number)  
- **unit_price** (decimal)  
- **discount** (decimal, 0–1 or percent)  
- **sales** (decimal) → usually calculated as `quantity * unit_price * (1 - discount)`  
- **profit** (decimal)  
- **ship_mode**, **region**, **city**, **state**, **postal_code**, **segment** (categorical)  

### 2. Customers
- **customer_id**  
- **customer_name**  
- **segment**  
- **city**  
- **state**  
- **join_date**, etc.  

### 3. Products
- **product_id**  
- **product_name**  
- **category**  
- **sub_category**  
- **list_price**  
- **cost**, etc.  

### 4. Calendar / Date (Recommended)
- **date**  
- **year**, **quarter**, **month**, **day**  
- **fiscal fields** (fiscal year/quarter/month)  
- **isHoliday**, etc.  

> ⚠️ **Note**: The `Calendar/Date` table should be created in Power BI and marked as the official Date Table for correct time intelligence calculations.
