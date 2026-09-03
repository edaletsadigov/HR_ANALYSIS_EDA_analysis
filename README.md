# HR Attrition Analysis

An analysis of employee attrition on a 10,000-employee HR dataset, carried out with Python (pandas, plotly, scipy). The project examines the relationship of department, job role, salary, satisfaction, workload, and tenure with attrition, and supports the findings with statistical tests (Chi-Square, Spearman correlation).

**Author:** Ədalət Sadıqov [LinkedIn](https://www.linkedin.com/in/%C9%99dal%C9%99t-sad%C4%B1qov-3b6297381/)

---

## Repo Structure

```
├── README.md                  ← this file (general overview)
├── dataset/
│   ├── employee_attrition_dataset_10000.csv
│   └── README.md               ← data dictionary, column explanations
├── charts/
│   ├── 01_attrition_count.png ... 19_salary_by_joblevel_and_role.png
│   └── README.md               ← explanation and finding for each chart
└── notebook/
    └── HR_ANALYSIS_ədalət_sadıqov.ipynb   ← full analysis code
```

- Dataset and column explanations → [`dataset/README.md`](dataset/README.md)
- Explanation of all 19 visualizations → [`charts/README.md`](charts/README.md)
- Full, working analysis code → [`notebook/HR_ANALYSIS_ədalət_sadıqov.ipynb`](notebook/HR_ANALYSIS_ədalət_sadıqov.ipynb)

---

## Methodology

1. **Data Overview & Cleaning** — 10,000 rows × 26 columns, no missing values, no duplicates, column names standardized.
2. **Attrition Analysis** — overall rate, breakdown by department, job role, overtime.
3. **Employee Groups Analysis** — comparison by gender, marital status, age group, salary, satisfaction, workload, tenure.
4. **Relationships & Statistical Testing** — Chi-Square test (Department vs Attrition), Spearman correlation matrix.
5. **Additional Analysis** — workforce structure (count by department/role), salary distribution (by department/job level/role).

---

## Visual Overview (Highlights)

The full set of charts (19 visuals) and their explanations → [`charts/README.md`](charts/README.md). The 4 most important findings are shown below.

### Attrition Count
![Attrition Count](charts/01_attrition_count.png)

1,997 out of 10,000 employees left — baseline attrition rate of **19.97%**.

### Attrition by Department
![Attrition by Department](charts/02_attrition_by_department.png)

The difference between departments is small (19.4%–20.9%) — the Chi-Square test shows this is not statistically significant.

### Satisfaction Metrics by Attrition
![Satisfaction Metrics by Attrition](charts/11_satisfaction_metrics_by_attrition.png)

Job Satisfaction and Work-Life Balance are actually somewhat **higher** among employees who left — no consistent, clear trend was found.

### Correlation Heatmap
![Correlation Heatmap](charts/14_correlation_heatmap.png)

Spearman correlation matrix: there is no relationship stronger than ±0.03 between `attrition_flag` and any other variable.

---

## Key Findings

1. Overall attrition rate of **19.97%** (1,997 out of 10,000 employees left).
2. Attrition is somewhat higher among employees working overtime (20.07% vs 19.87%), but the difference is small and should not be taken as a strong explanation on its own.
3. Job Satisfaction and Work-Life Balance were actually somewhat **higher** among employees who left, while only Work Environment Satisfaction was lower — no consistent, clear trend was found across the three metrics.
4. There are small differences by department (Finance 20.85%) and job role (Assistant 21.43%), but the Chi-Square test shows this is not statistically significant.
5. Chi-Square test result: **p = 0.748** (p ≥ 0.05) — no statistically significant relationship was found between Department and Attrition. The Spearman correlation matrix also shows no relationship stronger than ±0.03 across all variables.

> **Important note:** Correlation ≠ causation. In this dataset, there is generally a weak statistical signal between demographic/work variables and attrition — this suggests the dataset may be synthetic in nature (details: [`dataset/README.md`](dataset/README.md)).

## Business Recommendations

1. Distribute workload more evenly across teams to reduce overtime load.
2. Conduct quarterly employee satisfaction surveys, identify core issues in teams with low satisfaction, and implement targeted improvement measures.
3. Categorize the main turnover factors (compensation, workload, career development, job satisfaction, management, work environment) and develop targeted retention strategies for the highest-impact factors.

---

## Tools Used

- **Python** — pandas, numpy, scipy (statistics), plotly (interactive visualization)
- **Visualization (static export for this repo)** — matplotlib, seaborn
- **Statistical tests** — Chi-Square Test of Independence, Spearman Rank Correlation

## How to Run

```bash
pip install pandas numpy scipy plotly ipywidgets
jupyter notebook notebook/HR_ANALYSIS_ədalət_sadıqov.ipynb
```

The CSV file must be in the same folder as the notebook, or change the `pd.read_csv()` path to `dataset/employee_attrition_dataset_10000.csv`.



