# Loan Prediction - Outlier Detection & Handling

This repository contains EDA and outlier handling on Loan Prediction dataset.

## Dataset Overview
- 367 rows, 12 columns
- Columns: ApplicantIncome, CoapplicantIncome, LoanAmount etc.

## Steps Performed
1. **Descriptive Stats:** `dataset.describe()` - Found max ApplicantIncome 72529 vs mean 4805
2. **Visualization:**
   - `sns.boxplot(x="ApplicantIncome")` - detected extreme outliers
   - `sns.boxplot(x="CoapplicantIncome")` - detected outliers
   - `sns.distplot / histplot` - right-skewed distribution
3. **Outlier Removal:**
   - Used IQR method to find max_range
   - Filtered data: `dataset[CoapplicantIncome > max_range]` to show max values
   - Cleaned dataset shape: 359 x 12 (after removal)

## Tools Used
Python, Pandas, Seaborn, Matplotlib, Jupyter Notebook

## Key Insight
After removal, boxplot becomes clean and data becomes normally distributed, improving model accuracy.
