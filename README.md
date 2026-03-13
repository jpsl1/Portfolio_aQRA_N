# Credit Risk Analysis – Loan Default Prediction
This project explores credit risk modelling using a consumer loan dataset.
The objective is to identify drivers of loan default and build a simple probability of default (PD) model while demonstrating data quality assessment, risk segmentation, and expected loss estimation similar to frameworks used in banking risk manageme

Data used: Loan Data Set from https://www.kaggle.com/datasets/burak3ergun/loan-data-set/data

Goal:
Explore, validate, and model credit risk in a loan dataset while demonstrating banking concepts and data governance practices.

What is done:
- Data quality analysis
- Exploratory data analysis
- Credit risk modelling
- Logistic regression PD model
- Expected loss estimation
_______________________
# Project Overview - Loan Risk Analysis Portfolio for Nordea – Quantitative Risk Analyst
** Objective:**

The purpose of this project is to analyze a dataset of loan applicants to understand the factors influencing loan approval and to develop a framework for assessing credit risk. In Notebook 1, the focus is on exploring the data and visualizing its distributions.
 In Notebook2, I do basic data preparation for model building
In Notebook 3, I build predictive models and evaluate risk of a loaner.
Dataset:
The dataset contains 614 loan applications with features including ApplicantIncome, CoapplicantIncome, LoanAmount, Loan_Amount_Term, Credit_History, MaritalStatus, Gender, NumberOfDependents, Property_Area, and Loan_Status.
Link to raw data: Loan Data Set
Approach:
The project is divided into three stages:
Exploratory Data Analysis (Notebook 1): Inspect and clean the dataset, handle missing values, visualize distributions of categorical and numeric variables, and explore relationships between features and loan approval using boxplots, histograms, and countplots.
Feature Engineering and Preparation (Notebook 2): Transform numeric features, create derived features such as Total_Income, DTI, and Debt_Ratio, and prepare the dataset for modeling by encoding categorical variables and selecting features.
Modeling and Risk Assessment (Notebook 3): Apply Logistic Regression and XGBoost models to predict loan approval, compare model performance, and evaluate predicted probabilities to estimate credit risk.
Key Considerations:
Outliers were inspected using histograms and boxplots; winsorization and log transformations were used selectively to preserve realistic applicant behavior.
Derived financial measures were included to capture household repayment capacity.
Outcome / Goal (per notebook):
Notebook 1: Understand the dataset and identify variables that influence loan approval.
Notebook 2: Prepare features and the dataset for modeling to maximize predictive power.
Notebook 3: Build and evaluate predictive models for loan approval and perform risk estimation.
Intended Use:
This analysis provides a structured framework for evaluating loan applications and identifying key factors affecting credit risk. It demonstrates a combination of statistical analysis, feature engineering, and predictive modeling relevant for the role of a Quantitative Risk Analyst.
Notebook 1
Executive Summary (Notebook Header Version)
This project analyzes a dataset of 614 loan applications to understand the factors influencing loan approval and to develop a framework for assessing credit risk. The analysis includes exploratory data analysis, feature engineering, and predictive modeling using Logistic Regression and XGBoost.
Notebook Goal:
•	Notebook 1: Explore and visualize the data to identify key variables affecting loan approval.
•	Notebook 2: Prepare and engineer features for modeling to improve predictive performance.
•	Notebook 3: Build, evaluate, and compare predictive models for loan approval, and estimate credit risk.
The findings and models aim to provide a structured approach to evaluating loan applications and understanding household repayment capacity.
