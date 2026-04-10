# 📊 Loan Default Risk Prediction using Logistic Regression

## 📌 Project Overview

This project focuses on analyzing borrower data and building a machine learning model to predict loan default risk. The goal is to help financial institutions identify high-risk customers and make better lending decisions.

The dataset contains ~396,000 loan records with 27+ features including borrower demographics, financial details, and credit history.

---

## 🎯 Objectives

* Analyze borrower behavior and financial patterns
* Identify key factors influencing loan defaults
* Build a predictive model for credit risk
* Provide actionable business recommendations

---

## 📂 Dataset

* Size: ~396K rows, 27+ features
* Includes:

  * Loan details (amount, term, interest rate)
  * Borrower info (income, employment, home ownership)
  * Credit history (DTI, public records, bankruptcies)

---

## 🛠️ Tech Stack

* Python (Pandas, NumPy)
* Visualization: Matplotlib, Seaborn
* Machine Learning: Scikit-learn
* Imbalanced Data Handling: SMOTE
* Statistical Analysis: Statsmodels

---

## 🔍 Key Steps

### 1. Data Preprocessing

* Handled missing values using domain-based imputation
* Extracted features from address and date columns
* Removed rows with excessive null values

### 2. Exploratory Data Analysis (EDA)

* Identified skewed distributions and outliers
* Found strong correlation between loan amount & installment (0.95)
* Observed majority loans are fully paid (~81%)

### 3. Feature Engineering

* Label Encoding & Target Encoding
* Created risk indicator flags:

  * `mort_acc_flag`
  * `pub_rec_flag`
  * `bankruptcies_flag`

### 4. Outlier Treatment

* Applied log transformation to reduce skewness

### 5. Multicollinearity Check

* Used VIF to remove highly correlated features
* Dropped:

  * `loan_amnt`
  * `sub_grade`

### 6. Model Building

* Algorithm: Logistic Regression
* Data split: Train / Validation / Test
* Feature scaling applied

### 7. Handling Imbalanced Data

* Used **SMOTE** to balance target classes

---

## 📈 Model Performance

### Before SMOTE:

* Accuracy: ~98.5% (biased due to imbalance)

### After SMOTE:

* Precision: ~0.86
* Recall: ~0.99 ✅
* F1 Score: ~0.92
* ROC-AUC: ~0.997

📌 High recall ensures most risky customers are correctly identified.

---

## 📊 Key Insights

### 👤 Customer Behavior

* Most borrowers:

  * Grade B (low risk)
  * Employment >10 years
  * Mortgage holders
* Top professions:

  * Teacher
  * Manager
  * Registered Nurse

### 💳 Loan Trends

* 36-month loans dominate (~75%)
* Debt consolidation is the top purpose (~60%)

### ⚠️ Risk Indicators

* High bankruptcies & public records → high risk
* Higher DTI → increased default probability
* Geographic location also impacts risk

---

## 💡 Business Recommendations

* Prioritize **recall-focused models** to avoid missing risky customers
* Offer **better rates to low-risk segments** (Grade A/B, stable jobs)
* Apply **strict checks for high-risk borrowers**
* Use **risk-based pricing strategies**
* Monitor high-risk regions and adjust policies

---

## 📌 Conclusion

The model performs exceptionally well in identifying high-risk borrowers with very high recall and strong overall performance. It can be effectively used in real-world credit risk assessment systems.

---
