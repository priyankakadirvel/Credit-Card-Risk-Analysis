# Credit Card Risk Analysis  
### Credit Default Prediction using Logistic Regression

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge)

---

## Project Overview
This project performs **credit card default risk analysis** using **Logistic Regression**, a widely accepted and interpretable classification model in the banking and financial domain.  
The objective is to predict whether a customer is likely to **default on credit payments**, enabling better **risk assessment and decision-making**.

The project demonstrates a **complete analytics and modeling pipeline**, from dataset understanding and EDA to model interpretation.

---

## Dataset Description
The dataset contains **1,150 customer records**, each representing an individual credit card holder with demographic, employment, income, and debt-related attributes.

### Dataset Shape
- **Rows:** 1,150  
- **Columns:** 9  

### Sample Records
| age | ed | employ | address | income | debtinc | creddebt | othdebt | default |
|----|----|--------|---------|--------|---------|----------|---------|---------|
| 41 | 3 | 17 | 12 | 176 | 9.3 | 11.36 | 5.01 | 1 |
| 27 | 1 | 10 | 6 | 31 | 17.3 | 1.36 | 4.00 | 0 |
| 40 | 1 | 15 | 14 | 55 | 5.5 | 0.86 | 2.17 | 0 |

---

## Feature Explanation

### Demographic & Stability Features
- **age** – Customer age  
- **ed** – Education level (ordinal scale)  
- **employ** – Years of employment  
- **address** – Years at current address  

These variables reflect **customer stability**, which influences repayment reliability.

---

### Financial Features
- **income** – Annual income  
- **debtinc** – Debt-to-income ratio  
- **creddebt** – Credit card debt  
- **othdebt** – Other outstanding debts  

Higher debt burden relative to income increases default risk.

---

### Target Variable
- **default**
  - `1` → Customer defaulted  
  - `0` → Customer did not default  

---

## Exploratory Data Analysis (EDA)
EDA revealed:
- Class imbalance between defaulters and non-defaulters
- Strong relationship between **debt ratios, employment duration**, and default risk
- Income alone is not sufficient; **debt structure matters more**

---

## Logistic Regression: Algorithm Explanation

### What is Logistic Regression?
Logistic Regression is a **binary classification algorithm** that models the probability of an outcome using the **sigmoid function**:

\[
P(Y=1) = \frac{1}{1 + e^{-(\beta_0 + \beta_1X_1 + \dots + \beta_nX_n)}}
\]

It outputs a **probability score**, which is converted into a class label using a threshold (typically 0.5).

---

### Why Logistic Regression for Credit Risk?
- Produces **interpretable coefficients**
- Outputs **risk probabilities**, not just class labels
- Widely accepted in **financial and regulatory environments**
- Effective for linearly separable risk patterns

---

## How Classification Works in This Project

1. Customer features are standardized and passed into the model  
2. Each feature is multiplied by its learned coefficient  
3. The weighted sum is passed through a sigmoid function  
4. Output probability determines default classification  

This allows the model to distinguish **high-risk vs low-risk customers**.

---

## Feature Influence (Model Coefficients Insight)

From the trained Logistic Regression model:

| Feature | Coefficient Sign | Interpretation |
|------|-----------------|----------------|
| employ | Negative | Longer employment reduces default risk |
| othdebt | Negative | Higher unmanaged debt increases risk |
| address | Negative | Residential stability lowers risk |
| ed | Slight Negative | Education has marginal influence |
| debtinc | Positive | Higher debt-to-income increases default probability |

These coefficients explain **what influences default and why**, making the model suitable for real-world credit decisions.

---

## Model Evaluation
The model was evaluated using:
- Accuracy - 87%


Key focus was placed on **recall for defaulters**, ensuring high-risk customers are correctly identified.

---

## Business Impact
- Enables early detection of risky customers  
- Supports credit approval and limit decisions  
- Reduces financial loss due to defaults  
- Provides explainable, auditable predictions  

---

## Skills Demonstrated
- Data Cleaning & Preprocessing  
- Exploratory Data Analysis  
- Logistic Regression Modeling  
- Feature Interpretation  
- Financial Risk Analysis  
- Business-Oriented Decision Support  



## Author
**Priyanka K**  
MSc Data Science  
# Credit-Card-Risk-Analysis

This project aims to predict customer loan defaults using a Logistic Regression model. By analyzing a dataset of financial and demographic information, I developed a machine learning model to identify key factors that contribute to a customer defaulting on their loan. The insights from this project can help financial institutions make more informed lending decisions, ultimately reducing their risk.
