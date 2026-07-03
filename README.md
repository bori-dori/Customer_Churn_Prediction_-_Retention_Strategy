# Customer Churn Prediction & Retention Strategy

## Project Overview

Customer churn is one of the biggest challenges for subscription-based businesses because acquiring new customers is significantly more expensive than retaining existing ones.

This project develops a machine learning model to identify customers who are likely to churn and provides data-driven retention strategies based on the most influential churn factors.

---

## Business Problem

The objective is to predict whether a customer will churn using historical customer information.

Early identification of high-risk customers enables businesses to:

- Reduce customer attrition
- Improve retention campaigns
- Allocate marketing resources more efficiently
- Increase customer lifetime value

---

## Dataset

The dataset contains customer demographic information, service usage, billing information, and customer behavior.

Target variable:

- Churn (Yes / No)

Features include:

- Customer demographics
- Service plans
- Usage behavior
- Monthly charges
- Equipment information
- Customer support activity

---

## Project Workflow

1. Data Loading
2. Exploratory Data Analysis (EDA)
3. Statistical Feature Selection
   - Chi-Square Test
   - Kruskal-Wallis Test
4. Correlation Analysis
5. Data Preprocessing
   - Missing value imputation (KNN Imputer)
   - One-Hot Encoding
   - Train/Test Split
6. Class Imbalance Handling (SMOTE)
7. Random Forest Model Development
8. Hyperparameter Tuning (Randomized Search)
9. Model Evaluation
10. Feature Importance Analysis
11. Business Recommendations

---

## Feature Engineering

The following preprocessing steps were performed:

- Removed statistically insignificant variables
- Removed highly correlated numerical features
- Excluded high-cardinality categorical variables
- One-Hot Encoded categorical variables
- Imputed missing numerical values using KNN Imputer
- Applied SMOTE to address class imbalance

---

## Models Evaluated

Five Random Forest-based models were compared.

| Model | Description |
|--------|-------------|
| Baseline Random Forest | Default model |
| Random Forest + Class Weight | Adjusted for class imbalance |
| Random Forest + Randomized Search | Hyperparameter tuning |
| Random Forest + SMOTE | Oversampling minority class |
| Random Forest + SMOTE + Randomized Search | Combined balancing and tuning |

Models were evaluated using:

- Precision
- Recall
- F1-score
- ROC-AUC

---

## Key Findings

- Customer tenure was the strongest predictor of churn.
- Equipment age also showed high predictive importance.
- Customer usage behavior and recurring charges contributed significantly to churn prediction.
- Applying SMOTE substantially improved Recall, making the model more effective at identifying customers likely to churn.

---

## Business Recommendations

Based on the model findings:

- Prioritize retention efforts for customers with short tenure.
- Monitor customers with aging equipment.
- Identify customers showing declining service usage.
- Develop proactive retention campaigns for high-risk customers predicted by the model.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- Imbalanced-learn (SMOTE)

---

## Skills Demonstrated

- Exploratory Data Analysis (EDA)
- Statistical hypothesis testing
- Feature selection
- Missing value imputation
- Handling imbalanced datasets (SMOTE)
- Random Forest modeling
- Hyperparameter tuning
- Model evaluation
- Business insight generation

