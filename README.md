# 🏀 Nike Sales Analysis Dashboard (Excel + Power Query)

## 📌 Project Overview

This project focuses on analyzing retail and online sales data to uncover insights related to revenue, profitability, discount strategies, and customer segments.

The dashboard was built using **Microsoft Excel**, leveraging **Power Query for data cleaning** and **Pivot Tables + Charts for visualization**.

---

## 🎯 Objectives

* Clean and preprocess raw sales data
* Correct inconsistencies in MRP, Revenue, and Profit
* Analyze the impact of discounts on profitability
* Compare performance across regions, channels, and product categories
* Build an interactive dashboard with actionable insights

---

## 🛠️ Tools Used

* Microsoft Excel
* Power Query
* Pivot Tables
* Data Visualization (Charts, Slicers)

---
flowchart LR

A[Cleaned Data] --> B[Pivot Tables]
B --> C[KPI Cards]
B --> D[Charts]
B --> E[Slicers]

D --> F[Revenue by Region]
D --> G[Monthly Trends]
D --> H[Discount vs Profitability]
D --> I[Top Products]

E --> J[Gender Filter]
E --> K[Region Filter]
E --> L[Channel Filter]

F --> M[Final Dashboard]
G --> M
H --> M
I --> M
C --> M
J --> M
K --> M
L --> M

## 🧹 Data Cleaning Process

### 1. Handling Missing & Incorrect Values

* Replaced null values using appropriate techniques
* Standardized inconsistent entries (e.g., region names)

### 2. Correcting MRP

* Grouped data by `Product_Name`
* Calculated **Median MRP**
* Merged back into main dataset
* Created `MRP_Clean` column:

  * If MRP is null → use median
  * Else → use original MRP

---

### 3. Fixing Discount Values

* Corrected values where discount > 1 (converted to percentage format)

---

### 4. Revenue Calculation

```excel
Revenue = Units_Sold × MRP_Clean × (1 - Discount)
```

---

### 5. Profit Handling

* Profit column retained from dataset
* Removed invalid rows:

  * Where `Units_Sold = 0` but Profit ≠ 0

---

### 6. Profit Margin Calculation

```excel
Profit Margin = Profit / Revenue
```

⚠️ Important:

* Calculated **outside Pivot Table** to avoid aggregation errors

---

## 📊 Dashboard Features

### 🔹 KPI Cards

* Total Revenue: ₹73,82,044
* Total Profit: ₹6,65,885
* Profit Margin: 9%
* Units Sold: 1213
* Best Product: Premier III
* Best Region: Mumbai

---

### 🔹 Visualizations

* Revenue & Profit by Region
* Monthly Revenue Trend
* Discount vs Profitability (Combo Chart)
* Most Profitable Products
* Profit Distribution by Gender
* Category-wise Performance

---

### 🔹 Filters (Slicers)

* Gender
* Sales Channel (Online / Retail)
* Region
* Year
* Discount Bucket

---

## 🔍 Key Insights

### 1. Channel Performance

Retail channel delivers higher profit margins compared to online sales.

👉 Recommendation:
Optimize online pricing strategy and reduce excessive discounting.

---

### 2. Discount Strategy

High discounts (>50%) significantly reduce profit margins (~6%).

👉 Recommendation:
Focus on moderate discount ranges (10–30%) for better profitability.

---

### 3. Revenue Concentration

Majority of revenue comes from low discount (0–10%) sales.

👉 Recommendation:
Avoid unnecessary discounting on high-demand products.

---

### 4. Customer Segment

Kids category contributes the highest share of profit.

👉 Recommendation:
Increase focus on high-performing segments.

---

## 🚀 How to Use

1. Open the Excel file
2. Navigate to the **Dashboard** sheet
3. Use slicers to filter data dynamically
4. Explore insights across different dimensions

---

## 📈 Project Outcome

* Built a complete end-to-end data analysis workflow
* Transformed raw, inconsistent data into actionable insights
* Developed an interactive dashboard with business recommendations

---

## 📌 Future Improvements

* Convert dashboard to Power BI for advanced visuals
* Add cost data for more accurate profit analysis
* Automate data refresh using Power Query

---

## 📎 Author

Harsh Vardhan

---

## ⭐ If you found this useful

Give this repo a star and feel free to connect!

