# Day 4 — Pandas: Tabular Data

Worked with real, messy tabular data using Pandas — the standard tool for loading, cleaning, and exploring datasets.

**Objectives**
- Load a real dataset into a DataFrame and inspect its structure
- Select columns and filter rows by condition
- Clean missing values and duplicates with a documented rationale
- Aggregate data with `groupby`

**Topics Covered**
- Series vs. DataFrame
- Loading and inspecting data (`read_csv`, `head`, `info`, `describe`)
- Selecting and filtering (`.loc`, `.iloc`, boolean filtering)
- Cleaning data (missing values, duplicates, type conversion)
- Grouping and aggregation (`groupby`, `agg`)

**Dataset:** [`titanic.csv`](../titanic.csv) — the classic Titanic passenger dataset, chosen for its real missing values and clear categorical groupings.

**Completed**
- Loaded the Titanic dataset and reported its shape, columns, and dtypes
- Counted missing values per column and handled each with a documented justification (median fill for age, mode fill for embarked/embark_town, dropped deck)
- Filtered to a meaningful subset (female passengers in 1st/2nd class) and interpreted the survival rate difference
- Used `groupby` on class and sex to find survival rate patterns

**Notebook:** [`day4_pandas.ipynb`](./day4_pandas.ipynb)