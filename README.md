# 🛒 SuperMarket Analytics Dashboard (Power BI)

This project delivers an end-to-end Power BI data modeling and visualization solution for a fictional supermarket chain. It covers everything from data preparation, modeling, DAX calculations, to creating an interactive, business-ready dashboard.

---

## 📦 Data Sources

The project uses the following datasets (CSV format):

- Customers
- Products
- Stores
- Regions
- Calendar
- Return Data
- Transactions (1997 & 1998)

---

## 🛠️ Tools & Technologies

- **Power BI Desktop**
- **DAX** (Data Analysis Expressions)
- **Power Query (M Language)**

---

## 🚧 Project Breakdown

### 📌 Part 1: Data Connection & Transformation
- Connected and cleaned data from multiple CSV files.
- Used Power Query Editor to:
  - Promote headers
  - Ensure correct data types
  - Create calculated and conditional columns (e.g., `full_name`, `birth_year`, `has_children`, `discount_price`)
  - Grouped data for aggregations (e.g., average retail price by brand)
  - Handled nulls and merged files from folders

---

### 📌 Part 2: Data Modeling
- Established relationships:
  - One-to-many joins between `Transaction_Data` and dimension tables (`Customers`, `Products`, `Stores`, `Calendar`)
  - Snowflake schema using `Regions`
- Confirmed correct cardinality, filter direction, and key consistency
- Applied semantic formatting and geographic categorization

---

### 📌 Part 3: DAX Calculations
#### ➕ Calculated Columns:
- `Weekend`, `End of Month` (Calendar)
- `Current Age`, `Priority`, `Short_Country` (Customers)
- `Price_Tier` (Products)
- `Years_Since_Remodel` (Stores)

#### 📏 Measures Created:
- `Quantity Sold`, `Quantity Returned`
- `Total Transactions`, `Total Returns`, `Return Rate`
- `Weekend Transactions`, `% Weekend Transactions`
- `Total Revenue`, `Total Cost`, `Total Profit`, `Profit Margin`
- `Unique Products`, `YTD Revenue`, `60-Day Revenue`
- Last month KPIs: `Transactions`, `Revenue`, `Profit`, `Returns`
- `Revenue Target` (5% increase over previous month)

---

### 📌 Part 4: Dashboard Design

#### ✅ Final Report Page: **Topline Performance**
- **Matrix Table:** Total Transactions, Profit, Margin, and Return Rate by Product Brand (Top 30 with conditional formatting)
- **KPI Cards:** Current Month Transactions, Profit, Returns (with comparisons vs. last month)
- **Map Visual:** Transactions by store city with slicers for country
- **Treemap:** Transaction drilldown by Country > State > City
- **Column Chart:** Weekly Revenue Trend for 1998
- **Gauge Chart:** Revenue vs. Target comparison
- **Custom Interactions:** Controlled visual cross-filtering for clarity

---

## 📈 Key Insights
- Identified top-performing product brands by transaction volume and profitability.
- Tracked return rates to identify product categories needing quality review.
- Compared revenue trends against targets to monitor sales performance.
- Uncovered high-engagement weekends and peak regions for marketing focus.

---
