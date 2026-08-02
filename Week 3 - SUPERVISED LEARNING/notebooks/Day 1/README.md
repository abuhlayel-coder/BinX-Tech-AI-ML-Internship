# Week 3 - Day 1: Supervised Learning Concepts & the Scikit-learn API

## Overview
Introduction to supervised learning as the foundation for Phase 2: understanding how models learn from labeled data, the difference between regression and classification, and the consistent workflow scikit-learn uses to train and evaluate every model.

## Topics Covered
- What supervised learning is: learning from labeled examples
- Regression vs. classification
- Features (X) and target (y)
- The scikit-learn API: instantiate, fit, predict, score
- The train/test split and why it matters

## Dataset
Diabetes dataset (`sklearn.datasets.load_diabetes`)

## What Was Done
- Loaded the dataset and separated it into features (`X`) and target (`y`)
- Performed an 80/20 train/test split with a fixed `random_state`
- Verified the shapes of `X_train`, `X_test`, `y_train`, `y_test` were consistent
- Explained in Markdown why the model must never see the test set during training

## Key Takeaway
Never evaluate a model on the same data it was trained on. A model can memorize its training data and look perfect, yet fail completely on new data — splitting the data into train and test sets is the only honest way to estimate real-world performance.

## Files
- `Week3_Day1_Supervised_Learning_Basics.ipynb`
