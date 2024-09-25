# 💳 Credit Card Financial Dashboard

Welcome to the **Credit Card Financial Dashboard** project! This project aims to provide real-time insights into credit card performance metrics, making it a comprehensive tool for stakeholders to monitor, analyze, and optimize credit card operations.

---

## 📝 Project Objective

The objective of this project is to develop an interactive and visually engaging dashboard that tracks **weekly credit card metrics**, enabling financial institutions to make informed decisions based on critical data. The project focuses on improving **operational efficiency** by providing insights into:

- Revenue trends
- Transaction analysis
- Customer behavior
- Card usage patterns

---

## 📊 Dashboard Features

The dashboard provides valuable insights through various performance indicators and breakdowns, such as:

- **Revenue and Interest Overview**: Real-time revenue (57M), interest earned (8M), transaction amounts (46M), and transaction counts (667.2K).
- **Customer Segmentation**: Data segmented by job roles, education, age group, and geography.
- **Revenue Breakdown**:
  - By card category (Blue, Silver, Gold, Platinum)
  - By customer demographic (age, gender, job)
  - By expenditure type (bills, travel, groceries, entertainment)
- **Transaction Trends**: Monitoring via swipe, chip, and online transaction types.
- **Top States**: Texas (TX), New York (NY), and California (CA) contribute significantly to revenue (68%).

The reports are split into:

1. **Credit Card Transaction Report**: Tracks key financial metrics such as total transactions, interest, and revenue distribution by various categories.
2. **Credit Card Customer Report**: Focuses on customer data, segmented by age group, gender, education level, and more, to analyze spending behavior and satisfaction.

---

## 🛠️ Technologies & Skills Used

This project leverages a range of technologies and analytical skills:

- **SQL**: For database creation and data manipulation.
- **Power BI**: For real-time dashboard visualizations and reports.
- **DAX Queries**: Used for advanced custom queries (e.g., grouping by Age, Income, Week-over-Week analysis).
- **MS Excel**: For additional data handling, preprocessing, and preliminary analysis.
- **Data Cleaning**: Cleaning and preparing raw data before importing it into SQL.
- **Exploratory Data Analysis (EDA)**: Performing in-depth analysis to uncover trends, correlations, and insights.
- **Data Modelling**: Structuring and linking customer and transaction data for seamless analysis.

---

## 🗃️ Data Modeling

Two main datasets were used:

1. **Credit Card Data (`cc_detail`)**: Includes key transactional data like credit limit, revolving balance, total transaction amount, chip usage, etc.
2. **Customer Data (`cust_detail`)**: Captures demographic information like age, gender, education level, income, job type, etc.

The project also involves importing CSV data into SQL and using **SQL queries** to ensure a smooth data pipeline between the database and Power BI.

---

## 📈 Project Insights

Here are some key insights extracted from Week 53 data:

- Revenue increased by **28.8%** WoW, with a customer count increase of **25.96%**.
- **Male customers** contributed more revenue (31M) compared to female customers (26M).
- **Blue and Silver cards** dominated, contributing to **93%** of overall transactions.
- States like **TX, NY, and CA** contributed **68%** of the overall revenue.
- The overall activation rate is **57.5%**, while the delinquent rate remains low at **6.06%**.

---

## 🚀 How to Use

1. **Clone the Repository**:  
   ```bash
   git clone https://github.com/yourusername/Credit_Card_Financial_Dashboard.git
   ```
   
2. **Database Setup**:
   - Create and import data into SQL using the provided SQL scripts.
   - Connect your SQL database to Power BI for real-time data visualization.

3. **Power BI Dashboard**:  
   Open the Power BI file to explore the interactive reports.

---

## 🧑‍💻 SQL Queries and Data Pipeline

- **SQL Database Creation**: The database includes two tables (`cc_detail` and `cust_detail`), populated using CSV imports.
- **DAX Queries**: Custom queries are used for grouping customers by age, income, and weekly trends.
  
Here’s an example of one DAX query used for calculating weekly revenue:
```sql
Current_week_Revenue = CALCULATE(
   SUM('cc_detail'[Revenue]),
   FILTER(ALL('cc_detail'), 'cc_detail'[Week_Num] = MAX('cc_detail'[Week_Num]))
)
```

---

## 🏆 Key Achievements

- Increased business intelligence through granular insights into customer behavior.
- Improved financial monitoring through real-time analytics.
- Enhanced ability to track key performance indicators (KPIs) and take data-driven decisions.
