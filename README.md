# 📊 Customer Churn Analysis

## 📌 Project Overview

This project analyzes customer churn using Python, SQL, SQLite, Pandas, Matplotlib, and Seaborn.

The analysis uses a customer churn database containing 30,000 customer records across three tables:

- Customer
- Subscription
- Support

The objective is to understand customer churn patterns and identify the key factors associated with customer attrition, including subscription plans, contract types, customer satisfaction, support escalations, and cancellation reasons.

---

## 🎯 Project Objectives

- Analyze overall customer churn and retention
- Clean and prepare customer, subscription, and support data
- Identify churn patterns across different subscription plans
- Compare monthly and annual contract churn
- Analyze the relationship between customer satisfaction and churn
- Analyze the impact of support escalations on churn
- Identify major cancellation reasons
- Analyze customer lifetime value (CLTV)
- Generate actionable business insights for customer retention

---

## 🛠️ Tools & Technologies

- **Python**
- **SQL**
- **SQLite**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---

## 🗄️ Database Structure

The SQLite database contains three main tables:

### 1. Customer Table

Contains customer-level information such as:

- Customer ID
- Name
- Country
- State
- Gender
- Date of Birth
- Interests
- Pincode

### 2. Subscription Table

Contains subscription and churn-related information:

- Customer ID
- Subscription Start Date
- Subscription Type
- Renewal Date
- Plan Type
- Contract Type
- Cancellation Date
- Cancellation Reason
- Monthly Charges
- CLTV
- Churn Score
- Churn Flag

### 3. Support Table

Contains customer support information:

- Customer ID
- Complaint Date
- Escalation Status
- CSAT Score
- Customer Comments

The notebook shows 30,000 records in both the Customer and Subscription tables and 12,701 records in the Support table.

---

## 🧹 Data Cleaning

The project includes several data preparation steps:

- Checked table structure and data types
- Checked missing values
- Checked duplicate records
- Standardized gender values
- Converted date columns to datetime
- Handled missing country values using state information
- Removed unnecessary columns
- Standardized subscription type values
- Checked invalid CSAT scores
- Created the `churn_flag` based on cancellation status

The customer table was cleaned for missing values and unnecessary fields, while subscription dates were converted to datetime format. 

---

## 📈 Key Metrics

| Metric | Value |
|---|---:|
| Total Customers | 30,000 |
| Churned Customers | 8,973 |
| Retained Customers | 21,027 |
| Churn Rate | 29.91% |
| Retention Rate | 70.09% |
| Average Monthly Charges | 14.76 |
| Average CLTV | 532.93 |
| Average Churn Score | 43.06 |

The notebook calculates 8,973 churned customers and an overall churn rate of 29.91%.

---

## 🔍 Key Findings

### 📌 Overall Churn

The overall customer churn rate is **29.91%**, while the retention rate is **70.09%**.
### 📌 Contract Type

Monthly contract customers show a higher churn rate of **32.55%**, compared with **25.59%** for annual contract customers.

### 📌 Plan Type

Basic plan customers have the highest churn rate at **42.24%**, followed by:

- Standard: 26.75%
- Premium: 21.91%


### 📌 Customer Satisfaction

Customers with low CSAT scores have a churn rate of **73.17%**, compared with **40.37%** among customers with excellent CSAT scores. 

### 📌 Support Escalations

Customers with escalated support cases show a churn rate of **72.60%**, compared with **41.27%** among customers without escalations. 


### 📌 Cancellation Reasons

Among churned customers, the major recorded cancellation reasons include:

- Too expensive
- Switched to competitor
- Poor service
- Technical issues
- Not using the service

The notebook's cancellation analysis records **2,517 customers (28.05%)** citing "Too expensive" and **2,477 customers (27.61%)** citing "Switched to competitor." 

---

## 📊 Analysis Performed

The project analyzes churn across:

- Plan Type
- Contract Type
- Subscription Type
- State
- Monthly Charges
- CLTV
- Churn Score
- Customer Satisfaction (CSAT)
- Support Escalations
- Cancellation Reasons

The notebook also creates grouped churn analyses by plan, state, subscription type, and support escalation status.

---

## 💡 Business Insights

The analysis indicates that churn is associated with several customer and subscription factors, particularly:

- Plan type
- Contract type
- Customer satisfaction
- Support escalations
- Cancellation reasons

Pricing concerns and competitor switching are also prominent cancellation reasons.

---
├── Churn_Analysis.ipynb
└── customer_churn.db
