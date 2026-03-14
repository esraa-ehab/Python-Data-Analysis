# Python Data Analysis (EDA)

This project is a simple Exploratory Data Analysis (EDA) workflow built in a Jupyter notebook.
It uses user profile data, performs cleaning and transformation, and produces summary statistics plus visual insights.

## Project Contents

- `EDA.ipynb`: Full analysis notebook (data loading, cleaning, analysis, visualization).
- `Data/users.csv`: Dataset used in the notebook.

## What This Project Does

1. **Loads data**
   - Pulls user data from `https://dummyjson.com/users?limit=100`.
   - Saves the dataset to `Data/users.csv`.

2. **Explores the dataset**
   - Checks shape, columns, data types, missing values, duplicates, and descriptive stats.

3. **Cleans and prepares data**
   - Converts nested object-like columns (`hair`, `address`, `bank`, `company`, `crypto`) into separate normalized columns.
   - Parses `birthDate` into datetime.
   - Drops sensitive columns: `password`, `ssn`, `ein`, `ip`.
   - Fills missing values in `maidenName`.
   - Standardizes dtypes using `convert_dtypes()`.

4. **Analyzes and visualizes**
   - Average age overall and by gender.
   - Gender and city distributions.
   - Average height and weight.
   - Correlation matrix for age, height, and weight.
   - Plots for role distribution, age distribution, age groups, blood groups, city-gender split, and department-gender split.

## Insights from the Analysis

- The dataset combines demographic, physical, geographic, and company attributes, which makes it useful for multi-dimensional profiling.
- Expanding nested JSON fields into flat columns is an important step that makes filtering, grouping, and plotting much easier.
- Department and city breakdowns can reveal representation patterns that are not obvious in overall counts.
- Correlation checks (age, height, weight) provide quick validation on whether linear relationships are meaningful or weak.
- Removing sensitive personal fields early is a good privacy-first practice, even in EDA projects.