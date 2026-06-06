# Comprehensive Financial & Sales Performance Dashboard

## 📌 Project Overview
This repository features an advanced **Power BI Dashboard** designed to transform raw financial and sales transaction data into actionable strategic insights. Built with a focus on interactive financial analysis, this project demonstrates robust data modeling, dynamic DAX computations, and executive-level visual storytelling tailored for corporate decision-making.

The dashboard provides a deep-dive analysis of revenue streams, profit margins, and year-over-year (YoY) performance metrics, allowing stakeholders to easily track business health at a glance.

---

## 🛠️ Core Features & Functionalities

### 1. Advanced Data Modeling
* **Schema:** Implemented a highly optimized **Star Schema** to ensure maximum report performance and scalability.
* **Tables:** Centered around a transactional Fact Table (`sales`) seamlessly linked to key Dimension Tables (`calendar`, `Dim_Products`, and `Dim_Customers`).

### 2. Tailored Visualizations & Charts
* **Interactive Drill-Throughs 🔍:** Custom drill-through pages that allow users to click on a specific region or product category to inspect granular customer-level transactions.
* **Sales Decomposition Tree 🌳:** An AI-powered visualization enabling root-cause analysis of sales performance across multiple organizational hierarchies.
* **Dynamic KPI Cards 🎯:** High-impact cards showcasing Actual vs. Target performance with conditional formatting indicators (Green/Red alerts).
* **Multi-Axis Trend Charts 📈:** Monthly revenue tracking combined with moving averages to smooth out seasonal fluctuations.

### 3. Sophisticated DAX Formulas 🧪
The analytical depth of this dashboard relies on optimized **DAX (Data Analysis Expressions)** measures. Key calculations include:


```dax
Active Customers = DISTINCTCOUNT(sales[customer_id])

Average Order Value = DIVIDE([Total Sales], [Total Orders], 0)

Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

Sales Last Year = CALCULATE([Total Sales], SAMEPERIODLASTYEAR(calendar[date]))

Total Orders = DISTINCTCOUNT(sales[order_id])

Total Profit = SUM(sales[profit])

Total Quantity = SUM(sales[quantity])

Total Sales = SUM(sales[revenue])

Year Sales Growth % = 
DIVIDE(
    [Total Sales] - [Sales Last Year], 
    [Sales Last Year], 
    0
)

## 👤 Author & Developer

### ⚡ Developed by **Ahmad Telmoudi**
**Financial Data Analyst**

This project was independently designed, developed, and is fully maintained by **Ahmad Telmoudi**. As a Financial Data Analyst, I specialize in building robust data architectures and creating comprehensive, automated business intelligence solutions that bridge the gap between complex raw transactional numbers and clear strategic execution.

***

*Thank you for exploring this repository! Feel free to reach out for professional collaborations, detailed feedback, or any technical inquiries regarding this implementation.*
