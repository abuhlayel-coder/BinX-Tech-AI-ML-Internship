# Week 4 - Day 3: Bias-Variance & Diagnosing Model Fit

## Overview
Deliberately built an overfit model and an underfit model, diagnosed each using the train-vs-validation score gap, then applied regularization to shrink the gap on the overfit case.

## Dataset
Breast Cancer Wisconsin dataset (`sklearn.datasets.load_breast_cancer`) — same dataset and same train/validation/test split as Day 1.

## What Was Done
1. **Overfit model:** An unrestricted `DecisionTreeClassifier` (`max_depth=None`) reached 1.0000 training accuracy vs. 0.9561 validation accuracy — a gap of 0.0439, the overfitting signature.
2. **Underfit model:** A `DecisionTreeClassifier` restricted to `max_depth=1` scored 0.9267 train / 0.8947 validation — both low and close together, the underfitting signature.
3. **Regularization applied:** Compared `LogisticRegression` with weak regularization (`C=1e6`, gap 0.0439) to strong regularization (`C=0.01`, gap 0.0145). Strong regularization clearly shrank the train-validation gap.
4. **Visualization:** Plotted train vs. validation accuracy across a range of `C` values to show the bias-variance trade-off directly.
5. **Reflection (Markdown cells):** Documented each diagnosis and the regularization fix with score evidence.

## Key Takeaway
The train-vs-validation gap is the core diagnostic tool for model fit: a large gap signals overfitting (high variance), while low scores on both signal underfitting (high bias). Regularization trades a small amount of training accuracy for a smaller gap — i.e., it reduces variance at the cost of a bit more bias.

## Files
- `day3_Bias_Variance.ipynb` — fully executed notebook (includes a saved regularization plot)

## Tools Used
Scikit-learn (`DecisionTreeClassifier`, `LogisticRegression`, `StandardScaler`) • Pandas • Matplotlib • Jupyter Notebook
