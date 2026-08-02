# Week 2 - Statistics, Probability, Linear Algebra & EDA

## Overview
Week 2 of the BinX Tech AI & ML Internship builds the mathematical and analytical foundation for machine learning: descriptive statistics, probability, linear algebra, and hands-on exploratory data analysis (EDA).

## Dataset
IMDb Top 1000 Movies (`imdb_top_1000.csv`) - used consistently across all five days.

## Daily Breakdown

| Day | Topic | Focus |
|---|---|---|
| [Day 1] | Descriptive Statistics | Mean, median, mode, spread, mean vs. median on skewed data |
| [Day 2] | Probability & Distributions | Conditional probability, Bayes' theorem, normal/binomial/uniform distributions |
| [Day 3] | Linear Algebra for ML | Vectors, matrices, dot product, matrix multiplication, shape errors |
| [Day 4] | EDA Part 1 | Univariate distributions and outlier detection with Seaborn |
| [Day 5] | EDA Part 2 | Bivariate analysis, correlation, full assembled EDA notebook |

## Tools & Libraries
NumPy, Pandas, Matplotlib, Seaborn 0.13.2, Jupyter Notebook, Python 3.13

## Key Takeaways From the Week
- Statistics (mean/median/spread) describe a dataset; probability describes uncertainty about it; linear algebra is how models actually compute predictions from it - EDA ties all three together into practice.
- Skewed data (votes, gross revenue) makes the median more trustworthy than the mean.
- Outliers require investigation, not automatic removal.
- Correlation shows relationship strength, never causation.
- A complete EDA notebook (stats -> distributions -> outliers -> relationships -> narrative) is the reusable template for every future project.

## Repository Structure
```
Week 2/
  Day 1/
    day1_descriptive_statistics.ipynb
    README.md
  Day 2/
    day2_probability_distributions.ipynb
    README.md
  Day 3/
    day3_linear_algebra.ipynb
    README.md
  Day 4/
    day4_distributions_outliers.ipynb
    README.md
  Day 5/
    day5_full_eda.ipynb
    README.md
  README.md
```
