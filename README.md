# Bank-Customer-Churn-Analysis-Dashboard
This project analyzes bank customer data to identify churn trends, high risk customer segments, behavioral drivers of attrition and retention opportunities, the goal is to support data driven customer retention strategies

## Project Overview

Customer churn is a major challenge in the banking industry. Losing customers reduces revenue, increases acquisition costs, and negatively impacts long-term profitability.

This project analyzes bank customer data to identify:

- Churn trends  
- High risk customer segments  
- Behavioral drivers of attrition  
- Retention opportunities  

Using **Power BI, DAX, and Power Query**, I built an interactive dashboard that enables stakeholders to quickly answer:

> **Who is most likely to churn — and why?**

The goal is to support data-driven customer retention strategies.

---

## Business Objectives

The dashboard answers key questions:

- What is the overall churn rate?
- Which customers are most at risk by age group?
- Does inactivity increase churn probability?
- How do credit scores and account balance affect churn rate?
- Do customers with more products churn less?
- Does tenure improve loyalty?

---

##  Tools Used

- **Power BI** (Visualization & Modeling)
- **DAX** (KPI calculations)
- **Power Query** (Data cleaning & transformation)
- **Excel / CSV** (Dataset)

---

## About the Dataset

The dataset used for this analysis contains information about bank customers, including demographic details, account activity, and churn status. Below are the key fields:


- customer_id
- Country
- Gender
- Age
- Tenure
- Credit_card
- Active_member
- Estimated_salary
- Credit score  
- Balance  
- Product_number 
- Churn status  

---

##  Data Preparation

- Removed duplicates  
- Renamed columns for clarity  
- Corrected data types  
- Cleaned categorical values  
- Optimized fields for segmentation analysis  

---

## Data Standardization

To improve readability and business interpretation, coded values were standardized:

| Before | After |
|--------|-------|
| M / F | Male / Female |
| 0 / 1 (Credit Card) | Yes / No |
| 0 / 1 (Activity Status) | Active / Inactive |
| 0 / 1 (Churn) | Retained / Churned |

This ensured the dataset was easy to understand for both technical and non-technical stakeholders.

---

## Data Formatting (Feature Engineering)

New columns were created:

- **Credit Score Bands** (300–400, 400–500, 500–600, 600–700, 700+)
- **Age Groups** (18–25, 26–35, 36–45, 46–55, 55+)
- **Account Balance Groups** (0, 1K–10K, 10K–50K, 50K–100K, 100K–150K, 150K+)
- **Tenure Groups** (2-year intervals)

These groupings allow meaningful comparison of churn behavior across segments.

---

# KPIs Measured

Total Customers  
Active Customers  
Inactive Customers  
Churn Rate  
Retention Rate  

Users can filter by:  
Gender  
Country  

Enabling deeper exploration.

# Key Insights & Business Interpretation

The analysis revealed several important behavioral patterns that directly impact customer churn

## Geographic differences:

Using the country filter,it showed that customers in Germany have the highest churn rate (32.4%), suggesting possible dissatisfaction with banking services or competitive alternatives in that region

## Churn rate by Activity Status:

Approximately 48% of customers are classified as inactive, highlighting a significant segment of users with low engagement. This group demonstrates a higher likelihood of churn, recording a churn rate of 27%, compared to customers who are actively engaged.This suggests that customer inactivity is a key driver of churn

## Churn rate by Age groups

Mid-age and older customers experience the highest churn rates. Customers aged 46–55 recorded the highest churn rate at 50.6%, followed by customers aged above 55, with a churn rate of 38.8%, younger customer groups exhibit significantly lower churn rates, suggesting stronger retention among younger demographics.

## Churn rate by number of bank product:

Customers with 3 - 4 product exhibit higher churn rates of (83 -100%) while customers with 1 - 2 products represent the majority and show lower churn ,multiple product adoption does not automatically translate to loyalty, increased complexity and dissatisfaction with bundled offerings can increase attrition

## Churn rate by Tenure:

Early-stage customers (0–2 years) have a churn rate of 21.15%, indicating that a significant number of customers leave shortly after joining.

Similarly, long-term customers (8–10 years) exhibit a churn rate of 21.3%, suggesting that longer tenure alone does not ensure retention and that customers may require additional value or incentives to remain engaged.  

Overall, churn rates remain relatively consistent across all tenure groups, ranging between 18% and 21%, highlighting that customer longevity does not necessarily translate into loyalty.

## Churn rate by credit Scores:

Customers with lower credit scores (>400) show greater churn behavior of 100%, which is the highest among all credit score groups. Beyond the low score segment, churn remains relatively stable at (20-21%)

## Churn rate by Account balance

Customers with balances between 1k–10k show the highest churn risk (100%), while those with 10k–50k balances also display elevated churn at 34%, making them the most vulnerable segment.  

Churn decreases as account balance increases, with customers above 100k showing lower churn rates (23–26%). Customers with zero balances have the lowest churn rate (14%), likely representing dormant but retained accounts.

# RECOMMENDATION

Based on these insights, I recommend the following strategies to reduce bank customer churn:

## Regional Retention Strategy (Geographic Differences)

Develop region specific customer retention initiatives for Germany, where churn is highest.  

Conduct customer feedback analysis to identify service gaps and competitor advantages in that market.

## Improve Customer Engagement
Implement proactive engagement programs targeting inactive customers.

Use automated reminders, personalized communication, and email to  reduce inactivity  
Track inactivity as an early churn warning signal.

## Age Based Customer Strategies

Design retention campaigns specifically for customers aged 46+.

Offer personalized financial guidance, relationship management, or simplified digital support.

Provide educational resources tailored to older customer segments.

## Product Simplification and Experience Optimization

Review the customer journey for multi-product users (3–4 products).

Simplify bundled product offerings

Improve onboarding and communication for additional products.

## Life cycle Based Retention Programs (Tenure)

### For New Customers (0–2 years):

Strengthen onboarding processes.

Introduce early engagement incentives and customer support

### For Long-Tenure Customers (8–10 years):

Launch loyalty rewards and exclusive benefits.

Offer account reviews or personalized offers.

## Credit Risk Monitoring

Recommendation:

Closely monitor customers with very low credit scores.

Provide financial education or flexible account support where possible

## Account Balance Based Retention Strategy

Recommendation:

Focus retention campaigns on customers with 1K–50K balances, as they represent the highest churn risk.

Monitor declining balances as an early churn indicator.

Offer incentives that encourage balance growth
