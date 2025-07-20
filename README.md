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

