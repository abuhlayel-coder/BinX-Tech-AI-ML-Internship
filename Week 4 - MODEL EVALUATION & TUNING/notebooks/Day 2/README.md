# Week 4 - Day 2: Cross-Validation

## Overview
Replaced Day 1's single validation split with **5-fold cross-validation**, using `cross_val_score` to get a mean accuracy and standard deviation across folds. Compared the result to Day 1's single-split score and confirmed stratified folds preserve class balance.

## Dataset
Breast Cancer Wisconsin dataset (`sklearn.datasets.load_breast_cancer`) — same dataset and same train/test split as Day 1. The test set from Day 1 was not touched.

## What Was Done
1. **Recreated the Day 1 split:** Same `random_state=42`, 80% train+val / 20% test, stratified.
2. **5-fold cross-validation:** Ran `cross_val_score` with the `max_depth=4` model from Day 1 on the train+val portion.
   - Fold scores: `[0.956, 0.989, 0.923, 0.923, 0.945]`
   - Mean accuracy: **0.9473**
   - Std deviation: **0.0245**
3. **Compared to Day 1:** Day 1's single-split validation accuracy was 0.9561; the cross-validated mean (0.9473) is close, differing by only ~0.009 — confirming Day 1's split wasn't a fluke, while the std (0.0245) shows how much the score varies across different data partitions.
4. **Confirmed stratification:** Verified with `StratifiedKFold` that every fold preserves the ~63%/37% class balance of the full dataset, which matters since this dataset is not perfectly balanced.

## Key Takeaway
A single validation score is one data point; cross-validation gives a distribution. The mean is a more reliable performance estimate, and the standard deviation reveals how stable (or lucky) that estimate is — something a single train/val split can never show.

## Files
- `Week4_Day2_Cross_Validation.ipynb` — fully executed notebook

## Tools Used
Scikit-learn (`cross_val_score`, `StratifiedKFold`, `RandomForestClassifier`) • Pandas • Jupyter Notebook
