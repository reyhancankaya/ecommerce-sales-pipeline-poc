# E-Commerce Sales & Analytics Pipeline (PoC)
This repository demonstrates an end-to-end data analytics pipeline, where raw e-commerce data is processed and analyzed entirely within a **Python-native environment** and visualized in **Tableau**.

## Project Overview
This project serves as a **Proof of Concept (PoC)** to showcase a seamless data workflow. Instead of traditional SQL layers, all complex analytical transformations—including time-series shifting and aggregations—were performed using **Python's Pandas library**, demonstrating high-level data manipulation skills.

## Tech Stack
* **Data Engineering & Analytics:** Python (Pandas)
* **Visualization:** Tableau Desktop

## Analytical Approach & Logic (Python Implementation)
The project replaces traditional SQL queries with advanced Python logic:
* **Retention Logic:** Used Pandas `.shift()` and `.groupby()` functions to calculate `Last Order Value`, mimicking the SQL `LAG()` function.
* **Operational Metrics:** Calculated Average Order Value (AOV) and total transaction counts through custom Python aggregations.
* **Category Analysis:** Leveraged Pandas pivot tables to prepare data for categorical revenue distribution.

## 🔍Data Validation & Quality Assurance (QA)
To ensure the integrity of the Python-to-Tableau pipeline, a rigorous validation process was implemented:
* **Verified Sample Validation:** The pipeline is validated using 5 core transactions. This small, controlled sample allows for a transparent, step-by-step verification of the Python-native logic.
* **Handled Discontinuities:** In Python, the first transaction for any customer correctly results in a `NaN/Null` value for the 'Last Order Value' column. This confirms the chronological accuracy of the `.shift()` logic.

## 📂 Repository Contents
* `notebook.ipynb`: The core engine containing Python ETL, Pandas-based analytics, and data cleaning.
* `ECommerce_Data_Final.xlsx`: The final output of the Python pipeline, ready for Tableau.
* `Executive_Sales_Dashboard_PoC.twbx`: The production-ready Tableau Dashboard.
