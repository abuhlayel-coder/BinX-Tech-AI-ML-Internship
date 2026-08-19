# Week 5 - Day 4: t-SNE & Anomaly Detection

## Overview
Visualized the Wine dataset with t-SNE, compared it directly against Day 3's PCA visualization, then used Isolation Forest to detect anomalies and inspected what made two flagged points unusual.

## Dataset
Wine dataset (`sklearn.datasets.load_wine`) — same 178 samples, 13 scaled chemical measurements as Day 1-3. True cultivar labels used only for plot coloring, never fed into t-SNE or Isolation Forest.

## What Was Done
1. **t-SNE visualization:** Reduced the 13 features to 2D using t-SNE (`perplexity=30`), colored by true cultivar for reference.
2. **PCA vs. t-SNE comparison:** Placed both 2D visualizations side by side. t-SNE produced tighter, more distinctly separated cultivar clusters (it optimizes for local neighborhoods), while PCA's clusters were a bit more spread since it optimizes for global variance instead.
3. **Isolation Forest:** Ran with `contamination=0.05`, flagging **9 of 178 points (5.1%)** as anomalies — matching the requested 5% target.
4. **Inspected two flagged points:** Point 59 had unusually low ash (1.36 vs. dataset average 2.37) and low alcalinity of ash (10.60 vs. 19.49); point 69 had unusually high magnesium (151 vs. average 99.74). Both sit well outside the typical range for at least one chemical measurement, explaining why Isolation Forest isolated them quickly.

## Key Takeaway
PCA and t-SNE both reduce dimensions for visualization but optimize for different things — PCA preserves global variance with interpretable axes, t-SNE preserves local neighborhoods with axes that carry no independent meaning. Isolation Forest's anomaly flags are conceptually the same idea as DBSCAN's noise points from Day 2: both are ways of identifying data that sits apart from the dense "normal" mass, just using different methods.

## Files
- `day4_TSNE_Anomaly_Detection.ipynb` — fully executed notebook

## Tools Used
Scikit-learn (`TSNE`, `IsolationForest`, `PCA`) • Pandas • Matplotlib • Jupyter Notebook
