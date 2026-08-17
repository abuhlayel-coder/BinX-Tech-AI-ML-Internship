# Week 4 - Day 5: Scikit-learn Pipelines & Tuned Mini-Project

## Overview
Week 4's closing mini-project: combined the Day 4 engineered features, a `ColumnTransformer`, and a `RandomForestClassifier` into a single leak-free `Pipeline`, tuned end-to-end with `GridSearchCV` and 5-fold cross-validation, then evaluated once on the held-out test set.

## Dataset
Breast Cancer Wisconsin dataset (`sklearn.datasets.load_breast_cancer`) — same dataset as Day 1-4. All 30 original features are numeric; 2 engineered features from Day 4 were added (32 total).

## What Was Done
1. **Engineered features carried over:** `radius_worst_to_mean_ratio` and `concavity_per_area`, applied identically to train and test.
2. **Pipeline + ColumnTransformer:** A `ColumnTransformer` scales all numeric columns, feeding into a `RandomForestClassifier`, both wrapped in a single `Pipeline` object.
3. **Baseline:** Untuned pipeline, 5-fold CV mean f1: **0.9649**.
4. **GridSearchCV on the whole pipeline:** Tuned `model__n_estimators`, `model__max_depth`, `model__min_samples_split` using the `step__param` syntax. Best params: `{max_depth: 10, min_samples_split: 5, n_estimators: 100}`, best CV f1: **0.9684**.
5. **Final held-out evaluation (once):** Test f1 **0.9655**, test accuracy **0.9561**.
6. **Reflection (Markdown cell):** Explained why wrapping preprocessing inside the pipeline makes leakage structurally impossible — the scaler is only ever fit on training data, refit independently per cross-validation fold.
7. **Results visualized:**
   - **Confusion matrix** — shows exactly where the 114 test predictions landed, including false negatives, which matter more than accuracy alone on a medical dataset.
   - **ROC curve (AUC)** — shows class separation across all thresholds, not just the default cutoff.
   - **Feature importance (top 10)** — one of the Day 4 engineered features, `radius_worst_to_mean_ratio`, ranked 8th, confirming it contributed real signal rather than just added noise.
   - **Week 4 score progression chart** — a single bar chart tracking the score from Day 1 through Day 5 to show the week's overall arc.

## Key Takeaway
A `Pipeline` chains preprocessing and modeling into one object, so scaling is always fit on training data only — during cross-validation, each fold refits it independently, and the test set is transformed the same way at the very end. This removes leakage risk structurally instead of relying on remembering to do it manually, and is the exact professional workflow the Phase 3 capstone requires.

## Week 4 Summary
Train/val/test discipline (Day 1) → cross-validation for reliable estimates (Day 2) → bias-variance diagnosis and regularization (Day 3) → feature engineering and systematic tuning (Day 4) → all combined into one leak-free, tuned pipeline (Day 5).

## Files
- `day5_Pipeline_Mini_Project.ipynb` — fully executed notebook

## Tools Used
Scikit-learn (`Pipeline`, `ColumnTransformer`, `GridSearchCV`, `RandomForestClassifier`) • Pandas • Matplotlib • Jupyter Notebook
