# Reducing Corporate Churn: An Actionable Data Audit Using Python and Correlation Analysis

Exploratory and correlation analysis of employee attrition, built to identify the strongest drivers of turnover and turn them into concrete, actionable HR recommendations.

## Overview

Losing employees is expensive — recruiting, onboarding, and lost productivity all add up. This project audits an HR dataset of 1,470 employees to answer one question: **why are people leaving, and what can the company do about it?**

Using Python for data cleaning, exploratory data analysis (EDA), and correlation analysis, the project moves from raw HR records to a set of prioritized, evidence-backed recommendations for reducing attrition.

## Dataset

- **Source:** IBM HR Analytics Employee Attrition & Performance dataset
- **File:** `HR-Employee-Attrition.csv`
- **Size:** 1,470 employee records, 35 attributes (demographics, compensation, job role, satisfaction scores, tenure, and more)
- **Data quality:** No missing or null values across any column

| Metric | Value |
|---|---|
| Total employees | 1,470 |
| Employees who left | 237 (16.1%) |
| Attrition rate — overtime workers | 30.53% |
| Attrition rate — non-overtime workers | 10.44% |
| Overtime attrition multiplier | ~2.9x |

## Tools & Libraries

- **Python 3**
- `pandas`, `numpy` — data loading, cleaning, and transformation
- `matplotlib`, `seaborn` — visualization
- `scikit-learn` — imported to scaffold a predictive extension 

## Methodology

1. **Data audit** — checked structure, data types, and missing values (`.info()`, `.describe()`, `.isna()`) to confirm the dataset was clean and analysis-ready.
2. **Exploratory Data Analysis** — visualized the overall attrition split, and compared attrition against salary, age, tenure, commute distance, and department.
3. **Categorical encoding** — one-hot encoded categorical fields (business travel, department, education field, gender, job role, marital status, overtime) to make them usable in correlation analysis.
4. **Correlation analysis** — correlated all numeric and encoded categorical variables against attrition, visualized as heatmaps, to rank the strongest predictors.
5. **Targeted deep-dive** — isolated overtime as a variable and quantified its effect on attrition rate directly.

## Key Insights

1. **Overtime is the single biggest driver of attrition.** Employees who work overtime leave at more than triple the rate of those who don't (30.53% vs. 10.44%) — a 20-point gap.
2. **Pay is a factor.** Employees who left earned noticeably less on average than those who stayed, pointing to a pay gap between leavers and stayers.
3. **Commute distance matters most among numeric variables.** `DistanceFromHome` has the highest positive correlation with attrition of any numeric field, and employees living farther from the office leave more often.
4. **Life stage and role concentrate risk.** Single employees, frequent travelers, and Sales Representatives show elevated attrition compared to their peers.
5. **Tenure and seniority are protective.** Total working years, job level, years in current role, and age are among the strongest factors *reducing* attrition risk — newer, junior employees are the most flight-prone.

## Recommendations

1. **Rebalance workloads** to reduce reliance on overtime, the strongest single predictor of attrition.
2. **Close the pay gap** between at-risk and retained employees, particularly for junior and lower-tenure staff.
3. **Offer hybrid work or flexible start times** for employees with long commutes.
4. **Prioritize retention efforts** on early-tenure, single employees and the Sales department, where risk is most concentrated.

## Repository Structure

```
.
├── README.md
├── HR-Employee-Attrition.csv
└── Reducing_Corporate_Churn_An_Actionable_Data_Audit_using_Python_and_Correlation_Analysis.ipynb
```

## How to Run

1. Clone the repository and navigate into it.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Launch the notebook:
   ```bash
   jupyter notebook "Reducing_Corporate_Churn_An_Actionable_Data_Audit_using_Python_and_Correlation_Analysis.ipynb"
   ```
4. Run all cells — `HR-Employee-Attrition.csv` should be in the same directory as the notebook.

## Future Work

- Train a predictive model (e.g., logistic regression, already scaffolded via `scikit-learn` imports) to flag at-risk employees before they leave.
- Build a simple attrition-risk scoring dashboard for HR to monitor in real time.
- Test statistical significance (e.g., chi-square, t-tests) behind the correlations to confirm which relationships are robust versus noise.

## Author

**Reliance Adegunloye**
Data Analyst | ALX Africa Certified
[![My LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/reliance-adegunloye?utm_source=share_via&utm_content=profile&utm_medium=member_ios) | adegunloyereliance@gmail.com
