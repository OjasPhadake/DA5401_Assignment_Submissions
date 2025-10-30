# **DA5401 - Assignment 7: Multi-Class Model Selection**

**Name:** Ojas Phadake

**Roll No:** CH22B007

## **Repository Contents**

This repository contains the complete solutions and analysis for Assignment 7 of the course DA5401.  
The assignment focuses on advanced model evaluation techniques for multi-class classification.

* **DA5401\_CH22B007\_Assignment7.ipynb** → Jupyter Notebook containing complete code, visualizations, and conceptual analysis for model selection.  
* **DA5401\_CH22B007\_Assignment7 PDF.pdf** → PDF export of the notebook for submission.

## **Problem Statement**

The objective of this assignment was to perform a comprehensive model selection study for a multi-class, complex classification task \- classifying land cover types using the **UCI Landsat Satellite dataset** (6 classes).

The primary focus was on adapting and interpreting advanced threshold-based metrics (ROC and PRC) to identify the best and worst classifiers, rather than relying on single-point metrics like Accuracy.

## **Tasks Performed**

* **Data Preprocessing:** Standardized features (Z-score normalization) and performed a stratified Train/Test split.  
* **Baseline Training:** Trained six core classifier types: KNN, Decision Tree, Dummy (Prior), Logistic Regression, Gaussian NB, and SVC (with probability=True).  
* **Multi-Class ROC Analysis:** Implemented and plotted the **Macro-Averaged One-vs-Rest (OvR) ROC Curves** for all models, calculating the corresponding AUC scores.  
* **Multi-Class PRC Analysis:** Implemented and plotted the **Macro-Averaged One-vs-Rest (OvR) Precision-Recall Curves**, calculating the corresponding Average Precision (AP) scores.  
* **Conceptual Analysis:** Explained the implications of $\\text{AUC} \< 0.5$ and justified why PRC is superior to ROC for imbalanced classification scenarios.  
* **Ensemble Experimentation (Bonus):** Introduced and evaluated **Random Forest** and **XGBoost** to establish the upper bound of performance.

## **Key Insights**

* **Performance Hierarchy:** Non-linear models **SVC** and **KNN** consistently demonstrated superior performance across all metrics (highest F1-Score, ROC-AUC, and PRC-AP), confirming the data's complex, non-linear class boundaries.  
* **Metric Discrepancy:** The model ranking slightly shifted between ROC-AUC and PRC-AP, demonstrating that high **separability (AUC)** does not always translate to the best **Precision-Recall balance (AP)** at practical thresholds.  
* **Model Failure:** Models with low AP (like the Decision Tree and Gaussian NB) exhibited a sharp drop in Precision as Recall increased, indicating poor prediction confidence and a high volume of False Positives needed to achieve completeness.  
* **Worst-Case Baseline:** The intentionally reversed classifier confirmed the conceptual meaning of $\\text{AUC} \< 0.5$ (performing worse than random chance).

## **Final Recommendation**

Based on the synthesis of all metrics, **K-Nearest Neighbors (KNN)** or **SVC** is recommended as the best model for this task.

**Justification:** The **KNN** model achieved the highest **Weighted F1-Score** and **Macro-AP**, indicating the most robust and balanced performance for achieving both high confidence and high completeness in identifying all six land cover types. The comprehensive analysis across the entire range of thresholds ensures this model generalizes reliably.