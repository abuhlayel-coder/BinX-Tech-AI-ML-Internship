# Week 1 Mini-Project — Integrated Notebook

The Week 1 capstone: a single notebook that runs the full **load → process → visualize** pipeline using NumPy, Pandas, and Matplotlib together — the same pipeline shape every project in this program follows.

**Objectives**
- Load and clean a real dataset with Pandas
- Compute at least one derived numeric feature or summary statistic with NumPy
- Produce at least three labeled plots, including a histogram and a scatter plot
- Explain what each visualization reveals in Markdown

**Dataset:** [`titanic.csv`](../titanic.csv)

**Completed**
- Loaded and cleaned the Titanic dataset (same approach as Day 4: median-filled age, mode-filled embarked/embark_town, dropped deck)
- Used NumPy to engineer a `family_size` feature and a `fare_zscore` to flag unusually high fares
- Produced four labeled plots: age distribution (histogram), age vs. fare colored by survival (scatter), survival rate by class (bar), and a subplot comparing survival rate by family size against the fare distribution
- Documented findings in Markdown for each plot — fare/class was strongly tied to survival, and mid-sized families survived at higher rates than solo travelers or very large families

**Notebook:** [`Mini-Project.ipynb`](./Mini-Project.ipynb)