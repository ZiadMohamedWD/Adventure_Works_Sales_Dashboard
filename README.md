# AdventureWorks Sales Analysis: SQL to Power BI Pipeline

## Project Overview
This project demonstrates an end-to-end Business Intelligence workflow, transforming the complex **AdventureWorks** relational database into an interactive Power BI dashboard. By using a series of custom T-SQL views, I built a high-performance **Star Schema** to analyze sales performance, product trends, and regional demographics.

## Data Architecture (The "Star Schema")
Instead of connecting Power BI directly to raw transactional tables, I engineered a dedicated analytical layer using SQL views (`vw_`). This ensures the data is clean, pre-joined, and optimized for DAX measures.

### Analytical Layers:
* **Fact Table:** `vw_FactOrderDetails` (Sales metrics, quantities, and revenue).
* **Dimensions:** * `vw_DimProducts` (Categories, subcategories, and specs).
    * `vw_DimSalesPersons` (Staff performance and tracking).
    * `vw_DimTerritories` (Regional and geographic grouping).
    * `vw_DimShipMethods` & `vw_DimStatuses`.

## Tech Stack
* **Database:** SQL Server (AdventureWorks Sample DB).
* **Data Engineering:** T-SQL (Views for ETL/Data Modeling).
* **BI Tool:** Power BI Desktop.
* **Modeling:** Star Schema & DAX.

## Key Insights & Features
* **Automated Data Pipeline:** The use of SQL views allows for a "plug-and-play" experience where Power BI only ingests the necessary columns, significantly reducing refresh times.
* **Dynamic Sales Tracking:** Built DAX measures to track Year-over-Year (YoY) growth and Profit Margins across different product lines.
* **Territory Performance:** Visualized sales distribution to identify underperforming regions and high-value sales reps.

## Dashboard Preview
![Dashboard Screenshot](https://github.com/ZiadMohamedWD/Adventure_Works_Sales_Dashboard/blob/main/Screenshot%202026-02-28%20214920.png)

![Dashboard Screenshot](https://github.com/ZiadMohamedWD/Adventure_Works_Sales_Dashboard/blob/main/Screenshot%202026-02-28%20214933.png)

![Dashboard Screenshot](https://github.com/ZiadMohamedWD/Adventure_Works_Sales_Dashboard/blob/main/Screenshot%202026-02-28%20214952.png)

![Dashboard Screenshot](https://github.com/ZiadMohamedWD/Adventure_Works_Sales_Dashboard/blob/main/Screenshot%202026-02-28%20215005.png)
