# Loan Risk Analysis Portfolio – Quantitative Risk Analyst (Nordea)
# Project Overview

This project analyzes a dataset of 614 loan applications to understand factors influencing loan approval and develop a framework for credit risk assessment. The analysis covers:

- Data Cleaning and EDA

- Feature Engineering and Transformation

- Predictive Modeling using Logistic Regression and XGBoost

# Objective:
To explore borrower characteristics, identify key predictors of loan approval, and develop an interpretable model for estimating the probability of default (PD), supporting risk-based lending decisions.

# Dataset:
The dataset includes demographic and financial information, such as ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History, MaritalStatus, Gender, NumberOfDependents, Property_Area, and Loan_Status.

**Link to Raw Data**: https://www.kaggle.com/datasets/burak3ergun/loan-data-set/data

# Project Pipeline
Raw Dataset (614 applications)
        |
Data Cleaning & Missing Value Handling
        |
Exploratory Data Analysis
        |
Feature Engineering & Transformation
        |
Train/Test Split
        |
Model Training (Logistic Regression, XGBoost)
        |
Hyperparameter Tuning
        |
Model Evaluation
        |
Credit Risk Assessment (PD & Risk Segmentation)

# Methodology
## Notebook 1 – Exploratory Data Analysis (EDA)

**Data Cleaning:** Imputed missing values (median/mode), analyzed missingness (mostly MCAR).

**Feature Engineering:** Created derived features:

- Total_Income = Applicant + Coapplicant income

- DTI (Debt-to-Income ratio)

- Debt_Ratio (Loan-to-Income ratio)

- Has_Coapplicant (binary indicator)

**Outlier & Skew Handling:** Winsorization and log transformations applied to numeric variables.

**Insights:**

- Credit_History is the most predictive variable for loan approval.

- Several numeric features were skewed but are now suitable for modeling.

## Notebook 2 – Feature Engineering & Data Preparation

**Data Split:** 80% training, 20% testing.

**Feature Encoding:** One-hot encoding for categorical variables.

**Model Insights (preliminary):**

- Logistic Regression highlighted Credit_History, Has_Coapplicant, and financial ratios.

- XGBoost identified Credit_History, Education, Property_Area_Semiurban, and Loan_Amount_Term as key predictors.

- Feature Retention Strategy: All features retained to allow interaction effects in modeling.

## Notebook 3 – Predictive Modeling & Risk Assessment

**Models:** Logistic Regression and XGBoost, with and without hyperparameter tuning.

**Performance:**

- Logistic Regression (tuned) achieved AUC ≈ 0.85; interpretable and suitable for risk assessment.

- XGBoost performed robustly but is less interpretable.

**Risk Segmentation:**

- PD-based categories: Low, Medium, High Risk.

- Confusion matrix indicates most safe applicants approved, high-risk applicants flagged or rejected.
| :Risk Category: | :Number of Applicants: | :Average PD (%): | :Total Loan Amount: | :Total Expected Loss: |
|:---------------:|:----------------------:|:----------------:|:-------------------:|:---------------------:|
| :Low Risk:      | :97:                   | :3.9:            | :13,548:            | :287:                 |
| :Medium Risk:   | :12:                   | :30.6:           | :1,617:             | :225:                 |
| :High Risk:     | :14:                   | :62.9:           | :2,384:             | :739:                 |

**Key Takeaways:**

- Preprocessing, feature engineering, and tuning improve model stability.

- Credit_History, financial ratios, and coapplicant presence are strong predictors.

- Logistic Regression offers a transparent, actionable framework for credit risk decisions.

**Key Insights**

- Borrower financial capacity and credit history are the strongest predictors of loan approval.

- Derived ratios like DTI and Debt_Ratio provide meaningful risk signals.

- Preprocessing improves interpretability and model performance for linear models.

- Tree-based models (XGBoost) capture complex patterns with minimal preprocessing.

- PD-based segmentation supports risk-aware lending strategies.

# Limitations

Dataset is small (614 observations), so results may not generalize broadly. Analysis identifies associations, not causal relationships. Some high-dimensional interactions may require larger datasets to validate.

# Intended Use

This portfolio demonstrates quantitative risk analysis workflow: from cleaning and exploration, to feature engineering, predictive modeling, and PD-based risk assessment. It is suitable for showcasing skills relevant to a Junior Quantitative Risk Analyst role.
