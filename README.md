# Telco customer churn analysis and executive dashboard

## Overview
This project focuses on diagnosing and reducing customer churn for a telecommunications provider. Using Python for exploratory data analysis and Power BI Desktop for reporting, I built an executive dashboard to pinpoint where the company is losing money and how to keep customers from leaving.

Key metrics:
- Total customers: 7.04K
- Churned customers: 1.869K
- Overall churn rate: 26.54%
- Total revenue: $16.06M
- Lost revenue: $2.86M

---

## Dashboard preview

---

## How I built this project

### 1. Python data cleaning and feature engineering
- Cleaned the raw Telco dataset and resolved missing values in total financial charges.
- Created custom tenure groups (<1 year, 1-2 years, 2-3 years, 3-4 years, 4-5 years, 5-6 years) to better understand customer retention over time.
- Converted churn flags into numeric binary values (0/1) to calculate churn rates and feature relationships during Python EDA.
  
### 2. Data modeling and measures in Power BI
- Calculated core DAX metrics for total revenue, revenue loss, customer counts, and churn rates.
- Set up demographic slicers (SeniorCitizen, Dependents, Partner, PaperlessBilling) for quick filtering.

### 3. Dashboard design and visual layout
- Layout setup: Refined the visual arrangement into a balanced 2x2 grid. 
- Visual 1 (Lifecycle risk): Created a clustered column chart showing churn rate across contracts and tenure brackets. 
- Visual 2 (Support services): Built a clustered bar chart showing how TechSupport impacts churn across different internet services.
- Visual 3 (Financial leakage matrix): Applied conditional formatting to highlight exact revenue losses across internet services and payment methods.
- Visual 4 (Payment channels): Added a donut chart to break down churn by payment method.

---

## What the data tells us

### 1. The $1.435M revenue leak
Most of the financial damage is concentrated in one specific group: customers using Fiber Optic internet who pay via Electronic Check. This single intersection accounts for $1.435M in lost revenue, which is over half of the total $2.86M lost.

### 2. First-year month-to-month risk
Customers on Month-to-Month contracts during their first year (<1 year tenure) churn at a rate above 51%. Churn drops dramatically once customers pass two years of tenure or move onto 1-year or 2-year contracts.

### 3. Support services act as retention anchors
TechSupport and OnlineSecurity play a major role in keeping customers. Users without TechSupport see churn rates above 40%, while those with active support stay closer to 15%.

---

## Recommended next steps

- Incentive payment migration: Offer a small one-time credit ($5 to $10) to encourage Electronic Check users to switch to automatic payments like Bank Transfer or Credit Card.
- Onboarding support bundles: Give new Month-to-Month subscribers complimentary or discounted TechSupport trials during their first 90 days.
- Proactive contract upgrades: Target Month-to-Month customers reaching their 6-month and 11-month tenure milestones with annual contract upgrade offers.

---

## Note on project packaging
This portfolio is packaged as a local repository containing visual preview, raw data files, Python notebooks, and the original Power BI file (.pbix).
