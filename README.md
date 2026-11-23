# Kaggle Competitions & ML Projects

A collection of machine learning competitions and hackathon projects covering tabular data, imbalanced classification, financial modeling, clinical early-warning systems, and structural biology.

## Table of Contents

- [Kaggle ISIC 2024 — Skin Cancer Detection](#kaggle-isic-2024--skin-cancer-detection)
- [Jane Street Market Prediction](#jane-street-market-prediction)
- [PHEMS Hackathon — Early Sepsis Prediction](#phems-hackathon--early-sepsis-prediction)
- [RNA Folding — 3D Structure Prediction](#rna-folding--3d-structure-prediction)


---

## Kaggle ISIC 2024 — Skin Cancer Detection
### Contributors

| [Ioannis Demetriades](https://github.com/IoannisDem) | [Marios Kyriacou](https://github.com/marioskyriacou) |
| :---: | :---: |
Skin cancer detection using the **ISIC 2024** dataset, structured across two phases:

- **Phase A — Image Classification:** Exploratory work and modeling on dermatoscopic skin lesion images.
- **Phase B — Tabular Data Classification:**
  - **XGBoost (XGB):** Trained with hyperparameter tuning and repeated stratified K-fold cross-validation to handle severe class imbalance reliably.
  - **Artificial Neural Network (ANN):** Used a ratio matrix split to undersample the majority class alongside **SMOTE** to oversample the minority class for improved class balance.



---

##  Jane Street Market Prediction

Built machine learning models using real-world market data derived from Jane Street's production trading systems. This project addresses core quantitative modeling challenges, including fat-tailed return distributions, non-stationary time series, and abrupt market regime shifts.

## Dataset Overview

The dataset consists of historical market features and return responders stored in partitioned Parquet files (`train.parquet`, split into 10 parts):

| Column(s) | Description |
| :--- | :--- |
| `date_id`, `time_id` | Ordinally sorted integers providing chronological structure (intervals between `time_id` values may vary) |
| `symbol_id` | Unique identifier for each financial instrument |
| `weight` | Sample weight used in the competition evaluation metric |
| `feature_{00...78}` | 79 anonymized market data features |
| `responder_{0...8}` | 9 anonymized target responders clipped to `[-5, 5]` |

- **Prediction Target:** `responder_6`

- **Modeling Approach**

- **XGBoost (XGB):** Gradient boosted decision trees trained to capture non-linear feature interactions across anonymized market signals while accounting for sample weights.
- **Random Forest:** Ensemble bagging baseline used to evaluate variance reduction and feature importance under noisy, non-stationary financial data.

---

## PHEMS Hackathon — Early Sepsis Prediction

Developed a machine learning model using **XGBoost** for early prediction of sepsis from clinical/hackathon data.

- **Model:** XGBoost
- **Objective:** Early detection of sepsis to support timely clinical intervention
---

## RNA Folding — 3D Structure Prediction

Developed machine learning models to predict the 3D structure of Ribonucleic Acid (RNA) molecules directly from their nucleotide sequences, capturing the structural conformations that govern biological function.

- **Input:** RNA sequence
- **Target:** 3D molecular structure coordinates / structural representation


---




## Repository Structure

```text
.
├── isic-2024/
├── jane-street/
├── phems-sepsis-hackathon/
├── rna-fold/
└── README.md
```
