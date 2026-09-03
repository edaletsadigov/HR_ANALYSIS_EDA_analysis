# Charts — Explanation of Visualizations

This folder contains the static (PNG) versions of all 19 visualizations from the `HR_ANALYSIS_ədalət_sadıqov.ipynb` notebook. In the notebook, the original charts were built with Plotly (interactive); here they have been exported as static images with matplotlib/seaborn with the same content, so they display directly on GitHub.

All percentages are calculated on a dataset of 10,000 employees, with a baseline attrition rate of **19.97%** — compare each subgroup's percentage against this.

---

## 1. Attrition Analysis

### 01 — Attrition Count
![Attrition Count](01_attrition_count.png)

Total attrition count: 8,003 employees stayed (No), 1,997 employees left (Yes). Baseline rate: 19.97%.

### 02 — Attrition by Department
![Attrition by Department](02_attrition_by_department.png)

Attrition rate by department. Highest: Finance (20.85%), lowest: Marketing (~19.4%). The difference from the baseline rate (19.97%) is only about 1 percentage point — of little practical significance.

### 03 — Attrition by Job Role
![Attrition by Job Role](03_attrition_by_job_role.png)

Attrition rate by job role. Highest: Assistant (21.43%). The differences are small and were not confirmed by the Chi-Square test (see section 3).

### 04 — Attrition by Overtime
![Attrition by Overtime](04_attrition_by_overtime.png)

Among employees working overtime, attrition is 20.07%, and among those not working overtime, 19.87% — almost identical (difference of 0.2 percentage points). Overtime alone is not a strong explanatory factor.

---

## 2. Employee Groups Analysis

### 05 — Attrition by Gender
![Attrition by Gender](05_attrition_by_gender.png)

Comparison of attrition rate by gender.

### 06 — Attrition by Marital Status
![Attrition by Marital Status](06_attrition_by_marital_status.png)

Attrition rate by marital status (Single / Married / Divorced).

### 07 — Marital Status by Gender
![Marital Status by Gender](07_marital_status_by_gender.png)

Distribution of employee count by marital status × gender (demographic structure, not related to attrition).

### 08 — Attrition by Age Group
![Attrition by Age Group](08_attrition_by_age_group.png)

Attrition rate across 5 age groups (17-25, 26-35, 35-45, 46-55, 56-65).

### 09 — Income Distribution by Attrition
![Income Distribution by Attrition](09_income_distribution_by_attrition.png)

Box plot distribution of monthly income by Attrition=Yes/No — comparison of median and IQR.

### 10 — Average Income by Department and Attrition
![Average Income by Department and Attrition](10_avg_income_by_department_and_attrition.png)

Comparison of average income of retained vs. departed employees within each department.

### 11 — Satisfaction Metrics by Attrition
![Satisfaction Metrics by Attrition](11_satisfaction_metrics_by_attrition.png)

Average values of Job Satisfaction, Work-Life Balance, and Work Environment Satisfaction by Attrition. **Note:** Job Satisfaction and Work-Life Balance are actually somewhat **higher** among those who left; only Work Environment Satisfaction is lower — there is no consistent trend.

### 12 — Workload Metrics by Attrition
![Workload Metrics by Attrition](12_workload_metrics_by_attrition.png)

Average values of Project Count, Avg Hours/Week, and Absenteeism by Attrition (3 separate axis scales, subplot).

### 13 — Tenure Metrics by Attrition
![Tenure Metrics by Attrition](13_tenure_metrics_by_attrition.png)

Box plot distribution of Years at Company, Years in Current Role, and Years Since Last Promotion by Attrition.

---

## 3. Relationships and Final Decisions

### 14 — Correlation Heatmap
![Correlation Heatmap](14_correlation_heatmap.png)

Spearman correlation matrix among all numerical variables. **Key finding:** there is no correlation stronger than ±0.03 between `attrition_flag` and any other variable — meaning virtually no linear/monotonic relationship is observed in the dataset (see the "Important Note" section in the dataset README).

> Chi-Square test (Department vs Attrition): the χ² statistic was calculated, **p = 0.748** (p ≥ 0.05) — no statistically significant relationship was found between Department and Attrition. This test was not exported as a separate chart; the result is in the corresponding cell of the notebook.

---

## 4. Additional Analysis

### 15 — Workforce Structure
![Workforce Structure](15_workforce_structure.png)

Distribution of employee count by department and job role (2 side-by-side bar charts).

### 16 — Department × Job Level Matrix
![Department and Job Level Matrix](16_department_joblevel_matrix.png)

Department × Job Level heatmap — shows how many employees are at each level within each department.

### 17 — Salary by Department
![Salary by Department](17_salary_by_department.png)

Box plot distribution of monthly income by department.

### 18 — Salary by Job Level
![Salary by Job Level](18_salary_by_joblevel.png)

Box plot distribution of monthly income by Job Level (1-5).

### 19 — Salary by Job Level and Job Role
![Salary by Job Level and Job Role](19_salary_by_joblevel_and_role.png)

Faceted box plot distribution of monthly income by Job Level × Job Role (a separate panel for each role).

---

## General Note

None of the differences shown in files 09, 11, 12, 13, 17, 18, 19 have been statistically tested beforehand (only Department has a Chi-Square test) — these charts are primarily **descriptive** in nature and do not imply causation. Correlation ≠ causation.

## Related Files

- Dataset and column explanations → [`../dataset/README.md`](../dataset/README.md)
- Full analysis code → [`../notebook/HR_ANALYSIS_ədalət_sadıqov.ipynb`](../notebook/HR_ANALYSIS_ədalət_sadıqov.ipynb)
- General project overview → [`../README.md`](../README.md)

