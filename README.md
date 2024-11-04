# nhanes_inferential_2023

## Overview

This project explores relationships and differences in health metrics and demographic variables using data from the [NHANES 2021-2023 survey](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2021-2023). The analysis was conducted using Python in Google Colab, with a focus on data preparation, inferential statistical tests, and findings.

## Research Questions and Analysis

### 1. Association Between Marital Status and Education Level
- **Objective**: Assess if there's a statistical association between marital status (married vs. not married) and education level (bachelor’s or higher vs. less than bachelor’s).
- **Test**: Chi-square test for independence.
- **Data Preparation**: Recoded `DMDMARTZ` and `DMDEDUC2` into binary categories.
- **Result**: Calculated chi-square statistic and p-value, followed by a bar plot visualizing the distribution. The result indicates whether education and marital status are associated.

### 2. Difference in Mean Sedentary Behavior Time Between Married and Not Married Individuals
- **Objective**: Determine if mean sedentary behavior differs based on marital status.
- **Test**: Independent t-test.
- **Data Preparation**: Cleaned `PAD680` by removing placeholder values (`7777`, `9999`) and recoded marital status as in Question 1.
- **Result**: Mean values and t-test results were displayed. The analysis shows if sedentary time significantly differs between marital status groups.

### 3. Effect of Age and Marital Status on Systolic Blood Pressure
- **Objective**: Examine how age and marital status jointly influence systolic blood pressure.
- **Test**: ANOVA.
- **Data Preparation**: Used `RIDAGEYR` (age) and `DMDMARTZ` (marital status).
- **Result**: Reported F-statistic and p-values for interpreting age and marital status’s influence on blood pressure.

### 4. Correlation Between Self-Reported Weight and Minutes of Sedentary Behavior
- **Objective**: Check for a correlation between self-reported weight and sedentary behavior time.
- **Test**: Pearson’s correlation coefficient.
- **Data Preparation**: Cleaned `WHD020` and `PAD680` for outliers (`7777`, `9999`).
- **Result**: Displayed correlation coefficient and p-value, providing insight into any significant linear relationship between weight and sedentary behavior.

### 5. Analysis of Education Level and Systolic Blood Pressure
- **Objective**: Assess if there's a significant difference in systolic blood pressure between individuals with a bachelor’s degree or higher and those with less than a bachelor’s degree.
- **Hypothesis**:
  - **Null Hypothesis (H0)**: No significant difference in systolic blood pressure between education levels.
  - **Alternative Hypothesis (H1)**: Significant difference in systolic blood pressure between education levels.
- **Test**: Independent t-test.
- **Data Preparation**: Recoded `DMDEDUC2` as “Bachelor_or_Higher” and “Less_than_Bachelor,” and removed `NaN` values in `BPXOSY3`.
- **Result**: Due to missing or insufficient data, the output returned `NaN` for the t-statistic and p-value. Therefore, we failed to reject the null hypothesis, suggesting no significant difference, though data limitations might affect this outcome.
