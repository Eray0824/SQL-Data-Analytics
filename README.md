# SQL Data Analytics - End-to-End Analysis (EDA & Advanced Analytics)

## Overview and Project Goals

<!-- Placeholder for a conceptual diagram of the full SQL analytics workflow -->
<!-- Example: ![SQL Analytics Workflow](https://github.com/your-username/your-repo/assets/your-image-id/sql_analytics_workflow.png ) -->

This project showcases a comprehensive approach to data analytics using SQL, covering both Exploratory Data Analysis (EDA) and Advanced Analytics. The primary goal is to transform raw data into actionable business intelligence, enabling informed decision-making by systematically uncovering trends, measuring performance, segmenting data, and building robust reports directly within a SQL environment.

### Key Concepts & Techniques

-   **Exploratory Data Analysis (EDA)**: Understanding data structure, identifying dimensions vs. measures, and profiling data.
-   **Advanced Analytics**: Tracking changes over time, cumulative analysis, performance comparison, part-to-whole analysis, and data segmentation.
-   **SQL Mastery**: Extensive use of `GROUP BY`, aggregate functions (`SUM`, `AVG`, `COUNT`), `DISTINCT`, `DATEDIFF`, `MIN`/`MAX`, `CASE WHEN`, CTEs (Common Table Expressions), Window Functions (`SUM() OVER`, `LAG()`, `ROW_NUMBER()`), and `UNION ALL`.
-   **Report Generation**: Creating consolidated, user-friendly views for key stakeholders.

---

## What was done: A Two-Part SQL Analysis

This project systematically performed a two-part data analysis using SQL:

### Part 1: Exploratory Data Analysis (EDA)

-   **Database Exploration**: Examined database schema, tables (Customers, Products, Sales), and columns using `INFORMATION_SCHEMA` views.
-   **Dimensions Exploration**: Identified unique values and granularity of dimensions like `Country`, `Gender`, `Category`, and `Subcategory`.
-   **Date Exploration**: Determined data time boundaries (`MIN`/`MAX` dates) and calculated time spans (`DATEDIFF`).
-   **Measures Exploration**: Calculated key business metrics (`Total Sales`, `Total Quantity`, `Average Price`, `Total Orders` using `COUNT(DISTINCT)`) and consolidated them into a single overview report.
-   **Magnitude Analysis**: Compared measures across dimensions (e.g., `Customers by Country`, `Revenue by Category`) using `GROUP BY`.
-   **Ranking Analysis**: Identified top/worst performers (e.g., `Top 5 Products by Revenue`, `Top Customers`) using `ORDER BY` and `TOP` (or `ROW_NUMBER()`).

### Part 2: Advanced Data Analytics

-   **Changes Over Time Analysis**: Analyzed sales performance over time (yearly, monthly) using `YEAR()`, `MONTH()`, and `DATE_TRUNC()`, identifying trends and seasonality.
-   **Cumulative Analysis**: Calculated running totals of sales and moving averages using `SUM() OVER` and `AVG() OVER` window functions to track business growth.
-   **Performance Analysis**: Compared current sales performance against targets (e.g., average sales, previous year's sales) using `LAG()` and `AVG() OVER (PARTITION BY ...)`, highlighting performance deviations.
-   **Part-to-Whole Analysis**: Determined the contribution of individual categories to overall sales (e.g., `Category Sales % of Total`) using `SUM() OVER ()` for overall totals, identifying dominant categories.
-   **Data Segmentation**: Grouped data into new categories based on measure ranges using `CASE WHEN` statements, creating segments like "Product Cost Ranges" and "Customer VIP/Regular/New".
-   **Report Generation (Customer & Product Reports)**: Built two comprehensive, multi-step reports (Customer Report, Product Report) as SQL views, consolidating detailed information, aggregations, derived KPIs (e.g., Recency, Average Order Value, Average Monthly Spend), and segmentations for easy consumption by other data users.

---

## Key Outcomes

This project demonstrates a complete analytical workflow in SQL, from understanding raw data to delivering actionable, consolidated reports. It highlights the power of SQL in performing complex data transformations, deriving new insights, and preparing data for various business intelligence needs. The resulting reports provide a 360-degree view of customer and product performance, enabling strategic decision-making.

---

## Project Materials

-   **SQL Scripts**: All SQL queries used for EDA and Advanced Analytics are available in this repository, organized by analysis type.
-   **Dataset**: The sample dataset (Customers, Products, Sales tables) is provided.
