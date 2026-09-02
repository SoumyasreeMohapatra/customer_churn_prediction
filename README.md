# Churn Analysis and Customer Intelligence 📊

This project performs a comprehensive analysis of customer churn using Python, Pandas, and SQLite. By analyzing customer demographics, subscription details, and support tickets, this notebook identifies key drivers of churn and calculates vital business metrics to help improve customer retention.

## 🚀 Key Features & Analysis

*   **Data Pipeline Integration:** Imports raw data from Excel (`customer_churn_data_raw.xlsx`), stores it locally in an SQLite database (`customer_churn.db`), and queries it into Pandas DataFrames for analysis.
*   **Data Cleaning & Feature Engineering:** Handles missing values, standardizes data types, and creates new features like `churn_flag`, `tenure_days`, and `churn_risk` profiles.
*   **Key Performance Indicators (KPIs) Calculated:**
    *   **Churn Rate:** 28.57%
    *   **Retention Rate:** 71.43%
    *   **Average Revenue Per User (ARPU):** $18.85
    *   **Revenue at Risk:** Calculated lost revenue from churned users.
    *   **Escalation vs. Churn Correlation:** Strong correlation (0.77) identified.
*   **Visualizations:** Includes comprehensive Matplotlib and Seaborn charts, such as Monthly Churn Trends, Churn Rate by Plan Type/State, and Correlation Heatmaps.

## 🛠️ Technologies Used

*   **Python 3**
*   **Pandas & NumPy:** For data manipulation and numerical calculations.
*   **SQLite3:** For lightweight, local database management and SQL querying within Python.
*   **Matplotlib & Seaborn:** For data visualization and exploratory data analysis (EDA).
*   **Jupyter Notebook:** Interactive development environment.

## 📂 Dataset Overview

The analysis merges three primary data tables:
1.  **Customers:** Contains demographic info (`customerid`, `name`, `country`, `state`, `gender`, `dob`).
2.  **Subscriptions:** Contains billing and plan details (`subscription_start_date`, `plan_type`, `contract_type`, `monthly_charges`, `churn_score`, `cancellation_date`).
3.  **Support:** Contains customer service interactions (`complaint_date`, `escalations`, `csat_score`).

## 💻 How to Run the Project

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/churn-analysis.git](https://github.com/yourusername/churn-analysis.git)
   cd churn-analysis
   Install required dependencies:
Ensure you have Python installed, then run:

Bash
pip install pandas numpy matplotlib seaborn jupyterlab openpyxl
Run the Jupyter Notebook:

Bash
jupyter notebook churn_analysis.ipynb
Note on Data: If you don't have the pre-built customer_churn.db, the notebook includes a script in the first section to automatically generate it from the provided customer_churn_data_raw.xlsx file.

📈 Key Insights
Customers on the Basic plan have a significantly higher churn rate (60%) compared to Premium (14.2%) and Standard (22.2%) plans.

There is a high correlation between customer support escalations and eventual churn.

Created by Soumyasree Mohapatra