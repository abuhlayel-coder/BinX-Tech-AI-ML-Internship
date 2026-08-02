# Week 2 - Day 5: EDA Part 2 - Correlation & Data Storytelling

## Overview
Final EDA day of the week: bivariate relationships, correlation, and assembling the whole week's work into one complete, narrated EDA notebook.

## Topics Covered
- Bivariate analysis: scatter plots, grouped box plots
- Correlation and the correlation heatmap
- Correlation is not causation
- Pairplots for scanning all relationships at once
- Data storytelling - communicating findings, not just charts

## Dataset
IMDb Top 1000 Movies (`imdb_top_1000.csv`)

## What Was Done
- Plotted `No_of_Votes` vs `Gross` (scatter) and `IMDB_Rating` by genre (grouped box plot)
- Built a correlation matrix and heatmap across all numeric columns
- Generated a pairplot to scan all pairwise relationships
- Identified the strongest relationships and discussed their modeling implications
- Assembled descriptive stats, distributions, outlier handling, and correlation into a single full EDA notebook

## Key Takeaway
Correlation reveals strength and direction of a linear relationship, never causation. The full EDA notebook from today is the reusable template for every future project: clean -> describe -> visualize -> detect outliers -> examine relationships -> narrate findings.

## Files
- `day5_full_eda.ipynb`
