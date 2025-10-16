# DA5401 - Assignment 6

**Name:** Ojas Phadake
**Roll No:** CH22B007

---

## Repository Contents

This repository contains the solutions for **Assignment 6** of the course **DA5401**.
The assignment focuses on **handling missing data**, **data imputation**, and analyzing the effect of different imputation strategies on classification performance using **Logistic Regression**.

* **DA5401_CH22B007_Assignment6.ipynb** → Jupyter Notebook containing complete code, results, and performance analysis for all imputation techniques.
* **DA5401_CH22B007_Assignment6 PDF.pdf** → PDF export of the notebook for submission and easy reference.

---

## Problem Statement

The objective of this assignment is to explore and compare various strategies for dealing with **missing data** in a real-world dataset and analyze their impact on model performance.

Specifically, four datasets were prepared using different strategies:

1. **Model A — Median Imputation:** Missing values replaced with the median of the feature.
2. **Model B — Linear Regression Imputation:** Missing values predicted using a linear regression model trained on other features.
3. **Model C — Non-linear Regression Imputation:** Imputation performed using non-linear regression (e.g., Random Forest).
4. **Model D — Listwise Deletion:** Rows containing missing values were dropped entirely.

---

## Tasks Performed

* Introduced missingness into selected numerical columns.
* Implemented various imputation methods (median, linear regression, non-linear regression).
* Trained and evaluated Logistic Regression models on each version of the dataset.
* Compared model performance using **Accuracy**, **Precision**, **Recall**, and **F1-score**.
* Discussed the conceptual implications of each method in the context of **MAR (Missing At Random)** assumptions.

---

## Key Insights

* **Imputation methods** generally preserved more information than **Listwise Deletion**, leading to better model generalization.
* **Non-linear regression imputation (Model C)** outperformed linear imputation when relationships between features were non-linear, better capturing feature interactions.
* **Listwise Deletion (Model D)** often led to reduced training data and biased estimates, even if its model appeared simpler or cleaner.
* The **MAR assumption** underlies regression-based imputations — implying that missingness depends only on observed data.

---

## Conclusion

In this study, **Non-linear Regression Imputation (Model C)** emerged as the most effective approach, balancing performance and conceptual soundness.
Regression-based imputation methods should be preferred when feature relationships are complex, while simple median imputation may suffice for linear or small datasets.
Listwise Deletion should be avoided unless missingness is minimal or completely random.