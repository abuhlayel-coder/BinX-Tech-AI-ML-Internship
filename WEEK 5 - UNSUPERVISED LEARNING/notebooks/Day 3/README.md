# Week 5 - Day 3: Dimensionality Reduction with PCA

## Overview
Applied PCA to the Wine dataset to see how much of the 13-dimensional chemical data can be captured in fewer dimensions, chose a component count that retains ~95% of the variance, and visualized the data in 2D.

## Dataset
Wine dataset (`sklearn.datasets.load_wine`) — same 178 samples, 13 scaled chemical measurements as Day 1-2. True cultivar labels used only for coloring the final plot, not for PCA itself (PCA is unsupervised).

## What Was Done
1. **Fit PCA on all 13 components** and plotted cumulative explained variance — the first component alone explains 36.2%, the first two together 55.4%.
2. **Chose the component count for 95% variance:** **10 of 13** components are needed to reach 96.2% cumulative variance — a modest reduction, showing this dataset's 13 features carry relatively little redundancy between them.
3. **Reduced to 2 components for visualization:** These 2 components alone capture 55.4% of the variance, and despite that loss, a scatter plot colored by the true cultivar labels shows the three cultivars separating into visually distinct regions.
4. **Documented the trade-off:** Preserved most of the variance that actually distinguishes the cultivars; cost the direct interpretability each original feature (like "alcohol" or "color intensity") had, since each component is now a combination of all 13 original measurements.

## Key Takeaway
PCA's value here is less about aggressive compression (13→10 for 95% variance is a modest cut) and more about visualization: reducing 13 dimensions to just 2 still preserved enough structure to visually separate the wine cultivars, even though PCA never saw those labels during fitting.

## Files
- `day3_PCA.ipynb` — fully executed notebook

## Tools Used
Scikit-learn (`PCA`, `StandardScaler`) • Pandas • Matplotlib • Jupyter Notebook
