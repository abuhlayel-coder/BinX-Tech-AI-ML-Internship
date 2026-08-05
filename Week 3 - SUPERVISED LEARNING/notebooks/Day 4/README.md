# Week 3 - Day 4: Trees, Forests, SVMs & k-NN

## Overview
Comparing four different classification algorithms on the same problem: decision trees, random forests, support vector machines, and k-nearest neighbors, training them fairly on the same split and metric, then interpreting which one wins and why.

## Topics Covered
- Decision trees: interpretable rules, prone to overfitting
- Random forests: ensembles of trees and feature importances
- Support Vector Machines and the margin
- k-Nearest Neighbors
- Fair model comparison (the "no free lunch" principle)

## Dataset
Breast Cancer Wisconsin dataset (`sklearn.datasets.load_breast_cancer`) same features/target and train/test split as Day 3, for a fair comparison

## What Was Done
- Reused the exact Day 3 train/test split
- Trained a Decision Tree, Random Forest, SVM, and k-NN on identical data
- Compared all four on Accuracy, Precision, Recall, and F1-score in one table
- Reported and visualized the Random Forest's top 10 feature importances
- Identified the best-performing model and explained why it likely won

## Key Takeaway
Random Forest was the top performer (F1 ≈ 0.972), narrowly ahead of k-NN and SVM, with the plain Decision Tree trailing slightly. This matches expectations: the ensemble approach smooths out the overfitting risk a single tree carries, while still handling this dataset's moderate size and dimensionality well. The strongest features driving predictions were `worst area` and `worst concave points`, both measures of tumor size and shape irregularity, which lines up with medical intuition that larger, more irregularly-shaped masses are more likely to be malignant. No single algorithm wins by default; comparing several fairly on the same split and metric is what makes the result trustworthy.

## Files
- `day4_trees_forests_svm_knn.ipynb`
