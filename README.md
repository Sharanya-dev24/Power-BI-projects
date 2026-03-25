#Retail Sales & Order Analytics Dashboard — Descriptive Summary (2003–2005)

> An end-to-end Power BI dashboard that surfaces descriptive statistics across 3 years and 10,000+ orders from a retail store, enabling quick insights into sales performance, order trends, and product behaviour.

##Overview

This project explores and summarizes retail sales data spanning **2003 to 2005** using descriptive statistics. Built entirely in Power BI — from data cleaning to dashboarding — it provides a structured view of orders, sales, customers, and products through an interactive, drill-through enabled dashboard.

## Dataset
- **Source:** [Kaggle]
- **Period Covered:** 2003, 2004, 2005
- **Total Orders:** ~10,000

### Tables & Relationships

| Table | Role | Key Column(s) |
|-------|------|---------------|
| **Orders** | Main / Fact table | `ORDERID`, `PRODUCTCODE` |
| **Sales** | Linked to Orders | `ORDERID` |
| **Customers** | Linked to Orders | `ORDERID` |
| **Products** | Linked to Orders | `PRODUCTCODE` |

> The **Orders** table is the central fact table, connecting to all other tables via `ORDERID` and `PRODUCTCODE`.

##Tech Stack

| Tool | Purpose |
|------|---------|
| **Microsoft Excel** | Quick data inspection and sanity checks |
| **Power BI Desktop** | Data cleaning, transformation, modelling, and dashboarding |


## Project Workflow

### 1.Data Cleaning *(Power Query)*
- Handled missing/null values
- Removed duplicate records
- Applied fill-down/fill-up where appropriate

### 2.Data Transformation *(Power Query)*
- Renamed columns for clarity and consistency
- Dropped unnecessary columns
- Merged and appended tables where needed
- Added calculated columns:
  - **Year**, **Quarter**, **Month**, **Day** — extracted from order date for time-based analysis

### 3.Data Modelling
- Established relationships across all four tables in Power BI's Model View
- Defined cardinality and cross-filter direction for accurate measure calculations

### 4.DAX Measures & Calculations

| Measure | Description |
|---------|-------------|
| `Total Sales` | Sum of all sales across the dataset |
| `Total Qty` | Total quantity of items ordered |
| `Average Sales` | Mean sales value per order |

- Created a **Summary Table** using DAX to consolidate key descriptive statistics (min, max, average, count, etc.)

### 5.Hierarchies
- Built date hierarchies in the **Orders** and **Sales** tables:
  - Year → Quarter → Month → Day

### 6.Visualizations & Dashboard Features
- **Drill-through** functionality to filter and explore stats by individual year (2003, 2004, 2005)
- *(visuals description  — visuals used, layout, key pages, etc.)*

## Dashboard Screenshots
Overall dashboard: ![Overview](https://github.com/Sharanya-dev24/Power-BI-projects/blob/main/Sales%20Descriptive%20dashboard%20overall.png) |

Dashboard view filtered on 2003 (2003, 2004 and 2005 screenshots are attached in file section): ![Drill-through-2003](https://github.com/Sharanya-dev24/Power-BI-projects/blob/main/Sales%20Descriptive%20dashboard%202003%20filtered.png) |


## ✨ Features & Highlights

> *(full walkthrough of the dashboard — visuals, insights, and design decisions.)*
