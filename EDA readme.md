# Task 5 — Exploratory Data Analysis (EDA) on Titanic Dataset

## Overview
This project is part of the **Data Analyst Internship — Task 5**.
The goal is to perform Exploratory Data Analysis (EDA) on the Titanic dataset to find **patterns, trends, and anomalies** using Python, Pandas, Matplotlib, and Seaborn.

---

## Dataset
- **Source**: Kaggle Titanic Dataset (`train.csv`)
- **Rows**: 891 passengers
- **Columns**: Passenger details such as Age, Sex, Pclass, Fare, Cabin, etc.
- **Target Variable**: `Survived` (0 = No, 1 = Yes)

---

## Steps Performed
1. **Data Loading & Overview**
   - Checked dataset shape, info, and summary statistics.
   - Identified missing values.

2. **Data Cleaning & Feature Engineering**
   - Filled missing Age values with median grouped by `Sex` and `Pclass`.
   - Filled missing Embarked with the mode (`S`).
   - Filled missing Fare with median.
   - Extracted **Title** from Name.
   - Created **FamilySize** from `SibSp` + `Parch` + 1.
   - Extracted **Deck** from Cabin.

3. **Univariate Analysis**
   - Histograms for Age and Fare.
   - Countplots for Sex and Pclass.
   - Boxplot for FamilySize.

4. **Bivariate Analysis**
   - Survival by Sex.
   - Survival by Pclass.
   - Age vs Fare colored by Survival.

5. **Multivariate Analysis**
   - Correlation heatmap of numeric features.
   - Pairplot of Age, Fare, FamilySize vs Survival.

6. **Skewness Check & Transformation**
   - Found Fare is heavily skewed.
   - Applied log transformation to normalize Fare distribution.

---

## Key Insights
1. Females had a much higher survival rate than males.
2. First-class passengers had the highest survival rates; third class had the lowest.
3. Most passengers were aged between 20–40 years; younger passengers had better chances of survival.
4. Fare is right-skewed; most fares were below 50.
5. Small families (2–4 members) survived more often than large families or solo travelers.
6. Fare and Pclass are negatively correlated.
7. Age, Fare, and FamilySize show important relationships with survival probability.

---

## Tools Used
- **Python** — Data analysis & plotting
- **Pandas** — Data manipulation
- **Matplotlib / Seaborn** — Data visualization
- **NumPy** — Numerical operations
- **SciPy** — Skewness check

---

## How to Run
1. Place `train.csv` in the same folder as the notebook.
2. Open Jupyter Notebook or Google Colab.
3. Run all cells to reproduce analysis and plots.
4. Export notebook as PDF for submission.

---

## Files in This Project
- `titanic_eda.ipynb` — Jupyter Notebook with full EDA.
- `train.csv` — Dataset used for analysis.
- `README.md` — This file with project details.
- `EDA_Report.pdf` — Exported PDF version of the analysis.

---

## Outcome
This EDA improves understanding of:
- Passenger demographics.
- Survival factors.
- Relationships between features.
- Data preprocessing for modeling.
