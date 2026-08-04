# Week 3 - Day 3: Logistic Regression & Classification Metrics

## Overview
Introduction to classification: predicting a category instead of a number, why accuracy alone is misleading, and how to properly evaluate a classifier using the confusion matrix, precision, recall, F1, and AUC-ROC.

## Topics Covered
- Logistic regression: weighted sum + sigmoid → probability
- Why accuracy is misleading on imbalanced data
- The confusion matrix: TP, FP, FN, TN
- Precision, recall, F1, and their trade-off
- AUC-ROC

## Dataset
Breast Cancer Wisconsin dataset (`sklearn.datasets.load_breast_cancer`) — binary classification (malignant vs. benign)

## What Was Done
- Loaded the dataset and split into features/target, then train/test split
- Trained a `LogisticRegression` model and generated predictions and class probabilities
- Built and interpreted the confusion matrix
- Computed precision, recall, and F1 with `classification_report`
- Reasoned about whether precision or recall matters more for a cancer diagnosis problem
- Computed AUC-ROC and plotted the ROC curve

## Key Takeaway
Accuracy alone can hide a model's real weaknesses, especially on imbalanced data. For a problem like cancer diagnosis, missing a real positive case (a false negative) is far more costly than a false alarm, so recall matters more than precision here — and the confusion matrix, F1, and AUC-ROC together give a much more honest picture of performance than accuracy alone.

## Files
- `day3_logistic_regression.ipynb`
