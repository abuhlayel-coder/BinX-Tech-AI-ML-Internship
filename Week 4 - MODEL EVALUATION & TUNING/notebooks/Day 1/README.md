# Week 4 - Day 1: Train / Validation / Test Splits

## Overview
Moved beyond the simple train/test split used in Week 3 to a proper **three-way split**: train, validation, and test. Tuned a hyperparameter using only the validation set, then evaluated the final model on the test set exactly once.

## Dataset
Breast Cancer Wisconsin dataset (`sklearn.datasets.load_breast_cancer`) — 569 samples, 30 features, binary classification. Reused from Week 3, Day 3.

## What Was Done
1. **Three-way split (60/20/20):** Two calls to `train_test_split` — first carved off the test set (20%), then split the remainder into train (60%) and validation (20%), both stratified by target.
2. **Hyperparameter tuning on validation only:** Trained a `RandomForestClassifier` across four `max_depth` values (2, 4, 6, None), comparing accuracy on the validation set only. Best: `max_depth=4` (validation accuracy 0.9561).
3. **Final evaluation:** Retrained with the chosen `max_depth`, then evaluated on the test set exactly once — final test accuracy **0.9474**.
4. **Reflection (Markdown cells):** Explained why tuning against the test set would produce a misleading, overly optimistic score, and why even a single validation set can be unreliable on smaller datasets (motivating cross-validation, Day 2).

## Key Takeaway
The test set is opened exactly once, after every modeling decision is final. Using it repeatedly during tuning causes information to leak into your choices, so the reported score stops reflecting true generalization performance.

## Files
- `Week4_Day1_Train_Val_Test_Split.ipynb` — fully executed notebook

## Tools Used
Scikit-learn (`train_test_split`, `RandomForestClassifier`) • Pandas • Jupyter Notebook
