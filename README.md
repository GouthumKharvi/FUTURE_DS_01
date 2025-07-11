# FUTURE_DS_01
E-commerce Sales Dashboard using Power BI



````markdown
# 📊 Business Sales Dashboard – Ecommerce Sales Data (Power BI)

## 📁 Project Overview

This project is part of **Future Interns – Data Science & Analytics Internship (Task 1)**.  
The goal is to work with raw e-commerce sales data, clean and model it, and build a professional Power BI dashboard that helps business users answer key questions like:

- ✅ What are the best-selling products?
- ✅ When do sales peak during the year?
- ✅ Which categories or regions bring the most revenue?

---

## 📌 Dataset Used

- **Dataset Chosen**: `Superstore Sales Dataset`
- Contains tables:
  - `Orders`: Sales transactions including product, date, discount, profit, region info
  - `Returns`: Returned Order IDs
  - `People`: Manager by Region
  - `OrdersUnique`: Created manually for relationship setup
  - `SalesForecast`: 15-day forecast data

---

## ⚙️ Data Cleaning & Modeling

Performed in **Power Query**:
- Removed null values and empty rows
- Identified and removed duplicate Order IDs by creating a unique `OrdersUnique` table
- Ensured all data types were correctly assigned
- Created relationships:
  - `Orders[Order ID]` ↔ `Returns[Order ID]`
  - `Orders[Region]` ↔ `People[Region]`
  - `Orders[Order ID]` ↔ `OrdersUnique[Order ID]`

---

## 🔢 Key Measures (DAX)

Created DAX measures to derive KPIs:

```DAX
Total Sales = SUM(Orders[Sales])
Total Quantity = SUM(Orders[Quantity])
Total Profit = SUM(Orders[Profit])
Total Returns = CALCULATE(COUNT(Returns[Order ID]))
Avg Delivery Days = AVERAGE(DATEDIFF(Orders[Order Date], Orders[Ship Date], DAY))
````

---

## 📊 Dashboard Visuals (Page 1)

### 🟦 KPI Cards

* Total Sales
* Total Profit
* Total Quantity
* Total Returns

### 📊 Visual Charts

* **Donut Chart** – Sales by Region (East, West, South, Central)
* **Donut Chart** – Sales by Segment (Consumer, Corporate, Home Office)
* **Area Chart** – Sales by Month-Year (2011–2014)
* **Area Chart** – Profit by Month-Year
* **Clustered Bar Chart** – Sales by Ship Mode
* **Clustered Bar Chart** – Top 3 Sub-Categories by Sales
* **Clustered Bar Chart** – Top 5 Products by Sales
* **Map Chart** – Sales and Profit by State

### 🎛 Filters Used

* Region Slicer: East, West, Central, South
* Interactive chart filtering enabled with **Edit Interactions**

---

## 📈 Forecasting Page (Page 2)

* **Line Chart** – Business Sales Forecast (Next 15 Days)
* **Line Chart (Zoomed)** – Forecast with Zoom-Pan enabled
* **Clustered Horizontal Bar Chart** – Top 10 States by Sales

---

## 🧠 Summary Page (Page 3)

### 📌 Insights Summary:

* 🔝 **Best-Selling Product**: Canon image CLASS 2200 Advanced Copier (₹62K sales)
* 📆 **Peak Sales Period**: November and December (all 4 years show high values)
* 🏆 **Top Regions**: West (32%) and East (30%) contribute the highest sales
* 🗂️ **Top Categories**: Technology (₹0.84M) and Furniture (₹0.74M)

---

## 🎯 Skills Demonstrated

* ✅ Data Cleaning & Transformation (Power Query)
* ✅ Data Modeling and Relationships
* ✅ DAX Measures and Calculations
* ✅ Forecasting and Trend Analysis
* ✅ Business Storytelling with Visuals
* ✅ Interactive Dashboard Design in Power BI

---

## 📥 Tools Used

* **Power BI Desktop**
* **Microsoft Excel** (basic exploration)
* (Optional) SQL – Not used in this task

---

## 📸 Screenshots

📌 *Included screenshots of My  dashboard pages here in the GitHub repo.*

---

## 🚀 How to View

1. Clone this repo or download the `.pbix` file
2. Open in [Power BI Desktop](https://powerbi.microsoft.com/)
3. Explore each page:

   * Dashboard
   * Forecast
   * Summary

---




