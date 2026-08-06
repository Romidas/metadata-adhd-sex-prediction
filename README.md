# Metadata-Based ADHD and Sex Prediction using Machine Learning

## Overview

This repository contains my contribution to a collaborative MSc Data Science project investigating whether demographic, behavioural, clinical questionnaire and MRI metadata can be used to predict:

- ADHD diagnosis
- Biological sex

Two complementary modelling approaches were used:

- **LightGBM** for predictive modelling
- **Logistic Regression** for statistical inference

Model interpretation was performed using **SHAP (SHapley Additive exPlanations)**, while logistic regression assumptions were assessed using **Box–Tidwell tests** and **Variance Inflation Factors (VIFs)**.

---

## Research Question

> Can demographic, behavioural and MRI metadata accurately predict ADHD diagnosis and biological sex?

---

## Workflow

```
Metadata
      │
      ▼
Data Preprocessing
      │
      ├── Missing Value Imputation
      ├── Rare Category Merging
      ├── One-Hot Encoding
      └── Ordinal Encoding
      │
      ▼
LightGBM
      │
      ├── Cross-validation
      ├── Performance Evaluation
      └── SHAP Interpretation
      │
      ▼
Logistic Regression
      │
      ├── Assumption Checking
      ├── Odds Ratios
      └── Model Diagnostics
```

---

## Dataset

The metadata consisted of:

- Demographic variables
- Behavioural questionnaire scores
- Clinical metadata
- MRI acquisition metadata

The original dataset contained:

- **1,213 participants**
- **24 metadata variables**

The dataset is **not included** in this repository due to licensing and privacy restrictions.

---

## Methods

### Data Preprocessing

- Rare category merging
- Iterative imputation for numerical variables
- Mode imputation for categorical variables
- One-hot encoding
- Ordinal treatment of Barratt education and occupation variables

### Predictive Modelling

- LightGBM
- Stratified 5-fold Cross Validation
- SHAP feature importance

### Statistical Modelling

- Logistic Regression
- Box–Tidwell Test
- Variance Inflation Factor (VIF)
- Likelihood Ratio Test
- McFadden Pseudo R²

---

## Results

| Task | ROC-AUC | Interpretation |
|------|--------:|---------------|
| ADHD Prediction | **0.81** | Reasonable discrimination |
| Sex Prediction | **0.61** | Weak discrimination |

Key findings:

- Behavioural questionnaire variables were the strongest contributors to ADHD prediction.
- LightGBM outperformed logistic regression for predictive performance.
- Logistic regression provided interpretable associations but demonstrated limited explanatory power.
- Metadata alone was insufficient for accurate biological sex prediction.

---

## Repository Structure

```
metadata-adhd-sex-prediction/
│
├── notebooks/
├── report/
├── figures/
├── data/
├── README.md
└── requirements.txt
```

---

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- LightGBM
- SHAP
- Statsmodels
- Matplotlib

---

## My Contribution

This repository contains **my contribution** to a collaborative MSc Data Science project.

My responsibilities included:

- Metadata preprocessing
- Missing value imputation
- Feature engineering
- LightGBM model development
- SHAP-based model interpretation
- Logistic regression modelling
- Model diagnostics and statistical inference
- Results interpretation and reporting

---

## Future Work

Potential improvements include:

- Integration of MRI-derived imaging features
- Multiple imputation instead of single iterative imputation
- External validation on an independent dataset
- Comparison with additional machine learning algorithms

---

## License

This project is released under the MIT License.
