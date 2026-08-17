# Week 5 - Day 1: Unsupervised Learning & K-Means

## Overview
First unsupervised learning notebook — no target `y` was used at any point in the clustering process. Clustered wine samples with K-Means, chose the number of clusters (k) using the elbow method and silhouette score, and interpreted the resulting groups by their chemical profiles.

## Dataset
Wine dataset (`sklearn.datasets.load_wine`) — 178 samples, 13 chemical measurements (alcohol, color intensity, flavanoids, etc.). The dataset's true cultivar labels exist but were **not used for clustering** — only referenced at the end as a bonus sanity check.

## What Was Done
1. **Scaled all features** with `StandardScaler` before clustering (required since K-Means is distance-based).
2. **Elbow method:** Ran K-Means for k=1 to 10 and plotted inertia. The curve flattened noticeably after k=3, with k=4 as a secondary candidate.
3. **Silhouette score:** Compared k=3 (0.2849) vs. k=4 (0.2602) — k=3 scored higher, confirming the elbow's suggestion.
4. **Final clustering:** Fit K-Means with k=3, visualized on a 2D scatter (alcohol vs. color intensity), and examined each cluster's average chemical profile.
5. **Sanity check:** Compared the 3 clusters against the true (unused) cultivar labels — the clusters aligned strongly with the actual cultivars (e.g. cultivar 0 → 59/59 in cluster 2, cultivar 1 → 65/71 in cluster 0), suggesting K-Means found a real underlying pattern rather than noise.

## Key Takeaway
Without any labels, K-Means, guided by the elbow method and silhouette score, recovered groupings that closely matched the wine's real cultivar categories — evidence that the algorithm found genuine chemical structure in the data, not an arbitrary split.

## Files
- `Week5_Day1_KMeans.ipynb` — fully executed notebook

## Tools Used
Scikit-learn (`KMeans`, `StandardScaler`, `silhouette_score`) • Pandas • Matplotlib • Jupyter Notebook
