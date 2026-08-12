# Week 4 - Day 4: Feature Engineering & Hyperparameter Tuning

## Overview
Engineered two new features from the raw measurements, defined a hyperparameter grid for a `RandomForestClassifier`, tuned it with `GridSearchCV` + 5-fold cross-validation, and compared the tuned result against an untuned baseline.

## Dataset
Breast Cancer Wisconsin dataset (`sklearn.datasets.load_breast_cancer`) — same dataset and split as Day 1-3.

## What Was Done
1. **Engineered features:**
   - `radius_worst_to_mean_ratio` — how much a tumor's largest radius exceeds its mean radius (captures size irregularity).
   - `concavity_per_area` — mean concavity normalized by area (captures shape irregularity independent of tumor size).
2. **Baseline:** Untuned `RandomForestClassifier` (default hyperparameters, original features) — 5-fold CV mean f1: **0.9630**.
3. **Hyperparameter grid:** `n_estimators` [100, 200, 300], `max_depth` [4, 6, 10, None], `min_samples_split` [2, 5] — 24 combinations × 5 folds.
4. **GridSearchCV result:** Best params `{max_depth: 4, min_samples_split: 2, n_estimators: 300}`, best cross-validated f1: **0.9676**.
5. **Comparison:** Tuned model improved over baseline by **+0.0046** f1.
6. **Reflection (Markdown cells):** Justified each engineered feature and discussed whether feature engineering or hyperparameter tuning contributed more to the improvement.

## Key Takeaway
`GridSearchCV` systematically searches a hyperparameter grid using cross-validation, so the chosen settings are based on a reliable estimate rather than a single lucky split — directly building on the Day 1-2 lessons about validation reliability. Feature engineering and hyperparameter tuning are complementary: better features give the model better raw material, while tuning finds the best way to use it.

## Files
- `Week4_Day4_Feature_Engineering_GridSearchCV.ipynb` — fully executed notebook

## Tools Used
Scikit-learn (`GridSearchCV`, `RandomForestClassifier`, `cross_val_score`) • Pandas • Jupyter Notebook
