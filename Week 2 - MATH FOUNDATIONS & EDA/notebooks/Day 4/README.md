# Week 2 - Day 4: EDA Part 1 - Distributions & Outliers

## Overview
First hands-on EDA day: visualizing distributions with Seaborn and systematically detecting outliers with the IQR method.

## Topics Covered
- Why EDA comes before modeling
- Univariate plots: histogram, box plot, count plot, KDE
- Outlier detection with the IQR method (1.5x IQR rule)

## Dataset
IMDb Top 1000 Movies (`imdb_top_1000.csv`)

## What Was Done
- Cleaned `Runtime` and `Gross` columns into numeric form
- Plotted histograms for every numeric variable (rating, meta score, votes, runtime, gross)
- Plotted box plots to visually spot outliers
- Applied the IQR method to flag outliers in `No_of_Votes` and justified keeping them (genuine blockbusters, not data errors)
- Plotted count plots for `Primary_Genre` and `Certificate`, noting class imbalance (Drama dominates)

## Key Takeaway
An outlier is a question, not a verdict - investigate before deciding to keep, cap, or remove. In this dataset, "outlier" vote counts and gross revenue reflect real blockbuster status, not errors, and should be transformed (e.g. log scale) rather than dropped.

## Files
- `day4_distributions_outliers.ipynb`
