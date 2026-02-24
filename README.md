# Bank-Customer-Churn-Analysis-Dashboard
This project analyzes bank customer data to identify churn trends, high risk customer segments, behavioral drivers of attrition and retention opportunities, the goal is to support data driven customer retention strategies
# 🏦 Bank Customer Churn Analysis Dashboard

## 📌 Project Overview

Customer churn is a major challenge in the banking industry. Losing customers reduces revenue, increases acquisition costs, and negatively impacts long-term profitability.

This project analyzes bank customer data to identify:

- Churn trends  
- High-risk customer segments  
- Behavioral drivers of attrition  
- Retention opportunities  

Using **Power BI, DAX, and Power Query**, I built an interactive dashboard that enables stakeholders to quickly answer:

> **Who is most likely to churn — and why?**

The goal is to support data-driven customer retention strategies.

---

## 🎯 Business Objectives

The dashboard answers key questions:

- What is the overall churn rate?
- Which customers are most at risk by age group?
- Does inactivity increase churn probability?
- How do credit scores and account balance affect churn rate?
- Do customers with more products churn less?
- Does tenure improve loyalty?

---

## 🛠 Tools Used

- **Power BI** (Visualization & Modeling)
- **DAX** (KPI calculations)
- **Power Query** (Data cleaning & transformation)
- **Excel / CSV** (Dataset)

---

## 📊 About the Dataset

The dataset contains information about bank customers, including:

- Demographic details  
- Account activity  
- Credit score  
- Account balance  
- Product usage  
- Churn status  

---

## 🔧 Data Preparation

- Removed duplicates  
- Renamed columns for clarity  
- Corrected data types  
- Cleaned categorical values  
- Optimized fields for segmentation analysis  

---

## 🔄 Data Standardization

To improve readability and business interpretation, coded values were standardized:

| Before | After |
|--------|-------|
| M / F | Male / Female |
| 0 / 1 (Has Credit Card) | Yes / No |
| 0 / 1 (Activity Status) | Active / Inactive |
| 0 / 1 (Churn) | Retained / Churned |

This ensured the dataset was easy to understand for both technical and non-technical stakeholders.

---

## 🧩 Data Formatting (Feature Engineering)

New columns were created:

- **Credit Score Bands** (300–400, 400–500, 500–600, 600–700, 700+)
- **Age Groups** (18–25, 26–35, 36–45, 46–55, 55+)
- **Account Balance Groups** (0, 1K–10K, 10K–50K, 50K–100K, 100K–150K, 150K+)
- **Tenure Groups** (2-year intervals)

These groupings allow meaningful comparison of churn behavior across segments.

---

## 📐 Core DAX Measures & KPI Logic

### Customer Metrics

```DAX
Total Customers =
COUNT(bank Customer Churn Prediction[customer_id])

Active Customers =
CALCULATE(
    COUNT(bank Customer Churn Prediction[customer_id]),
    bank[activity_status] = "Active"
)

Inactive Customers =
CALCULATE(
    COUNT(bank Customer Churn Prediction[customer_id]),
    bank[activity_status] = "Inactive"
)
