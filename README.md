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

- Raw Dataset (614 applications)
  
- Data Cleaning & Missing Value Handling
        
- Exploratory Data Analysis
        
- Feature Engineering & Transformation
        
- Train/Test Split
        
- Model Training (Logistic Regression, XGBoost)
        
- Hyperparameter Tuning
        
- Model Evaluation
        
- Credit Risk Assessment (PD & Risk Segmentation)

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
- 
**Key Takeaways:**

- Preprocessing and tuning improve model stability.

- Credit_History, financial ratios, property area and coapplicant presence are strong predictors.

- Logistic Regression offers a transparent, actionable framework for credit risk decisions.
  
**Risk Segmentation:**

- PD-based categories: Low, Medium, High Risk.

- Confusion matrix indicates most safe applicants approved, high-risk applicants flagged or rejected.

**Number of Applicant per Risk Category, Average PD of Applicants, Total Loan amount, and Expected Loss predicted by build model:**

- **Low Risk**
   - Number of Applicants: 97
   - Average PD (%): 3.9
   - Total Loan Amount: 13,548
   - Total Expected Loss: 287

- **Medium Risk**
   - Number of Applicants: 12
   - Average PD (%): 30.6
   - Total Loan Amount: 1,617
   - Total Expected Loss: 225

- **High Risk**
   - Number of Applicants: 14
   - Average PD (%): 62.9
   - Total Loan Amount: 2,384
   - Total Expected Loss: 739             

**Key Insights**

- Borrower financial capacity and credit history are the strongest predictors of loan approval.

- Preprocessing improves interpretability and model performance for linear models.

- Tree-based models (XGBoost) capture complex patterns with minimal preprocessing.

- PD-based segmentation supports risk-aware lending strategies.

# Limitations

Dataset is small (614 observations), so results may not generalize broadly. Analysis identifies associations, not causal relationships. Some high-dimensional interactions may require larger datasets to validate. 

# Intended Use

Demonstrate a quantitative risk analysis workflow, from data cleaning and EDA, to feature engineering, predictive modeling, and PD-based risk assessment.

# References used in portfolio

Articles by Muhammad Faizin Zen:

- Building a Credit Score Model: Understanding the Business Context and Dataset (Feb 2025)  
- Building a Credit Score Model: Handling Missing Values and Outliers (Feb 2025)
- Building a Credit Score Model: Feature Engineering and Encoding (Feb 2025)  
- Building a Credit Score Model: Feature Selection (Feb 2025)
-  Building a Credit Score Model: Model Selection, Training, and Evaluation (Feb 2025)
- Building a Credit Score Model: Hyperparameter Tuning for an Optimized Credit Scoring Model (Feb 2025)
- 
Example on Kaggle by Louis Deconinck
- Credit Risk Modelling: Probability of Default (2023)

  LGD estimation taken from
-  (Basel II Glossary, 2013: https://web.archive.org/web/20130421005422/http://www.basel-ii-risk.com/Basel-II/Basel-II-Glossary/Loss-Given-Default.htm)

## Instructions to Run the Notebooks

### 1. Clone the Repository

Download the repository to your local machine:
git clone https://github.com/jpsl1/Portfolio_aQRA_N.git

cd loan-risk-analysis

### 2. Install Required Packages

Create and activate a virtual environment (optional):
python -m venv venv
source venv/bin/activate

On Windows use:
venv\Scripts\activate

### Install the required dependencies:

pip install -r Requirements.txt

### 3. Launch Jupyter Notebook

Start Jupyter Notebook:

jupyter notebook

Open and run the notebooks sequentially:

1. **Notebook 1 – Exploratory Data Analysis  - data_quality_and_cleaning.ipynb**
2. **Notebook 2 – Feature Engineering & Data Preparation - transformation_and_feature_selection.ipynb**
3. **Notebook 3 – Predictive Modeling & Risk Assessment - modeling_and_risk_analysis.ipynb**

Each notebook builds on the output of the previous one.

### 5. Dataset

The dataset is included in the `data` folder.

Alternatively, it can be downloaded from:

https://www.kaggle.com/datasets/burak3ergun/loan-data-set/data
