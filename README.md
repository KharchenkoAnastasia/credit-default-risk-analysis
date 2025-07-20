# 🏠 Home Credit Default Risk – EDA Project

## 📌 Project Objective

The goal of this project is to explore and analyze data from the **Home Credit Default Risk** competition hosted on **Kaggle**. The aim is to assess the financial reliability of loan applicants and understand which factors contribute most to the risk of default. This analysis serves as a foundation for building predictive models that can estimate the likelihood of a client having repayment difficulties.

## 📂 Dataset Overview

The dataset was obtained from the official Kaggle competition:  
🔗 [Home Credit Default Risk – Kaggle Competition](https://www.kaggle.com/competitions/home-credit-default-risk)

### Primary Files Used in EDA:

#### `application_train.csv`
This is the main training dataset containing static data for loan applications. Each row represents a single loan, with one unique record per applicant. It includes the `TARGET` column indicating whether the applicant had repayment difficulties:

- `TARGET = 1`: Client had payment difficulties (e.g., overdue by more than X days).
- `TARGET = 0`: Client had no repayment issues.

#### `HomeCredit_columns_description.csv`
A metadata file containing detailed descriptions of all features (columns) present across the datasets. It was used to better understand the meaning and context of variables during the EDA process.

## 🔍 Key Steps Performed

**1. Data Structure Check**
- Inspected dataset dimensions, column names, and data types.

**2. Statistical Report for Numeric Variables**
- Used descriptive statistics (mean, median, standard deviation, etc.) to understand the distribution and scale of features.

**3. Analysis of Categorical Variables**
- Identified key categorical columns and analyzed their unique values.

**4. Analysis of Numerical Variables**
- Identified key numeric columns and analyzed their distributions and uniqueness.

**5. Handle Incorrect Data Types**
- Converted columns with incorrect types (e.g., converted `int` columns to `bool` to save memory) to appropriate data types.

**6. Handle Missing Values**
- Assessed the extent of missing data across all columns.
- Removed columns with more than **40% NULL** values.

**7. Check Columns with NULL Values < 40%**
- Retained and analyzed columns with acceptable levels of missing data.
- Evaluated columns based on:
  - Null Percentage
  - Skewness
  - Median
  - Mode
  - Mean

**8. Check Columns with NULL Values > 0% and < 1%**
- Carefully handled columns with minimal missing data to avoid unnecessary data loss.

**9. Analyze Columns with Invalid/Unknown Data Values**
- Replaced or categorized placeholder values such as `"XNA"`, `"Unknown"`, etc.
- Standardized columns like `DAYS_EMPLOYED` and `YEARS_REGISTRATION` by converting negative values to positive.

**10. Binning Continuous Columns**
- Transformed continuous numerical variables into categorical bins for improved interpretability.

**11. Categorizing the `YEARS_BIRTH` Column**
- Grouped clients into age brackets to analyze credit risk by age group.

**12. Categorizing the `YEARS_REGISTRATION` Column**
- Grouped clients based on the number of years registered to evaluate loyalty or stability.

**13. Saving Updated Data with Compression**
- Exported the cleaned and updated dataset in a compressed format for efficient storage and further modeling.


