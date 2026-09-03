# Dataset — Employee Attrition (10,000 rows)

This folder contains the raw dataset used in the HR Attrition Analysis project.

**File:** `employee_attrition_dataset_10000.csv`
**Size:** 10,000 employees (rows) × 26 columns
**Missing values:** none (0 missing values)
**Duplicates:** none (neither at the `employee_id` level nor at the full-row level)

---

## Column Explanations (Data Dictionary)

| Column | Type | Range / Values | Explanation |
|---|---|---|---|
| `Employee_ID` | int | 1–10000 | Unique employee ID |
| `Age` | int | 20–59 | Age |
| `Gender` | str | Male, Female | Gender |
| `Marital_Status` | str | Single, Married, Divorced | Marital status |
| `Department` | str | Finance, HR, IT, Marketing, Sales | Department |
| `Job_Role` | str | Analyst, Assistant, Executive, Manager | Job role |
| `Job_Level` | int | 1–5 | Job level (1 = lowest) |
| `Monthly_Income` | int | 3,000–19,999 | Monthly income |
| `Hourly_Rate` | int | 15–99 | Hourly rate |
| `Years_at_Company` | int | 1–29 | Number of years at the company |
| `Years_in_Current_Role` | int | 1–14 | Number of years in current role |
| `Years_Since_Last_Promotion` | int | 0–9 | Years since last promotion |
| `Work_Life_Balance` | int | 1–4 | Work-life balance rating (1 = poor, 4 = excellent) |
| `Job_Satisfaction` | int | 1–5 | Job satisfaction rating |
| `Performance_Rating` | int | 1–4 | Performance rating |
| `Training_Hours_Last_Year` | int | 0–99 | Training hours in the last year |
| `Overtime` | str | Yes, No | Whether the employee works overtime |
| `Project_Count` | int | 1–9 | Current number of projects |
| `Average_Hours_Worked_Per_Week` | int | 30–59 | Average weekly hours worked |
| `Absenteeism` | int | 0–19 | Days of absenteeism per year |
| `Work_Environment_Satisfaction` | int | 1–4 | Work environment satisfaction rating |
| `Relationship_with_Manager` | int | 1–4 | Relationship with manager rating |
| `Job_Involvement` | int | 1–4 | Degree of job involvement |
| `Distance_From_Home` | int | 1–49 | Distance from home (km) |
| `Number_of_Companies_Worked` | int | 1–4 | Number of companies previously worked at |
| `Attrition` | str | Yes, No | **Target variable** — whether the employee left or not |

> Note: two derived columns were also created during the analysis, which are not in the original CSV:
> `attrition_flag` (Attrition = "Yes" → 1, "No" → 0) and `age_group` (5 age groups: 17-25, 26-35, 35-45, 46-55, 56-65).

---

## Distribution of the Target Variable

| Attrition | Count | Percentage |
|---|---|---|
| No | 8,003 | 80.03% |
| Yes | 1,997 | 19.97% |

There is class imbalance (80/20) — this should be taken into account if any predictive model is built (e.g. class weighting, SMOTE, etc.).

---

## Important Note — Nature of the Dataset

The Spearman correlation matrix (see `../charts/14_correlation_heatmap.png`) and the Chi-Square test (Department vs Attrition, p = 0.748) show that in this dataset there is **virtually no strong, statistically significant relationship** between demographic/work variables and `Attrition` — all correlation coefficients are within ±0.03. This suggests the dataset is likely synthetic (artificially generated rather than drawn from a real work environment). Therefore, any predictive (classification) model built on this dataset is not expected to perform well — the dataset is better suited for **practicing EDA / visualization / statistical testing methodology** than for making real business decisions.

## Source

The dataset was provided by the user (Ədalət Sadıqov) for the HR Analysis project. It is not real company data.

