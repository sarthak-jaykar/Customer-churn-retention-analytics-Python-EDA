# Customer Churn & Retention Analytics

## Project Overview

This project analyzes customer churn patterns for a telecommunications company using Python and exploratory data analysis (EDA).

The objective is to identify customer segments with higher churn risk and translate the findings into actionable retention strategies.

## Business Problem

Customer churn directly affects recurring revenue and customer lifetime value. The business needs to understand:

- Which customer segments are most likely to churn?
- What customer characteristics are associated with churn?
- Which combinations of factors identify higher-risk customers?
- What retention actions could the business prioritize?

## Dataset

The dataset contains customer-level information including:

- Customer demographics
- Contract type
- Internet service
- Payment method
- Tenure
- Monthly charges
- Total charges
- Additional services
- Churn status

## Analysis Performed

### 1. Data Understanding
- Dataset structure
- Dimensions and columns
- Data types
- Initial data inspection

### 2. Data Cleaning
- Missing-value analysis
- Duplicate checks
- Data-type correction
- `TotalCharges` conversion and missing-value handling

### 3. Data Validation
- Data-type validation
- Unique-value checks
- Null-value verification
- Duplicate verification

### 4. Exploratory Data Analysis
- Overall churn distribution
- Churn by contract type
- Churn by internet service
- Churn by payment method
- Churn by customer demographics
- Churn by additional services
- Tenure and charge comparisons
- Combined customer-segment analysis
- Correlation analysis

### 5. Business Insights & Recommendations
EDA findings were translated into customer-risk segments and retention recommendations.

### 6. Final Visualization
Key findings were presented through charts for easier business interpretation.

## Key Findings

- Overall churn rate: **26.54%**
- Month-to-month customers: **42.71% churn**
- One-year contract customers: **11.27% churn**
- Two-year contract customers: **2.83% churn**
- Electronic check customers: **45.29% churn**
- Fiber optic customers: **41.89% churn**
- Churned customers had lower average tenure: **17.98 months**
- Retained customers had higher average tenure: **37.57 months**
- Churned customers had higher average monthly charges: **74.44**

### High-Risk Customer Combinations

| Customer Segment | Churn Rate |
|---|---:|
| Month-to-month + Senior Citizen | 54.65% |
| Month-to-month + Fiber optic | 54.61% |
| Month-to-month + Electronic check | 53.73% |

## Business Recommendations

- Encourage month-to-month customers to move to longer-term contracts through targeted incentives.
- Strengthen onboarding and retention programs for newer customers.
- Investigate pricing, service quality and support issues among fiber optic customers.
- Encourage migration from electronic checks to automatic payment methods.
- Promote Online Security and Tech Support through targeted offers.
- Use customer segmentation to identify high-risk customers for proactive retention campaigns.

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Git & GitHub

## Project Structure

```text
customer-churn-retention-analytics/
│
├── data/
├── notebooks/
├── outputs/
│   ├── charts/
│   └── screenshots/
│
├── README.md
├── requirements.txt
└── .gitignore