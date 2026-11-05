# 📊 Retail Operations & Financial MIS Dashboard (Power BI)

A portfolio-ready, executive-level Business Intelligence project built to track high-level financial performance, monthly revenue trends, and product-level profitability for a global retail distribution company.

---

## 🚀 Project Overview
In modern MIS and Data Analyst roles, stakeholders need immediate visibility into core financial health without wading through clutter. This dashboard is designed with a strict, minimalist scope to answer four vital business questions at a glance:
1. **What is our total revenue generation?**
2. **What is our overall profit margin health?**
3. **How does revenue trend across months?**
4. **Which products are driving the most revenue?**

---

## 🛠️ Data Architecture & Star Schema
The project uses a relational **Star Schema** architecture built inside Power BI. Data was cleaned, structured, and modeled to ensure optimal query performance and accurate time intelligence.

* **Fact Table (`Sales`):** Contains transactional records including `OrderID`, `OrderDate`, `CustomerID`, `ProductID`, `Quantity`, `UnitCost`, `UnitPrice`, and `Region`.
* **Dimension Table (`Products`):** Houses product metadata and categories.
* **Dimension Table (`Customers`):** Stores customer details.
* **Dimension Table (`CalendarTable`):** A generated DAX calendar table linked to `Sales[OrderDate]` to unlock time-series analysis.

*Relationship Model:* 1-to-Many (*) relationships established from Dimension tables (Products, Customers, CalendarTable) down to the Fact table (Sales).

---

## 📐 Core DAX Measures
The analytical engine relies on clean, optimized DAX formulas:

```dax
-- Total Revenue Calculation
Total Revenue = SUMX(Sales, Sales[Quantity] * Sales[UnitPrice])

-- Total Cost Calculation
Total Cost = SUMX(Sales, Sales[Quantity] * Sales[UnitCost])

-- Gross Profit Calculation
Gross Profit = [Total Revenue] - [Total Cost]

-- Profit Margin % Calculation
Profit Margin % = DIVIDE([Gross Profit], [Total Revenue], 0)
```
---


## 📈 Dashboard Layout & Features
The report follows a modern executive dark-theme aesthetic (#121212 background with #1E1E1E containers and vibrant accent lines):

Top KPI Cards: Instant visibility into Total Revenue and Profit Margin %.

Revenue Over Month (Line Chart): Tracks time-series performance across the calendar year.

Revenue by Product (Bar Chart): Highlights top-performing products driving commercial success.

## 🖼️ Dashboard Preview
Tip: Place your exported dashboard screenshot inside a folder named screenshots/ in your repository and name it executive-summary.png.

## 💼 Skills Demonstrated
Data Modeling: Star Schema design, 1-to-many relationship mapping, and handling granular data splits.

DAX Mastery: Calculated measures, iterative row context (SUMX), and safe division handling (DIVIDE).

MIS Best Practices: Creating focused, executive-ready dashboards with high signal-to-noise ratios.

Here is a clean, professional, and ready-to-copy `README.md` template tailored specifically for your focused Power BI MIS project. You can copy this directly into your GitHub repository!

---

```markdown
# 📊 Retail Operations & Financial MIS Dashboard (Power BI)

A portfolio-ready, executive-level Business Intelligence project built to track high-level financial performance, monthly revenue trends, and product-level profitability for a global retail distribution company.

---

## 🚀 Project Overview
In modern MIS and Data Analyst roles, stakeholders need immediate visibility into core financial health without wading through clutter. This dashboard is designed with a strict, minimalist scope to answer four vital business questions at a glance:
1. **What is our total revenue generation?**
2. **What is our overall profit margin health?**
3. **How does revenue trend across months?**
4. **Which products are driving the most revenue?**

---

## 🛠️ Data Architecture & Star Schema
The project uses a relational **Star Schema** architecture built inside Power BI. Data was cleaned, structured, and modeled to ensure optimal query performance and accurate time intelligence.

* **Fact Table (`Sales`):** Contains transactional records including `OrderID`, `OrderDate`, `CustomerID`, `ProductID`, `Quantity`, `UnitCost`, `UnitPrice`, and `Region`.
* **Dimension Table (`Products`):** Houses product metadata and categories.
* **Dimension Table (`Customers`):** Stores customer details.
* **Dimension Table (`CalendarTable`):** A generated DAX calendar table linked to `Sales[OrderDate]` to unlock time-series analysis.

*Relationship Model:* 1-to-Many (*) relationships established from Dimension tables (Products, Customers, CalendarTable) down to the Fact table (Sales).

---

## 📐 Core DAX Measures
The analytical engine relies on clean, optimized DAX formulas:

```dax
-- Total Revenue Calculation
Total Revenue = SUMX(Sales, Sales[Quantity] * Sales[UnitPrice])

-- Total Cost Calculation
Total Cost = SUMX(Sales, Sales[Quantity] * Sales[UnitCost])

-- Gross Profit Calculation
Gross Profit = [Total Revenue] - [Total Cost]

-- Profit Margin % Calculation
Profit Margin % = DIVIDE([Gross Profit], [Total Revenue], 0)

```

---

## 📈 Dashboard Layout & Features

The report follows a modern executive dark-theme aesthetic (`#121212` background with `#1E1E1E` containers and vibrant accent lines):

* **Top KPI Cards:** Instant visibility into **Total Revenue** and **Profit Margin %**.
* **Revenue Over Month (Line Chart):** Tracks time-series performance across the calendar year.
* **Revenue by Product (Bar Chart):** Highlights top-performing products driving commercial success.

---

## 🖼️ Dashboard Preview

> *Tip: Place your exported dashboard screenshot inside a folder named `screenshots/` in your repository and name it `executive-summary.png`.*

---

## 💼 Skills Demonstrated

* **Data Modeling:** Star Schema design, 1-to-many relationship mapping, and handling granular data splits.
* **DAX Mastery:** Calculated measures, iterative row context (`SUMX`), and safe division handling (`DIVIDE`).
* **MIS Best Practices:** Creating focused, executive-ready dashboards with high signal-to-noise ratios.

```

