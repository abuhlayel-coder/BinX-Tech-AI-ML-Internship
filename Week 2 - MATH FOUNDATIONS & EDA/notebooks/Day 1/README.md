# Week 2 - Day 1: Descriptive Statistics

## Overview
Introduction to descriptive statistics as the foundation for exploratory data analysis: measuring the center and spread of a numeric variable before doing any modeling.

## Topics Covered
- Central tendency: mean, median, mode
- Spread: range, variance, standard deviation, IQR
- Percentiles and quartiles
- Why mean vs. median matters for skewed data

## Dataset
IMDb Top 1000 Movies (`imdb_top_1000.csv`)

## What Was Done
- Computed mean, median, mode, standard deviation, and IQR for the `No_of_Votes`-equivalent numeric column (`No_of_Votes` demo) and the IMDb `No_of_Votes` column
- Compared mean vs. median on the `No_of_Votes` column to demonstrate the effect of outliers/skew
- Justified which measure better represents a "typical" value for skewed data

## Key Takeaway
The mean is pulled toward outliers; the median is not. For right-skewed data (like Number of Votes or movie gross revenue), the median is usually the more honest measure of a "typical" value.

## Files
- `Day 1_Descriptive_Statistics.ipynb`
