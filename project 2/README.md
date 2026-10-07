# 🏨 Hotel Booking Analytics

### Turning Hotel Booking Data into Business Insights

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)](https://pandas.pydata.org/)
[![SQL](https://img.shields.io/badge/SQL-SQLite-003B57?logo=sqlite)](https://www.sqlite.org/)
[![Excel](https://img.shields.io/badge/Excel-Analytics-217346?logo=microsoftexcel)](https://www.microsoft.com/microsoft-365/excel)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi)](https://powerbi.microsoft.com/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)](https://jupyter.org/)

---

## 📌 Project Overview

This project analyzes **50,000+ hotel booking records** to understand hotel performance, customer behavior, booking patterns, revenue, occupancy, and cancellations.

The project follows an end-to-end **Data Analytics workflow**, starting from raw data cleaning and exploratory analysis and ending with SQL-based business analysis, Excel reporting, and an interactive Power BI dashboard.

> **Goal:** Transform raw hotel booking data into clear, actionable business insights.

---

## 🎯 Business Objectives

The analysis focuses on answering key business questions:

* How is hotel revenue performing over time?
* Which hotel types generate more bookings and revenue?
* What are the monthly and seasonal booking trends?
* What is the cancellation rate?
* Which customer segments contribute the most bookings?
* Which market segments generate higher revenue?
* What is the average length of stay?
* Which booking channels are most frequently used?
* Which room types have the highest demand?
* Which countries contribute the most bookings?

---

# 🧰 Tech Stack

| Technology              | Purpose                              |
| ----------------------- | ------------------------------------ |
| 🐍 **Python**           | Data cleaning & exploratory analysis |
| 🐼 **Pandas**           | Data manipulation                    |
| 🔢 **NumPy**            | Numerical operations                 |
| 📊 **Matplotlib**       | Data visualization                   |
| 📈 **Seaborn**          | Statistical visualization            |
| 🗄️ **SQLite / SQL**    | Business queries & analysis          |
| 📗 **Excel**            | KPI analysis & reporting             |
| 📊 **Power BI**         | Interactive dashboard                |
| 📓 **Jupyter Notebook** | Analysis environment                 |
| 🔧 **Git & GitHub**     | Version control                      |

---

# 🔄 End-to-End Analytics Workflow

```text
                    RAW DATA
                       │
                       ▼
              ┌─────────────────┐
              │  Data Cleaning  │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Data Preparation│
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │       EDA       │
              │ Python + Pandas │
              └────────┬────────┘
                       │
            ┌──────────┴──────────┐
            ▼                     ▼
      ┌───────────┐        ┌────────────┐
      │    SQL    │        │   Excel    │
      │ Analysis  │        │   KPIs     │
      └─────┬─────┘        └──────┬─────┘
            │                     │
            └──────────┬──────────┘
                       ▼
              ┌─────────────────┐
              │    Power BI     │
              │   Dashboard     │
              └────────┬────────┘
                       │
                       ▼
                BUSINESS INSIGHTS
```

---

# 🧹 1. Data Cleaning & Preparation

Python and Pandas were used to prepare the raw dataset for analysis.

### Data preparation activities

* Identified missing values
* Handled inconsistent records
* Removed duplicate records where required
* Converted columns to appropriate data types
* Created calculated fields
* Prepared date-related columns
* Checked data quality and consistency
* Prepared analytical datasets for SQL and Power BI

### Example

```python
import pandas as pd
import numpy as np

df = pd.read_csv("hotel_booking.csv")

# Check dataset
print(df.shape)
print(df.info())

# Missing values
print(df.isnull().sum())

# Duplicate records
print(df.duplicated().sum())
```

---

# 🔍 2. Exploratory Data Analysis

Exploratory analysis was performed using **Pandas, Matplotlib and Seaborn**.

### Analysis Areas

**Booking Analysis**

* Total bookings
* Monthly booking trends
* Booking distribution
* Hotel-wise booking performance

**Revenue Analysis**

* Revenue trends
* Revenue by hotel type
* Revenue by market segment
* Average Daily Rate

**Customer Analysis**

* Customer types
* Guest distribution
* Repeat/segment behavior
* Geographic distribution

**Cancellation Analysis**

* Cancellation rate
* Cancellation by market segment
* Cancellation by hotel type
* Cancellation trends

---

# 🗄️ 3. SQL Business Analysis

SQLite was used to perform structured business analysis.

### Example Business Questions

```sql
-- Total number of bookings
SELECT COUNT(*) AS total_bookings
FROM hotel_bookings;
```

```sql
-- Bookings by hotel type
SELECT
    hotel,
    COUNT(*) AS total_bookings
FROM hotel_bookings
GROUP BY hotel
ORDER BY total_bookings DESC;
```

```sql
-- Monthly booking analysis
SELECT
    arrival_date_year,
    arrival_date_month,
    COUNT(*) AS total_bookings
FROM hotel_bookings
GROUP BY
    arrival_date_year,
    arrival_date_mont
```
