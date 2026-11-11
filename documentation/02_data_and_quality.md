# Data and Quality

## Source
| Field | Value |
| --- | --- |
| Dataset | Telco Customer Churn |
| Label | Secondary dataset from public sources (borrowed from the internet) |
| File used | `Telco-Customer-Churn.csv` |
| Grain | one row per customer (customerID is unique) |
| Size | 7,043 rows, 21 columns |
| Target | Churn (Yes or No): 1,869 Yes (26.54%) |

## Key fields

| Field | Meaning |
| --- | --- |
| customerID | Unique customer code |
| gender, SeniorCitizen, Partner, Dependents | Demographics and household |
| tenure | Months with the company |
| PhoneService, MultipleLines, InternetService | Phone and internet services |
| OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies | Add-on services |
| Contract | Month-to-month, One year, Two year |
| PaperlessBilling, PaymentMethod | Billing |
| MonthlyCharges, TotalCharges | Charges |
| Churn | Target |

## Quality decisions

| # | Issue | Rows affected | Decision |
| --- | --- | --- | --- |
| 1 | TotalCharges stored as text | All rows | Converted to a number; blanks become missing before the next step |
| 2 | TotalCharges blank | 11 rows | All 11 have tenure 0 and have not churned. Set to 0. |
| 3 | Duplicate rows and duplicate customer IDs | 0 | Checked and reported |
| 4 | Missing values in other fields | 0 | Checked and reported |

## Reconciliation

| Check | Expected | Result |
| --- | --- | --- |
| Rows | 7,043 | 7,043 |
| Churned customers | 1,869 | 1,869 |
| Overall churn rate | 26.54% | 26.54% (`churn_distribution.csv`) |
| Blank TotalCharges after cleaning | 0 | 0 |
