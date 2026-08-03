# Week 3 - Day 2: Linear Regression & Regression Metrics

## Overview
Introduction to linear regression as the first supervised learning model: fitting a straight line to predict a continuous number, interpreting what the model learned, and evaluating it with proper regression metrics against a baseline.

## Topics Covered
- How linear regression predicts a continuous number (weighted sum + bias)
- Training and predicting with `LinearRegression`
- Interpreting coefficients and the intercept
- Regression metrics: MAE, RMSE, R²
- Why a model must be compared against a baseline (predicting the mean)

## Dataset
Diabetes dataset (`sklearn.datasets.load_diabetes`)

## What Was Done
- Reused the Day 1 features/target split (`X`, `y`) and train/test split
- Trained a `LinearRegression` model on the training data
- Reported the model's coefficients and identified the feature with the strongest effect (`bmi`)
- Evaluated the model on the test set using MAE, RMSE, and R²
- Built a baseline that predicts the mean of `y_train` for every row, and compared its RMSE against the model's RMSE
- Documented the interpretation of the results in Markdown

## Key Takeaway
A model's metrics mean nothing on their own — they only matter relative to a baseline. This model's RMSE beat the mean-prediction baseline, confirming it learned a real, useful pattern rather than just guessing the average. Its R² (~0.45–0.5) shows it explains a meaningful but incomplete share of the variance in disease progression, with `bmi` and `s5` standing out as the strongest predictors.

## Files
- `day2_linear_regression.ipynb`
