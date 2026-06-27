# 🚀 Sales Analytics Data Warehouse Project

## 📊 Building a Normalized Star Schema Data Model in Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-Analytics-yellow?style=for-the-badge&logo=powerbi)
![Data Warehouse](https://img.shields.io/badge/Data%20Warehouse-Star%20Schema-blue?style=for-the-badge)
![Excel](https://img.shields.io/badge/Data%20Source-Excel-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Project-Completed-success?style=for-the-badge)

---

## 📌 Project Overview

This project demonstrates the implementation of a **Normalized Star Schema Data Model** using **Power BI**. The objective is to transform raw business data into a scalable analytical model optimized for reporting, dashboarding, and business intelligence solutions.

The model integrates multiple dimension and fact tables following data warehousing best practices to provide high-performance analytics and insightful visualizations.

---

## 🎯 Business Problem

Organizations often store transactional data across multiple systems, making reporting and analysis difficult.

### Challenges

- Data redundancy
- Slow reporting performance
- Complex relationships
- Inconsistent business metrics
- Difficult scalability

### Solution

A normalized star schema architecture was implemented to:

- Improve query performance
- Reduce redundancy
- Simplify reporting
- Enable scalable analytics
- Support advanced Power BI dashboards

---

# 🏗️ Data Model Architecture

## Fact Tables

### Sales_Fact

Stores all sales transactions.

| Column | Description |
|----------|------------|
| SalesID | Unique Sales Transaction |
| CustomerID | Customer Key |
| ProductID | Product Key |
| RegionID | Region Key |
| DateKey | Date Key |
| Quantity | Units Sold |
| Revenue | Sales Revenue |
| Discount | Applied Discount |

---

### Returns_Fact

Stores returned sales transactions.

| Column | Description |
|----------|------------|
| ReturnID | Return Transaction |
| SalesID | Related Sale |
| ReturnDateKey | Return Date |
| ReturnReason | Reason for Return |

---

## Dimension Tables

### Customer_Dim

- CustomerID
- FullName
- Gender
- Age
- Segment

### Product_Dim

- ProductID
- ProductName
- Category
- SubCategory
- Brand

### Region_Dim

- RegionID
- Country
- State
- City

### Date_Dim

- DateKey
- Date
- Day
- Month
- Quarter
- Year

---

# ⭐ Star Schema Design

```text
                     Date_Dim
                         |
                         |
Customer_Dim ---- Sales_Fact ---- Product_Dim
                         |
                         |
                    Region_Dim
                         |
                         |
                    Returns_Fact
```

---

# 🔗 Data Relationships

| Fact Table | Key | Dimension Table |
|------------|-----|----------------|
| Sales_Fact | CustomerID | Customer_Dim |
| Sales_Fact | ProductID | Product_Dim |
| Sales_Fact | RegionID | Region_Dim |
| Sales_Fact | DateKey | Date_Dim |
| Returns_Fact | SalesID | Sales_Fact |

---

# 📈 Business KPIs

## Sales Metrics

- Total Revenue
- Total Sales
- Average Order Value
- Quantity Sold
- Discount Analysis

## Customer Metrics

- Customer Segmentation
- Repeat Customers
- Customer Growth
- Demographic Analysis

## Product Metrics

- Best Selling Products
- Category Performance
- Brand Performance

## Returns Metrics

- Return Count
- Return Rate %
- Return Reasons
- Product Return Analysis

## Regional Metrics

- Country-wise Revenue
- State Performance
- City Analysis

---

# ⚙️ ETL Workflow

## Extract

Data imported from:

```text
Customer_Dim.xlsx
Product_Dim.xlsx
Region_Dim.xlsx
Date_Dim.xlsx
Sales_Fact.xlsx
Returns_Fact.xlsx
```

## Transform

Performed using Power Query:

- Data Cleaning
- Data Validation
- Duplicate Removal
- Relationship Creation
- Data Type Formatting

## Load

Loaded into Power BI Data Model.

---

# 🧮 DAX Measures

### Total Revenue

```DAX
Total Revenue =
SUM(Sales_Fact[Revenue])
```

### Total Quantity Sold

```DAX
Total Quantity Sold =
SUM(Sales_Fact[Quantity])
```

### Total Sales

```DAX
Total Sales =
COUNT(Sales_Fact[SalesID])
```

### Total Returns

```DAX
Total Returns =
COUNT(Returns_Fact[ReturnID])
```

### Return Rate %

```DAX
Return Rate % =
DIVIDE(
    [Total Returns],
    [Total Sales],
    0
)
```

---

# 📊 Dashboard Pages

## Executive Dashboard

- Revenue Overview
- KPI Cards
- Monthly Trend Analysis
- Sales Performance

## Customer Dashboard

- Customer Segmentation
- Customer Growth
- Demographic Insights

## Product Dashboard

- Product Rankings
- Category Analysis
- Brand Performance

## Region Dashboard

- Geographic Sales Analysis
- Revenue by State
- Revenue by City

## Returns Dashboard

- Return Trends
- Return Reasons
- Return Analysis

---

# 🛠️ Technology Stack

| Tool | Usage |
|--------|---------|
| Power BI Desktop | Data Modeling |
| Power Query | Data Transformation |
| DAX | Calculations |
| Excel | Data Source |
| Star Schema | Data Warehouse Design |

---

# 📂 Project Structure

```text
Sales-Analytics-Project/
│
├── Customer_Dim.xlsx
├── Product_Dim.xlsx
├── Region_Dim.xlsx
├── Date_Dim.xlsx
├── Sales_Fact.xlsx
├── Returns_Fact.xlsx
│
├── Data Modeler - Building a Normalized Star Schema Data Model.pbix
│
└── README.md
```

---

# 🚀 Key Achievements

✔ Designed Enterprise-Level Star Schema

✔ Built Scalable Data Warehouse Architecture

✔ Implemented Power BI Data Model

✔ Created Optimized Relationships

✔ Enabled Advanced Business Analytics

✔ Improved Reporting Performance

✔ Developed KPI-Driven Insights

---

# 📷 Project Preview

Add Power BI Dashboard Screenshots Here

```text
assets/
├── Dashboard-Overview.png
├── Sales-Dashboard.png
├── Customer-Dashboard.png
└── Product-Dashboard.png
```

---

# 📬 Contact

### Developer

**Power BI Data Analyst**

- Data Modeling
- Business Intelligence
- Data Warehousing
- Power BI Development

---

## ⭐ If you found this project useful, don't forget to star the repository!
