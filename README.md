# 🍫 Chocolate Sales Performance Dashboard

## 📌 Project Overview

This project provides a **Strategic Sales Analysis** for a chocolate distribution business. It tracks **$6.18M in total revenue** across multiple countries and sales representatives, offering insights into product popularity, seasonal trends, and regional performance.

---

## 🛠️ Data Cleaning & Transformation (ETL)

A significant portion of this project was dedicated to ensuring data quality. The following steps were taken using **Power Query**:

- **Duplicate Removal**  
  Identified and removed redundant transaction IDs to ensure sales figures weren't inflated.

- **Null Value Management**  
  Handled missing values in the `Amount` and `Boxes` columns to maintain calculation accuracy.

- **Column Optimization**  
  Removed unnecessary metadata columns that were not required for the final analysis, reducing file size and improving refresh rates.

- **Data Type Formatting**  
  Standardized currency and date formats for seamless time-series analysis.

---

## 📊 Dashboard Insights & Visualizations

### 1️⃣ Sales Performance Metrics (KPIs)

- **Total Sales ($6.18M)**  
  The primary metric representing overall business scale.

- **Revenue Per Box ($34.93)**  
  A critical efficiency metric calculated using DAX to understand unit profitability.

---

### 2️⃣ Trend Analysis

- **Monthly Sales Trend**  
  The line chart reveals a significant growth phase from April to June, allowing management to plan for seasonal demand and inventory allocation.

---

### 3️⃣ Geographical Distribution

- **Sales by Country**  
  A donut chart highlighting **Australia** and **New Zealand** as the top-performing regions, accounting for over 35% of total revenue.

---

### 4️⃣ Top Products & Sales Team Performance

- **Product Ranking**  
  Identifies *"Smooth Silk"* and *"50% Dark"* as flagship SKUs driving revenue.

- **Salesperson Performance**  
  A bar chart benchmarks the sales team, identifying top revenue generators and performance gaps.

---

## 📑 DAX Measures Documentation

Below are the custom DAX measures developed to power the analytical engine of this dashboard.

### 📊 Sales Aggregations

```dax
Total Sales =
SUM('Chocolate Sales'[Amount])

Total Boxes =
SUM('Chocolate Sales'[Boxes Shipped])

Avg Sales per Order =
AVERAGE('Chocolate Sales'[Amount])
```

---

### 📈 Efficiency Metric

This measure determines the average revenue generated for every box shipped, supporting pricing and logistics strategy.

```dax
Revenue per Box =
DIVIDE([Total Sales], [Total Boxes])
```

---

### 🎨 UI/UX Enhancement

Used for background transparency in custom visuals to maintain a clean, branded aesthetic.

```dax
Remove BG = "rgba(255, 255, 255, 0)"
```

---

## 🚀 Key Takeaways for the Business

- **Focus on High-Margin Products**  
  Prioritize the top 3 products in marketing campaigns.

- **Regional Strategy**  
  Increase marketing spend in Australia to capitalize on existing growth momentum.

- **Sales Training & Mentorship**  
  Pair top-performing sales representatives with lower-performing reps to improve team-wide performance.

---

## 💻 Tech Stack

- **Power BI** → Visualization & Data Modeling  
- **Power Query (M)** → Data Cleaning & ETL  
- **DAX** → Advanced Calculations & Statistical Analysis
