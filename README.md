# 📊 Telecom Customer Churn Analysis 

### [Customer Churn Dashboard: Link](https://app.powerbi.com/view?r=eyJrIjoiODJhYjA3MDEtY2JjZi00OGQ5LWI5Y2YtNmI1Zjg0ZTdhMWE2IiwidCI6ImI2NDE3Y2QwLTFmNzMtNDQ3MS05YTM5LTIwOTUzODIyYTM0YSIsImMiOjN9)

## Project Overview
Churn analysis helps businesses **understand why customers leave** and **identify patterns behind customer attrition**. In the telecom industry, customer churn is a critical challenge that impacts both **revenue** and **growth stability**. This project analyzes customer churn for a fictional telecom company, **INTELEVO Networks**, using a data-driven approach. It spans across SQL-based EDA and transformations, churn prediction using Random Forest in Python, and Power BI dashboards for business insights.


## Objective
To reduce customer churn by understanding key churn drivers, identifying high-risk segments and empowering business decisions through data storytelling.

## Dataset Source
This project uses the [Telecom Customer Churn Dataset](https://www.kaggle.com/datasets/shilongzhuang/telecom-customer-churn-by-maven-analytics), available on Kaggle. The dataset contains customer-level information including demographics, services used, contract details, and churn status. It has been modified and extended for modeling and visualization purposes throughout the project pipeline.

## Project Workflow
This project follows a structured, end-to-end data analytics workflow to identify and mitigate customer churn at INTELEVO Networks. The process integrates data engineering, predictive analytics, and business intelligence to generate actionable insights.

![image-2](https://github.com/user-attachments/assets/b0db173c-c112-4194-a10d-4c4172ebe02d)


- SQL Server – Loaded, cleaned, performed exploratory data analysis and modeled raw telecom data to create an analytics-ready dataset.
- Python – Built a Random Forest model to predict customer churn and identify key churn drivers.
- Excel – Exported cleaned data and model predictions to Excel for easy Power BI integration.
- Power BI – Designed interactive dashboards to visualize churn patterns, customer segments, and risk profiles.

## 🛠 Tools & Technologies
- **SQL Server Management Studio (SSMS)** – ETL, Exploratory Data Analysis
- **Python (Scikit-learn)** – Predictive modeling using Random Forest
- **Power BI** – Data storytelling through dashboards
- **Excel** – Preliminary data exploration

## 📂 Files in This Repository

```plaintext
telecom-churn-analysis/
│
├── 📁 data/                             # Cleaned and processed datasets used in modeling and visualization
│   ├── Final_Customer_Data_Canadian_Cities.csv   # Final dataset exported from SQL
│   ├── Predicted_Churners.csv                     # Churn predictions from Python model
│   └── Production_Data.xlsx                       # Enhanced dataset for Power BI (SQL + Python merged)
│
├── 📁 sql/                              # SQL scripts for data extraction, transformation, and EDA
│   └── Exploratory Data Analysis.sql              # SQL queries for loading, cleaning, and modeling data
│
├── 📁 python/                           # Python notebook for churn prediction using machine learning
│   └── Churn_Prediction.ipynb                   # Random Forest model implementation with prediction outputs
│
├── 📁 docs/                             # Project documentation and detailed process explanations
│   ├── Readme_SQL_EDA.md                         # Describes SQL-based data processing and transformation
│   └── Readme_Python_ML.md                       # Documents machine learning model pipeline and predictions
│
├── README.md                          # Main project overview, Dashboard Public Link, insights, and dashboard usage

```

## Key Business Insights

### 📄 Page 1: Overview
- **Churned Customers**: **1,732 customers** left INTELEVO Networks, resulting in a **revenue loss of $3.41 million**
- **Churn Rate** stands at **26.99%**, with an **Average Revenue Per User (ARPU)** of **$174.94/month**
- **Top churn reasons**: Competition (761 cases), Attitude, Price sensitivity, and Dissatisfaction
- The city of **Kelowna** had the **highest churn rate at 57.19%**
- **Deal 5** has the highest churn rate of **53.79%** generating least revenue.
  
![image-4](https://github.com/user-attachments/assets/2b9e5a57-b3b9-47d0-bcb9-54304f1f5cf5)


### 📄 Page 2: Demographics & Services
- Churn was higher among **male customers** (64% of churned base).
- **Month-to-month contract** users had the highest churn rate (**46.53%**), while **2-year contract** holders had the lowest (**2.73%**).
- Customers **not subscribed to Premium Support, Online Backup, or Online Security** were more likely to churn.
- **Fiber Optic** users churned the most among internet types (**41.10%**)
- Those paying by **Mailed Check** showed a churn rate of **37.82%**

![Screenshot 2025-06-16 113011](https://github.com/user-attachments/assets/75fd97b8-a0c7-4b84-98d0-29ee9fb09a5b)

### 📄 Page 3: Churn Predictions
- The **Random Forest model** predicted **385 customers at high risk of churn**
- Most at-risk customers use **month-to-month contracts** (358 out of 385)
- Cities with the highest concentration of predicted churners: **Mississauga**, **Toronto**, and **Calgary**
- At-risk profiles are mainly **aged 35–50**.

![image-3](https://github.com/user-attachments/assets/c842a4e6-609b-4600-b555-b4be1283fc6b)


## Dashboard Usage

Each page of the dashboard is tailored to specific business users within INTELEVO Networks to support data-driven decisions:

### Overview – For Executives & Senior Management
- Quickly assess overall business performance and churn health
- Monitor KPIs like **churn rate**, **ARPU**, and **revenue impact**
- Understand **top-level reasons** for customer loss and city-level patterns

### Demographics & Services – For Marketing & Customer Retention Teams
- Analyze **who is churning** based on demographics and service usage
- Identify high-risk customer groups (e.g., **age**, **gender**, **contract type**, **internet plan**)
- Support **targeted retention campaigns** and product improvement strategies

### Churn Predictions – For Data Analysts & Customer Success Teams
- Access **machine learning predictions** of customers most likely to churn
- Focus efforts on **high-risk, high-value customers** before they leave
- Use filters to segment and prioritize outreach based on **location**, **tenure**, and **payment behavior**

---
