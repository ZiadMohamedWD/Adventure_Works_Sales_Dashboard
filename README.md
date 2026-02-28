# 🧾 Power BI Project – Adventure Works Sales Dashboard  

## 📍 Training
**Information Technology Institute (ITI) – Data Analysis Scholarship**

## 💾 Data Source
**AdventureWorks2022 (SQL Server – DirectQuery Mode)**  
🔗 [Download AdventureWorks2022.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2022.bak)

---

## 📊 Project Overview
This project demonstrates business intelligence and data visualization skills using **Power BI**.  
The **Adventure Works Sales Dashboard** analyzes sales performance, growth trends, and regional performance for better decision-making insights.  

---

## 🧱 Data Modeling
**Tables Used:**
- `vw_DimProducts`  
- `vw_DimSalesPersons`  
- `vw_DimShipMethods`  
- `vw_DimStatuses`  
- `vw_DimTerritories`  
- `vw_FactOrderDetails`

**Data Model:**
- Connected tables using relationships between *FactOrderDetails* and *Dimension* tables.  
- Created a **Dates Table** using **DAX** for time intelligence functions.  

---

## 🧮 Measures (DAX)
- **No. Orders** = COUNTROWS(`vw_FactOrderDetails`)  
- **Total Subtotal** = SUM(`vw_FactOrderDetails[SubTotal]`)  
- **Total Tax** = SUM(`vw_FactOrderDetails[TaxAmt]`)  
- **Total Freight** = SUM(`vw_FactOrderDetails[Freight]`)  
- **Total Due** = SUM(`vw_FactOrderDetails[TotalDue]`)  
- **Total Quantity** = SUM(`vw_FactOrderDetails[OrderQty]`)  
- **Sales Growth %** =  
  ```DAX
  ( [Total Due] - CALCULATE([Total Due], DATEADD(Dates[Date], -1, YEAR)) ) /
  CALCULATE([Total Due], DATEADD(Dates[Date], -1, YEAR))
📄 Dashboard Pages
Page 1 – Overview

Visuals:

KPI Cards: No. Orders, Total Sales, Total Tax, Freight

Clustered Column Chart for sales summary

Slicers: Date, Territory, Salesperson

Purpose: General overview of sales performance.

Page 2 – Sales Performance

Charts:

Line Chart → Sales Growth % by Year

Scatter Chart → Sales vs. Tax (Bubble = No. Orders)

Bookmark toggle between:

Pie Chart: Sales by Territory

Bar Chart: Sales Growth % by Year

Purpose: Compare sales trends and performance metrics.

Page 3 – Drillthrough Insights (Bonus)

Visuals:

Detailed Salesperson report with Territory, Orders, and Total Sales.

Drillthrough button from other pages.

Back button navigation.

Purpose: Deep-dive analysis at salesperson level.

🧩 Skills Demonstrated

Power BI

DAX (Data Analysis Expressions)

SQL Server & DirectQuery

Data Modeling & Relationships

KPI Design

Interactive Dashboards & Storytelling

📈 Outcome

This project highlights the ability to:

Build and connect real-world databases in Power BI

Create time-based calculations and KPIs using DAX

Design dynamic, interactive dashboards for business insights
