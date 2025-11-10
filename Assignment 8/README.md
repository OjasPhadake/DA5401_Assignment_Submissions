# **DA5401 - Assignment 8: Ensemble Regression — Bias and Variance Trade-off**

**Name:** Ojas Phadake
**Roll No:** CH22B007

---

## **Repository Contents**

This repository contains the complete code, analysis, and discussion for Assignment 8 of the course **DA5401**.
The assignment explores the principles of **ensemble learning** for regression — Bagging, Boosting, and Stacking — applied to the **UCI Bike Sharing Demand** dataset.

* **DA5401_CH22B007_Assignment_8.ipynb** → Jupyter Notebook with preprocessing, model training, and evaluation.
* **DA5401_CH22B007_Assignment_8 - PDF.pdf** → PDF export of the notebook for submission.

---

## **Problem Statement**

The objective was to **predict hourly bike rental counts (`cnt`)** using advanced ensemble methods and study how each reduces bias or variance.
The task involved building multiple models and comparing their RMSE to identify the most generalizable approach.

---

## **Tasks Performed**

* **Data Preprocessing:** Loaded `hour.csv`, checked nulls/duplicates, dropped irrelevant columns, and performed One-Hot Encoding on categorical variables.
* **Baseline Models:** Implemented **Linear Regression** and **Decision Tree (depth=6)** for initial comparison.
* **Bagging (Variance Reduction):** Averaged multiple trees using **Bagging Regressor** to improve stability.
* **Boosting (Bias Reduction):** Used **Gradient Boosting Regressor** to iteratively correct residual errors.
* **Stacking (Optimal Combination):** Combined **KNN**, **Bagging**, and **Gradient Boosting** as base learners with a **Ridge Regression** meta-learner.
* **Visualization:** Created correlation heatmaps, residual plots, and an RMSE comparison bar chart.

---

## **Key Results**

| Model                        | Test RMSE |
| ---------------------------- | --------- |
| Linear Regression (Baseline) | 100.45    |
| Decision Tree (max_depth=6)  | 118.43    |
| Bagging Regressor            | 112.33    |
| Gradient Boosting Regressor  | 78.97     |
| **Stacking Regressor**       | **56.03** |

---

## **Insights and Conclusion**

* The **Stacking Regressor** achieved the lowest RMSE (**56.03**), outperforming all other models.
* **Bagging** reduced variance but did not lower bias enough.
* **Boosting** effectively reduced bias by sequentially learning from residuals.
* **Stacking** combined the strengths of all three — leveraging model diversity and meta-learning to minimize both bias and variance.
* The results confirm that stacking provides the most robust and generalizable predictions for bike rental demand forecasting.