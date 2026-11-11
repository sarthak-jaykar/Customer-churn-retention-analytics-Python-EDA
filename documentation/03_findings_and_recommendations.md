# Findings and Recommendations

## How to read this
Each finding follows: **finding → evidence → business implication → recommendation → measure**. Findings are associations in one snapshot, not causes.

## Metric definitions

| Metric | Definition |
| --- | --- |
| Churn rate | Churned customers in a group ÷ customers in that group |
| Average tenure | Mean months with the company, by churn status |
| Average monthly charges | Mean MonthlyCharges, by churn status |
| High-risk segment | A combination of factors with a churn rate above the overall rate, shown with its base count |

## Findings

**F1. About 1 in 4 customers churned (26.54%).**
*Implication:* the churn problem is material for recurring revenue.
*Recommendation:* set a churn target and track it monthly. *Owner:* retention manager.
*Measure:* monthly churn rate.

**F2. Month-to-month contracts churn most.**
42.71% for month-to-month, 11.27% for one year and 2.83% for two years.
*Implication:* the contract is the clearest lever in this data.
*Recommendation:* offer targeted incentives to move month-to-month customers to longer contracts. *Owner:* product manager.
*Measure:* share of month-to-month customers, monthly.

**F3. Newer customers churn more.**
Churned customers average 17.98 months of tenure against 37.57 for retained customers.
*Implication:* early tenure is the risk window.
*Recommendation:* strengthen onboarding and check-ins in the first year. *Owner:* customer success lead.
*Measure:* churn within 12 months of joining.

**F4. Electronic check and fiber optic customers churn more.**
45.29% for electronic check, 41.89% for fiber optic.
*Implication:* payment method and service type point to specific groups to review.
*Recommendation:* encourage automatic payment, and review fiber pricing, service quality and support. *Owner:* retention manager with product.
*Measure:* churn by payment method and internet service.

**F5. Security and support services go with lower churn.**
Customers without online security or tech support churn at about 41%. Customers with both services churn at 9.01%.
*Implication:* these services may protect against churn, but the data cannot show that they cause it.
*Recommendation:* test offering these services to customers without them, against a control group. *Owner:* product manager.
*Measure:* churn in the offered and control groups.

**F6. Churned customers pay more per month.**
Average monthly charges are 74.44 for churned customers against 61.27 for retained customers.
*Implication:* price may be part of the churn pattern.
*Recommendation:* review pricing for high-charge customers before changing any offer. *Owner:* finance partner with product.
*Measure:* churn by charge band.

**F7. Highest-risk segments.**
Month-to-month senior citizens 54.65%, month-to-month fiber optic 54.61%, month-to-month electronic check 53.73%.
*Implication:* these groups are the first targets for proactive retention.
*Recommendation:* run a retention campaign for these groups, with a control group. *Owner:* retention manager.
*Measure:* churn in the campaign and control groups, monthly.

## KPI definitions

| KPI | Definition |
| --- | --- |
| Churn rate | Churned ÷ customers in the group |
| Average tenure by churn | Mean tenure in months for churned and retained customers |
| Average monthly charges by churn | Mean MonthlyCharges for churned and retained customers |

## Caveats
- One snapshot: no time series.
- Associations only: no causal claims.
- Secondary public dataset, not checked against company records.
