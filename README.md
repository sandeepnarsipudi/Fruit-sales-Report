

🍎 Fruit Sales Analysis Dashboard (Power BI)

Dashboard Link: https://app.powerbi.com/view?r=eyJrIjoiYTJlZjk2MzEtZTIyZS00ZWViLWJjZGUtMzA4MjkyNWZlMTU2IiwidCI6IjIzODk2NDkwLTdlNzMtNGQ1Zi1hZjQ5LTBmMjUwMzQ5NWQ3NSJ9&pageName=e5b3f1d73af6a0940b6d

Dashboard Overview

This Power BI dashboard provides a comprehensive analysis of **fruit sales performance** using data sourced from **OneDrive** and developed entirely in **Power BI Service**. The report is designed to help users monitor sales trends, compare performance across customers and stores, and analyze business performance over time.

The dashboard consists of **three interactive report pages**, each focused on a specific analytical objective:

* **Fruit Sales Report**
* **Sum / Average Sales**
* **Sales Analysis**

---

Problem Statement

Sales teams often require flexible views to analyze both **total sales performance** and **average sales trends** without navigating across multiple pages. This project addresses that need by combining **dynamic bookmarks**, **interactive slicers**, and **time intelligence calculations** into a single, user-friendly Power BI solution.

Using this dashboard, users can:

* Track total and average fruit sales
* Analyze sales trends by date, customer, store, and product
* View YTD and running total sales
* Identify top-performing stores and customers

---

Tools & Technologies Used

* **Power BI Service**
* **OneDrive (Data Source)**
* **Power Query**
* **DAX (Data Analysis Expressions)**
* **Bookmarks & Slicers**
* **Custom Background Images**

---

Steps Followed

Data Loading & Preparation

* **Step 1:** Sales data was connected to Power BI Service using **OneDrive** as the data source.
* **Step 2:** Power Query was used to clean, format, and validate the data.
* **Step 3:** Relationships were created between fact and dimension tables to support accurate analysis.

Report Design

* Step 4:** Created three report pages:

  * **Fruit Sales Report** – Overall sales trends and slicers
  * **Sum / Average Sales** – Bookmark-based toggle between sum and average views
  * **Sales Analysis** – Detailed insights including YTD and running totals
* **Step 5:** Applied custom background images to enhance visual appeal and readability.
* **Step 6:** Added slicers for Customer, Brand, Category, Product, Store, Location, and Date.

Interactivity

* **Step 7:** Implemented **Bookmarks** to switch between **Sum of Sales** and **Average Sales** on the same page.
Sum of sales:
<img width="1746" height="788" alt="Screenshot 2026-02-08 172119" src="https://github.com/user-attachments/assets/e2bca2c5-e243-41a3-8768-765eb6b13ae5" />

Total sales:
<img width="1762" height="780" alt="Screenshot 2026-02-08 172149" src="https://github.com/user-attachments/assets/afbeca2b-e63c-4c6c-8657-2257b7413c3c" />

* **Step 8:** Applied page-level and visual-level filters for focused analysis.

---

Data Model

* Fact table: **Sales**
* Dimension tables: **Customer, Product, Brand, Store, Date**

---

DAX Measures 

Core Sales Measures

```DAX
Total Sales =
SUM ( Sales[Sales Amount] )
```

```DAX
Average Sales =
AVERAGE ( Sales[Sales Amount] )
```

---

Time Intelligence Measures

```DAX
Running Total Sales =
CALCULATE (
    [Total Sales],
    FILTER (
        ALL ( 'Date'[Date] ),
        'Date'[Date] <= MAX ( 'Date'[Date] )
    )
)
```

```DAX
Total YTD Sales =
TOTALYTD (
    [Total Sales],
    'Date'[Date]
)
```
---

Key Insights

* Sales trends can be analyzed dynamically using date filters and slicers.
* Bookmark-based views allow users to compare **total sales vs average sales** without changing pages.
* Running total and YTD measures provide clear visibility into business growth.
* Store and customer-level analysis helps identify high-performing segments.


---

Conclusion

This Fruit Sales Analysis Dashboard demonstrates effective use of **Power BI Service**, **OneDrive integration**, and **advanced interactivity using bookmarks**. The project highlights strong skills in data modeling, DAX, and user-focused dashboard design, making it a valuable portfolio project for Power BI and Data Analyst roles.

