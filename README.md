# Retail-Sales-Data-Analysis
End-to-end retail sales data cleaning and analysis project using Excel and Power Query

## 🚀 Project Overview
A comprehensive data analysis project focusing on transforming raw, unstructured retail sales data into a clean, reliable, and analytical-ready data model. This project demonstrates end-to-end data processing using **Microsoft Excel** and **Power Query (ETL)**, followed by advanced exploratory data analysis and interactive Pivot Table reporting.

---

## 🛠️ Tools & Technologies Used
- **Microsoft Excel:** Data modeling, Pivot Tables, and Dashboard calculations.
- **Power Query (M Code & ETL):** Automated data extraction, transformation, and cleaning pipeline.
- **Data Analysis & Feature Engineering:** Creating calculated columns (COGS, Discount Value, Shipping Duration).

---

## 🧹 Data Cleaning & ETL Process (Power Query)
The raw dataset contained several structural and formatting anomalies. The following automated ETL steps were built inside Power Query to ensure reproducibility and data integrity:

1. **Robust Data Source Connection:**
   * Established a dynamic connection to the source dataset ensuring smooth data refreshing without manual intervention.
2. **Date Formatting & Type Correction:**
   * *Issue:* `Ship Date` and `Order Date` columns were improperly typed as whole numbers, displaying internal Excel serial numbers (e.g., `42685`).
   * *Solution:* Explicitly transformed data types in the `Changed Type` step to strict date formats (`type date`) to enable accurate time-series analysis.
   
*(Here is a snapshot showing the date cleaning and raw format correction)*:
![Date Cleaning Process](Screenshot%202026-10-12%20200644.png)
![Date Cleaning Process](Screenshot%202026-10-12%20200548.png)

3. **Geographical & Text Restructuring:**
   * Cleaned and restructured location-based strings to separate geographical components correctly, ensuring accurate regional aggregation.
  *(Here is a snapshot showing the date cleaning of location)*:
![Date Cleaning Process](Screenshot%202026-10-12%20201722.png)
![Date Cleaning Process](Screenshot%202026-10-12%20201754.png)
4. **Error Handling & Null Management:**
   * Audited rows for missing values and structural errors to prevent downstream calculation failures.

---

## ⚙️ Feature Engineering & Custom Columns
Using Power Query custom column transformations, key business metrics were engineered to deepen the analytical scope:
- **`Discount Value`:** Calculated exact monetary discount impact on orders (`Sales * Discount`).
- **`COGS` (Cost of Goods Sold):** Derived accurate cost metrics based on sales and profit margins.
- **`Duration of Ship`:** Computed order fulfillment time by calculating the exact difference between `Ship Date` and `Order Date`.

*(Here is a snapshot showing the engineered custom columns)*:
![Custom Columns](Screenshot%202026-10-11%20023648.png)

---

## 💡 Key Business Insights & Pivot Table Analysis
The cleaned dataset (`Orders`, `Returns`, and `People` tables) was modelled to answer critical business questions through advanced Pivot Tables:

- **Top Customers:** Identified top customers by total sales volume and order frequency.
- **Geographical Performance:** Highlighted top-performing cities (e.g., New York City, Los Angeles) generating peak revenue percentages.
- **Product Category Breakdown:** Analyzed revenue and profit margins across categories.

*(Here is a snapshot of the Pivot Table analysis and insights)*:

![Pivot Tables Analysis](Screenshot%202026-10-12%20202229.png)

![Dashboard](Screenshot%202026-10-12%20202153.png)
---

## 📁 Repository Structure
```text
├── 1- Raw Data - Business Data Set.xlsx     # Original uncleaned dataset
├── Power Query and Pivot table.xlsx         # Final cleaned model with Pivot Tables
└── README.md                                # Project documentation
