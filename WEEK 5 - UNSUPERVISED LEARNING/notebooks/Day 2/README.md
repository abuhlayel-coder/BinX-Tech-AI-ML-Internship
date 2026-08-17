# Week 5 - Day 2: DBSCAN & Hierarchical Clustering

## Overview
Ran DBSCAN and hierarchical clustering on the same Wine dataset as Day 1, compared all three clustering methods side by side, and determined which fits this dataset's shape best.

## Dataset
Wine dataset (`sklearn.datasets.load_wine`) — same 178 samples, 13 scaled chemical measurements as Day 1.

## What Was Done
1. **DBSCAN** (`eps=2.0, min_samples=5`): Found 5 clusters, but flagged **85 of 178 points (48%) as noise**, with a negative silhouette score (-0.033) — a poor fit for this data.
2. **Hierarchical clustering:** Built a Ward-linkage dendrogram, cut at 3 clusters to match Day 1. Produced fairly balanced groups (64/58/56) with silhouette score **0.277** — very close to K-Means.
3. **Comparison table + side-by-side scatter plots:** All three methods plotted together on the same two features (alcohol vs. color intensity) for a direct visual comparison.
4. **Recommendation:** K-Means (silhouette 0.285) and Hierarchical (0.277) essentially tie and both clearly outperform DBSCAN. The wine chemical profiles form round, evenly-sized groups rather than irregular shapes with real outliers — exactly the data shape K-Means and Hierarchical clustering are suited for, and exactly what DBSCAN struggles with.

## Key Takeaway
No single clustering method is universally best — DBSCAN excels when data has irregular shapes and genuine outliers to flag, but on this dataset, with well-separated, similarly-sized groups, K-Means and Hierarchical clustering (which largely agree with each other) are the better fit. Comparing multiple methods with the same metric (silhouette score) is what makes that call possible, not just intuition.

## Files
- `Week5_Day2_DBSCAN_Hierarchical.ipynb` — fully executed notebook

## Tools Used
Scikit-learn (`DBSCAN`, `KMeans`, `silhouette_score`) • SciPy (`linkage`, `dendrogram`, `fcluster`) • Pandas • Matplotlib • Jupyter Notebook
