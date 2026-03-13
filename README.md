# Project Overview - Loan Risk Analysis Portfolio for Nordea – Quantitative Risk Analyst

**Objective:**

The purpose of this project is to analyze a dataset of loan applicants to understand the factors influencing loan approval and to develop a framework for assessing credit risk. <br>

In **Notebook 1**, the focus is on exploring the data and visualizing its distributions. <br>
In **Notebook 2**, the focus is on basic data preparation for model building. <br>
In **Notebook 3**, the focus is on predictive models and evaluate risk of a loaner. <br>

**Dataset:**
The dataset contains 614 loan applications with features including ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History, MaritalStatus, Gender, NumberOfDependents, Property_Area, and Loan_Status.

Link to raw data:  https://www.kaggle.com/datasets/burak3ergun/loan-data-set/data

### Approach:

The project is divided into three stages:

**Exploratory Data Analysis (Notebook 1):** Inspect and clean the dataset, handle missing values, visualize distributions of categorical and numeric variables as  well as demonstrate the need for derived features, and explore relationships between features and loan approval using boxplots, histograms, and countplots.

**Feature Engineering and Preparation (Notebook 2):** Transform numeric features, create derived features such as Total_Income, DTI, and Debt_Ratio, and prepare the dataset for modeling by encoding categorical variables and selecting features.

**Modeling and Risk Assessment (Notebook 3):** Apply Logistic Regression and XGBoost models to predict loan approval, compare model performance, and evaluate predicted probabilities to estimate credit risk.

### Key Considerations:

- Outliers were inspected using histograms and boxplots; winsorization and log transformations were used selectively to preserve realistic applicant behavior.
- Derived financial measures were included to capture household repayment capacity.
- Most important features for predicting loan approval are Loan_History and Property_Area_Semiurban

**Outcomes:**

Notebook 1: Understand the dataset and identify variables that influence loan approval.
- Visualized Credit_History as the most indicatory feature in loan approval. Demonstrated the need for numeric feature winzarisation and logistic transformation.
<br>
Notebook 2: Prepare features and the dataset for modeling to maximize predictive power.
- Found key features for model.
<br>
Notebook 3: Build and evaluate predictive models for loan approval and perform risk estimation.
- The logistic regression / XGBoost model achieved an AUC of 0.85, indicating strong ability to distinguish between approved and rejected loan applicants.

**Intended Use:**
This analysis provides a structured framework for evaluating loan applications and identifying key factors affecting credit risk. It demonstrates a combination of statistical analysis, feature engineering, and predictive modeling relevant for the role of a Quantitative Risk Analyst.

***Project Limitation:***
Due to the relatively small dataset (614 observations), results should be interpreted with caution. The analysis identifies patterns and associations within the data but does not imply causal relationships or guarantee generalization beyond this dataset.
