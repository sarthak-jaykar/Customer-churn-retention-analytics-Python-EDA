# Customer Churn \& Retention Analytics

Which telecom customers are most likely to leave, which customer characteristics go with churn, and which retention actions to prioritise. Built in Python (Jupyter notebook) with Pandas, NumPy, Matplotlib and Seaborn.

!\[Python](https://img.shields.io/badge/Python-3776AB?logo=python\&logoColor=white)

!\[Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas\&logoColor=white)

!\[NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy\&logoColor=white)
!\[Matplotlib](https://img.shields.io/badge/Matplotlib-11557C)
!\[Seaborn](https://img.shields.io/badge/Seaborn-4C8BB5)
!\[Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter\&logoColor=white)
!\[Domain](https://img.shields.io/badge/Domain-Business%20Analysis-success)

## Project Overview

Customer churn directly affects recurring revenue and customer lifetime value. A telecom business needs to know where churn sits and what to do about it.

The analysis answers these business questions:

1. Which customer segments are most likely to churn?
2. Which customer characteristics go with churn: contract, payment method, services, tenure and charges?
3. Which combinations of factors identify higher-risk customers?
4. What retention actions should the business prioritise?

The scope is customer records from one telecom service. Causes of churn, competitor offers and customer satisfaction are out of scope.

## Data Source

**Dataset:** Telco Customer Churn, a public customer dataset borrowed from the internet. Labelled as a **secondary dataset from public sources**. 7,043 customer records, 21 columns, one row per customer.

**File used:** `data/Telco-Customer-Churn.csv` (included in this repository). The dataset is treated as secondary data for educational portfolio analysis.

## Key Metrics (7,043 customers)

|KPI|Result|
|-|-|
|Customers|**7,043** (no duplicate customer IDs)|
|Churned customers|**1,869**|
|Overall churn rate|**26.54%** (about 1 in 4 customers)|
|Month-to-month contract churn|**42.71%**|
|One-year / two-year contract churn|**11.27%** / **2.83%**|
|Electronic check payment churn|**45.29%**|
|Fiber optic churn|**41.89%**|

## Key Findings

These findings describe the dataset. They show where churn sits, not why, and they do not establish causal effects.

1. **Overall, about 1 in 4 customers churned (26.54%).**
2. **Contract length is the strongest pattern.** Month-to-month customers churn at 42.71%, one-year at 11.27% and two-year at 2.83%.
3. **Newer customers are more likely to leave.** Churned customers averaged 17.98 months of tenure against 37.57 months for retained customers.
4. **Payment and service type matter.** Electronic check customers churn at 45.29% and fiber optic customers at 41.89%.
5. **Customers without online security or tech support churn at about 41%.** Those with both services churn at 9.01%.
6. **Churned customers pay more.** Average monthly charges are 74.44 for churned customers against 61.27 for retained customers.
7. **The highest-risk segments are month-to-month customers in these groups:** senior citizens (54.65%), fiber optic (54.61%) and electronic check payment (53.73%).

## Recommended Actions

These are proposed retention actions, not proven results.

|Priority|Area|Action|Proposed target|
|-|-|-|-|
|**P1**|Contract|Move month-to-month customers to longer contracts with targeted incentives.|Month-to-month churn below 35%|
|**P1**|High-risk segments|Run proactive retention for month-to-month senior, fiber optic and electronic-check customers.|Segment churn tracked monthly|
|**P2**|Onboarding|Strengthen onboarding and early-tenure support for newer customers.|Churn in the first 12 months|
|**P2**|Fiber service|Investigate pricing, service quality and support for fiber optic customers.|Fiber churn tracked quarterly|
|**P3**|Payment|Encourage migration from electronic check to automatic payment.|Share of electronic-check customers|
|**P3**|Services|Offer online security and tech support to customers without them.|Take-up and churn of those customers|

## Tools and Methodology

* **Python and Jupyter:** the analysis runs top to bottom in one notebook.
* **Libraries:** Pandas and NumPy for cleaning and summaries; Matplotlib and Seaborn for charts.

**Method**

* Phase 1: data understanding. Phase 2: cleaning. Phase 3: validation. Phase 4: EDA. Phase 5: business insights. Phase 6: final charts.
* Churn rates are shares of customers in each group who churned.
* Combinations of two factors identify the highest-risk groups.

**Cleaning rules**

* `TotalCharges` is stored as text. It is converted to a number. Eleven blank values belong to new customers with zero tenure, and they are set to 0.
* Duplicate checks and missing-value checks are run and reported.

**Outputs**

* Charts are saved to `screenshots/` (6 files).
* Summary tables are saved to `results/` (19 files).

## Repository Structure

```text
customer-churn-retention-python/
├── README.md
├── data/                                Included source dataset (Telco-Customer-Churn.csv)
├── documentation/
│   ├── 01\_business\_brief.md             Context, stakeholders, decisions, questions
│   ├── 02\_data\_and\_quality.md           Source, fields, quality decisions, reconciliation
│   └── 03\_findings\_and\_recommendations.md  Metric definitions, findings, actions
├── results/                             19 exported summary tables
├── screenshots/                         6 exported analysis charts
├── script/
│   └── customer\_churn\_analysis.ipynb    Analysis notebook
└── requirements.txt
```

## Analysis

|Question|Notebook section|Output|
|-|-|-|
|Q1. Overall churn|Phase 4|`churn\_distribution.csv`, `screenshots/01\_churn\_counts.png`, `02\_churn\_percentage.png`|
|Q2. Contract, payment and services|Phase 4|`churn\_rate\_by\_contract\*.csv`, `churn\_rate\_by\_paymentmethod.csv`, `churn\_rate\_by\_onlinesecurity.csv`, `churn\_rate\_by\_techsupport.csv`|
|Q3. Demographics and household|Phase 4|`churn\_rate\_by\_gender.csv`, `churn\_rate\_by\_seniorcitizen.csv`, `churn\_rate\_by\_partner.csv`, `churn\_rate\_by\_dependents.csv`|
|Q4. Tenure and charges|Phase 4|`tenure\_and\_charges\_by\_churn.csv`, `screenshots/06\_tenure\_vs\_monthly\_charges.png`|
|Q5. Combined high-risk segments|Phase 4 and 5|`churn\_rate\_by\_contract\_payment.csv`, `churn\_rate\_by\_contract\_internet.csv`, `churn\_rate\_by\_contract\_senior.csv`|

## Documentation

* [Business Brief](documentation/01_business_brief.md): stakeholders, decisions and questions
* [Data and Quality](documentation/02_data_and_quality.md): source, fields, quality decisions and checks
* [Findings and Recommendations](documentation/03_findings_and_recommendations.md): metric definitions, findings and actions

## How to Reproduce

```bash
pip install -r requirements.txt
jupyter notebook script/customer\_churn\_analysis.ipynb
```

The CSV is included in `data/`. Open the notebook and choose **Run All**. Charts and tables are saved automatically.

## Limitations

* **One snapshot:** the dataset shows customers at one point in time, so it cannot show how churn developed.
* **Associations only:** the rates show where churn sits, not why.
* **Secondary dataset:** the source is a public copy, and the notebook has not been checked against a company's own records.
* **No revenue figures:** lifetime value and revenue impact are not calculated.

## Author

[Sarthak Jaykar](https://www.linkedin.com/in/sarthak-jaykar/)

