# Customer Churn Prediction (Advanced)

## Problem Overview
Customer churn is a critical business problem, as retaining existing customers is often more cost-effective than acquiring new ones.  
The objective of this project is to build a **robust, end-to-end machine learning solution** that predicts whether a customer is likely to churn based on historical customer data.

This advanced version extends the basic churn prediction pipeline by incorporating **hyperparameter tuning, cross-validation, class imbalance handling, and model explainability**.

---

## Dataset Description
- **Dataset:** Telco Customer Churn Dataset (Publicly available)
- **Target Variable:** `Churn` (Yes / No)

### Feature Categories
- **Categorical Features:**  
  Gender, Contract, Internet Service, Payment Method, etc.
- **Numerical Features:**  
  Tenure, Monthly Charges, Total Charges

---

## Approach & Methodology

### 1. Data Understanding & Exploratory Data Analysis (EDA)
- Loaded and explored the dataset using `head()`, `info()`, and `describe()`
- Identified target variable distribution and class imbalance
- Handled missing and inconsistent values (conversion of `TotalCharges`)
- Performed EDA using visualizations:
  - Tenure vs Churn
  - Monthly Charges vs Churn
  - Contract Type vs Churn
- Summarized key insights to understand churn behavior

---

### 2. Feature Engineering
- Encoded categorical variables using one-hot encoding
- Scaled numerical features using `StandardScaler`
- Addressed class imbalance using:
  - Class weights
  - SMOTE (Synthetic Minority Over-sampling Technique)
- Clearly justified all feature engineering decisions

---

### 3. Model Development
The following machine learning models were used:
- **Logistic Regression** – baseline, interpretable model
- **Random Forest** – captures non-linear relationships and feature interactions

---

### 4. Hyperparameter Tuning & Cross-Validation
- Applied **GridSearchCV** to optimize Random Forest hyperparameters
- Tuned parameters such as number of estimators and tree depth
- Used **5-fold cross-validation** with ROC-AUC as the evaluation metric
- Selected the best-performing model based on cross-validated results

---

### 5. Model Evaluation
Models were evaluated using multiple performance metrics:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

Additional evaluation steps:
- Confusion matrix analysis
- Comparison of baseline vs tuned model performance
- Selection of the final model with clear justification

---

### 6. Model Explainability (SHAP)
- Used **SHAP (SHapley Additive exPlanations)** to interpret model predictions
- Identified the most influential features contributing to churn
- Visualized feature impact using SHAP summary plots
- Explained results in business-friendly terms

---

## Results Summary
- The tuned **Random Forest model** achieved the best performance across evaluation metrics
- Key churn drivers identified:
  - Month-to-month contracts
  - Low customer tenure
  - High monthly charges
  - Certain payment methods

---
