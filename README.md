# Online Food Ordering Behaviour Analysis

Exploratory and inferential analysis of an online food delivery customer dataset, looking at customer demographics, ordering decisions and feedback.

---

## Overview

This project profiles customers of an online food delivery service and tests whether demographic characteristics are related to whether they order and the feedback they give. It combines descriptive statistics, visual analysis and standard hypothesis tests in a single Python notebook.

## Dataset

| Item | Detail |
|---|---|
| File | `online food delivery dataset.csv` |
| Source | **[Add dataset source and licence here]** |
| Raw size | 388 rows |
| After removing duplicates | 285 rows (103 duplicate rows dropped) |
| Missing values | None after cleaning |

**Columns:** Age, Gender, Marital Status, Occupation, Monthly Income, Educational Qualifications, Family size, Customer Type, latitude, longitude, Pin code, Output (ordering decision: Yes/No), Feedback (Positive/Negative).

## Analysis Steps

1. Load the data and remove the empty trailing column; trim whitespace in `Feedback`.
2. Check missing values and drop duplicate rows.
3. Descriptive statistics and frequency tables for the categorical variables.
4. Visual analysis: customers by gender, occupation, income, customer type, ordering decision and feedback; age and family-size distributions.
5. Cross-tabulations: ordering by education and by gender; feedback by customer type.
6. Hypothesis tests (5% significance level):
   - Chi-square: gender vs ordering decision
   - Chi-square: customer type vs feedback
   - Welch's t-test: age of customers who ordered vs those who did not
   - Pearson correlation: age vs family size

## Results

| Measure | Result |
|---|---|
| Customers (after cleaning) | 285 |
| Ordering decision | 217 Yes, 68 No |
| Feedback | 231 Positive, 54 Negative |
| Gender vs ordering | Not significant (χ² = 0.21, p = 0.65) |
| Customer type vs feedback | Not significant (χ² = 0.15, p = 0.93) |
| Age vs ordering | Significant difference: mean age 24.3 (Yes) vs 25.9 (No), p < 0.001 |
| Age vs family size | Weak but significant positive correlation (r = 0.21, p < 0.001) |


## Tools

Python (pandas, NumPy, Matplotlib, seaborn, SciPy)
