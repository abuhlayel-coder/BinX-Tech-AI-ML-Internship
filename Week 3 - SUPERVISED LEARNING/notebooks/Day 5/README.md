# Week 3 - Day 5: End-to-End Mini-Project

## Overview
Assembling everything from Week 3 into one complete supervised-learning pipeline: EDA, preprocessing (missing values, encoding, scaling), a leakage-free train/test split, training multiple models, and evaluating them against a baseline to select and justify a final model.

## Topics Covered
- The full pipeline: EDA → preprocessing → split → modeling → evaluation
- Handling missing values with `SimpleImputer`
- One-hot encoding a categorical feature
- Feature scaling with `StandardScaler`
- Avoiding data leakage (fit on train only, transform on test)
- Choosing the right model and metric, and justifying the choice

## Dataset
Breast Cancer Wisconsin dataset (`sklearn.datasets.load_breast_cancer`), with a synthetic categorical feature (`clinic_region`) and deliberately introduced missing values added to exercise the full preprocessing stage.

## What Was Done
- Loaded the dataset and identified the task as classification (malignant vs. benign)
- Performed brief EDA: checked missing values, class balance, and two distribution plots by class
- Split the data first, then imputed missing values, one-hot encoded the categorical feature, and scaled numeric features — all fit on the training set only, applied to the test set via `.transform()`
- Trained a `DummyClassifier` baseline, Logistic Regression, and Random Forest on the identical preprocessed split
- Compared all three on Accuracy, Precision, Recall, F1, and AUC-ROC
- Selected and justified the better model

## Key Takeaway
Both real models dramatically outperformed the baseline (F1 ≈ 0.77 for always-predict-the-majority-class vs. F1 ≈ 0.97 for both trained models), confirming they learned genuine signal rather than exploiting class imbalance. Logistic Regression edged out Random Forest on F1 (0.972 vs. 0.966), while Random Forest was marginally better on AUC-ROC (0.995 vs. 0.993) — the two models are close to tied, and either would be a defensible choice. The critical discipline of this notebook wasn't the model choice, though — it was fitting every preprocessing step (imputer, encoder, scaler) on the training data only, so the test set stayed a genuinely honest, leakage-free measure of real-world performance.

## Files
- `day5_end_to_end_mini_project.ipynb`
