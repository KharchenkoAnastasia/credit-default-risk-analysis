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

## 🧪 Exploratory Data Analysis (EDA)

The EDA was conducted using the Jupyter notebook:  
📄 `Home_Credit_Default_Risk.ipynb`

### 🔍 Key Steps Performed:

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

**14. Checking for Imbalance in the `TARGET` Column**
- Identified a strong class imbalance:
  - ~8% default (`TARGET = 1`)
  - ~92% non-default (`TARGET = 0`)

**15. Data Splitting Based on TARGET**

- Created subsets for deeper comparison between defaulters and non-defaulters.

**16. Univariate Analysis of Categorical Variables**

- Plotted frequency distributions and compared category rates between classes.

**17. Correlation Analysis of Numerical Variables**

- Computed Pearson correlation coefficients and visualized them with heatmaps.

**18. Univariate Analysis of Numerical Variables**

- Examined distributions and summary statistics of numeric features independently.

**19. Bivariate/Multivariate Analysis**

- Explored relationships between pairs or groups of features and their impact on default risk.

**20. Continuous and Categorical Variables**

- Compared continuous distributions across categories; examined influence of categorical variables on numeric values.

**21. Dependencies Between Categorical Variables**

- Investigated how categories interact (e.g., gender × income type) and their effect on target.

**22. Conclusion: Categories of Clients to Focus On When Granting a Loan**

- Identified high-risk client profiles based on age, education, employment type, and income sources.

## 📊 Key Insights & Conclusions

Based on the EDA findings, the following applicant categories are considered more or less suitable for loan issuance:

### ✅ Safer Candidates for Loans
- **Higher Education**: Applicants with higher or academic degrees show the lowest default rates.
- **High Income**: Individuals with above-average income and stable financial standing are more likely to repay.
- **Stable Employment**: Long-term work experience indicates consistent income and lower risk.
- **Asset Ownership**: Ownership of a car or real estate often correlates with financial stability.
- **Clean Credit History**: Applicants with minimal recent credit bureau inquiries and positive credit records pose less risk.

### ⚠️ Moderate Risk
- Applicants with secondary education but strong income, employment, or asset profiles should be assessed with stricter criteria.

### ❌ High-Risk Applicants
- **Secondary/Secondary Special Education**: Especially those with low income, large credit amounts, or frequent credit inquiries tend to have higher default rates.

### 📊 Tools & Libraries

- **Python**  
  - `pandas`, `numpy`, `matplotlib`, `seaborn`
- **Google Colab**

## 📁 Repository Structure

```text
credit-default-risk-analysis/
│
├── Home_Credit_Default_Risk.ipynb           # Main EDA notebook
├── README.md                                # Project summary (this file)
└── data/                                    # (Not included in repo; sourced from Kaggle)
    ├── application_train.csv                # Main training dataset with client information and TARGET
    └── HomeCredit_columns_description.csv   # Column descriptions for all data files


