# 🧮 SQL EDA & Data Transformation – Churn Analysis

This documentation is created to help users **understand the logic and flow of the `Exploratory Data Analysis.sql` queries**, which prepares telecom churn data for modeling and dashboarding. It outlines the **SQL Server** workflow for data loading, exploration, cleaning, feature engineering, and view creation.

## 📁 Script: `Exploratory Data Analysis.sql`

## 🔍 Key Steps

### 1️⃣ Data Loading
- Created a database: `db_Churn`
- Loaded raw data into a staging table: `stg_Churn`

### 2️⃣ Exploratory Data Analysis (EDA)
- Profiled key attributes: `Gender`, `Contract`, `Customer_Status`, `State`
- Calculated churn distributions and revenue breakdowns
- Identified distinct values for fields like `Internet_Type`

![sql1](https://github.com/user-attachments/assets/eab76b7b-2f42-4544-a45d-f5a02359364b)

### 3️⃣ NULL Value Handling
- Used `CASE`, `ISNULL`, and default fallbacks to clean missing data
- Replaced unknowns with values like `'None'`, `'No'`, or `'Others'`

![sql3](https://github.com/user-attachments/assets/f5dd7771-b1f2-4aba-9870-f8d32bb21056)

### 4️⃣ Feature Engineering & Table Creation
- Created `prod_Churn` table with enriched, clean fields
- Standardized values for service usage and churn-related columns

![sql2](https://github.com/user-attachments/assets/e69619c7-ca6d-4230-a2b9-546fb87db507)

### 5️⃣ SQL View Creation
- `vw_ChurnData`: Filters for `Churned` and `Stayed` customers  
- `vw_JoinData`: Focuses on customers with status = `Joined`

![Screenshot 2025-06-16 125438](https://github.com/user-attachments/assets/e068b03b-6ab7-4556-98fb-4d2f44553135)

## 📊 Output Table

The cleaned dataset (`prod_Churn`) was used in both:
- **Churn prediction modeling in Python**
- **Dashboard visualization in Power BI**

