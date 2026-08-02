# Week 2 - Day 3: Linear Algebra for ML

## Overview
The vector/matrix representation of data and the operations (dot product, matrix multiplication) that models use to generate predictions.

## Topics Covered
- Vectors as a single data sample's features
- Matrices as a full dataset (samples x features)
- The dot product and its role in linear model predictions
- Matrix multiplication and the shape-matching rule

## Dataset
IMDb Top 1000 Movies (`imdb_top_1000.csv`)

## What Was Done
- Represented three movies (rating, meta score, runtime) as a (3x3) NumPy matrix
- Computed a weighted score for one movie by hand, then verified with `np.dot`
- Used `@` to compute scores for all three movies in a single matrix multiplication
- Deliberately triggered a shape-mismatch `ValueError` and explained the cause and fix

## Key Takeaway
A model's prediction is a weighted sum of features - the dot product. Matrix multiplication applies this across an entire dataset at once, and the inner-dimension rule (columns of X must match length of the weight vector) is the source of most shape errors in ML code.

## Files
- `day3_linear_algebra.ipynb`
