# Loan Approval Prediction using Machine Learning

## Project Overview

This project focuses on predicting loan approval status using borrower information such as income, loan amount, credit history, education, employment status, and property area.

The objective is to build a supervised Machine Learning model capable of predicting whether a loan application will be approved while demonstrating data preprocessing, class imbalance handling, model evaluation, and business interpretation.

---

## Problem Statement

Financial institutions process a large number of loan applications every day. Manual assessment can be time-consuming and inconsistent.

This project aims to develop a Machine Learning solution that can assist in predicting loan approval decisions based on applicant attributes.

---

## Dataset

Dataset Source:

https://www.kaggle.com/datasets/bhanupratapbiswas/loan-approval-prediction-case-study

### Features

* Gender
* Married
* Dependents
* Education
* Self_Employed
* ApplicantIncome
* CoapplicantIncome
* LoanAmount
* Loan_Amount_Term
* Credit_History
* Property_Area

### Target Variable

* Loan_Status

  * Y = Approved
  * N = Rejected

---

## Project Workflow

### 1. Data Preprocessing

* Missing Value Handling
* Label Encoding of Categorical Variables
* Feature Scaling using StandardScaler
* Data Cleaning

### 2. Feature Engineering

Created additional features:

* TotalIncome = ApplicantIncome + CoapplicantIncome
* ApplicantIncome_Log
* LoanAmount_Log

These transformations help improve model learning and reduce skewness.

### 3. Class Imbalance Handling

The dataset contains more approved loans than rejected loans.

To address this issue:

* SMOTE (Synthetic Minority Oversampling Technique) was applied on the training dataset.

### 4. Model Building

The following models were trained and evaluated:

* Logistic Regression
* Random Forest Classifier

### 5. Model Evaluation

Evaluation metrics used:

* Precision
* Recall
* F1 Score
* ROC-AUC Score

---

## Model Performance

### Logistic Regression

| Metric    | Score |
| --------- | ----- |
| Precision | 0.874 |
| Recall    | 0.894 |
| F1 Score  | 0.884 |
| ROC-AUC   | 0.793 |

### Random Forest

| Metric    | Score |
| --------- | ----- |
| Precision | 0.851 |
| Recall    | 0.871 |
| F1 Score  | 0.860 |
| ROC-AUC   | 0.818 |

---

## Key Findings

* Logistic Regression achieved the highest Precision, Recall, and F1 Score.
* Random Forest achieved the highest ROC-AUC Score.
* Credit History was identified as the most influential feature affecting loan approval.
* Income-related features and Loan Amount also contributed significantly to prediction performance.

---

## Business Insights

The analysis indicates that applicants with:

* Strong credit history
* Stable income
* Favorable income-to-loan ratio

have a significantly higher probability of loan approval.

These insights can assist financial institutions in improving loan assessment processes and reducing risk.

---

## Visualizations Included

The notebook contains:

* Missing Values Analysis
* Loan Approval Distribution
* Correlation Heatmap
* Confusion Matrix
* ROC Curve
* Feature Importance Analysis

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Imbalanced-Learn (SMOTE)
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Repository Structure

```text
Loan_Approval_Predictor/
│
├── Loan_Approval_Prediction.ipynb
├── final_cleaned_dataset.csv
├── README.md
│
├── images/
│   ├── missing_values.png
│   ├── distribution.png
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   └── feature_importance.png
│
└── report/
    └── Loan_Approval_Project_Report.pdf
```

---

## Conclusion

This project successfully demonstrates an end-to-end Machine Learning workflow including data preprocessing, feature engineering, class imbalance handling, model comparison, evaluation, and business-oriented interpretation. The results show that both Logistic Regression and Random Forest are effective models for loan approval prediction, with Credit History emerging as the most important predictor of approval decisions.
