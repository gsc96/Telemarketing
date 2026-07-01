# Telemarketing (SPANISH)

# Intelligent Data Analysis – Practical Assignment 1

Mandatory coursework for the **Intelligent Data Analysis** course of the **Master's Degree in Data Mining and Knowledge Discovery**. The objective of this project is to apply sampling techniques, descriptive statistics, data visualization, hypothesis testing, and linear regression to a real-world dataset using **R**.

## Dataset

- **Name:** ML Marathon Dataset (Azure Developer Community)
- **Source:** Microsoft Azure
- **Publication Year:** 2022
- **Type:** Open-access, multivariate CSV dataset

The dataset contains information from a **financial institution** that conducted **telemarketing campaigns** to promote **term deposit subscriptions**. Each record represents a customer contacted during one or more marketing campaigns and includes demographic information, banking details, and information about the contact itself.

The objective of the analysis is to characterize customers based on whether they subscribed to the term deposit and to identify which variables are associated with that decision.

### Main Variables

| Variable | Description |
|---|---|
| `age` | Customer age |
| `job` | Occupation |
| `marital` | Marital status (married, single, divorced) |
| `education` | Education level (primary, secondary, tertiary, unknown) |
| `default` | Whether the customer has credit in default |
| `balance` | Average yearly account balance |
| `housing` | Whether the customer has a housing loan |
| `loan` | Whether the customer has a personal loan |
| `contact` | Contact communication type (cellular, telephone, etc.) |
| `duration` | Duration of the last phone call (seconds) |
| `campaign` | Number of contacts performed during the current campaign |
| `pdays` | Days since the customer was last contacted in a previous campaign |
| `previous` | Number of contacts before the current campaign |
| `poutcome` | Outcome of the previous marketing campaign |
| `deposit` | **Target variable:** whether the customer subscribed (`yes`) or not (`no`) to a term deposit |

A **balanced stratified random sample** was generated using the `deposit` variable (1,000 observations per class, **n = 2,000**) with a fixed random seed to ensure reproducibility. All analyses presented in this project were performed using this sample.

---

## Project Contents

Using the balanced stratified sample (`n = 2,000`), the following analyses were carried out:

1. Generation of the balanced stratified sample
2. Descriptive statistical analysis of numerical variables by `deposit` group (mean, median, mode, variance, skewness, kurtosis, etc.)
3. Graphical exploration of numerical variables
4. Frequency and percentage table of `marital` by `deposit`
5. Visualization of the frequency table
6. Association test between two categorized continuous variables
7. Association test between `education` and another categorical variable
8. 95% confidence interval for the difference in means by `deposit`
9. Hypothesis test for the difference in means
10. Hypothesis test on a stratified sample of 30 observations
11. Comparison of call duration across education levels (ANOVA or non-parametric alternative, including assumption checks)
12. Simple linear regression between two quantitative variables
13. Final report summarizing the main findings (500–800 words)

---

## Technologies and Libraries

- **R** (R Markdown)
- **dplyr** – data manipulation
- **readr** – CSV file import
- **e1071** – skewness and kurtosis
- **modeest** – mode estimation
- **corrplot** – correlation visualization
- **kableExtra** – table formatting
