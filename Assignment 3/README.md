# DA5401 - Assignment 3  

**Name:** Ojas Phadake  
**Roll No:** CH22B007  

---

## 📂 Repository Contents
This repository contains the solutions for **Assignment 3** of the course **DA5401**.  
The assignment focuses on handling **class imbalance** in fraud detection using clustering-based sampling techniques, and evaluating their impact on classification performance.  

- **DA5401_CH22B007_Assignment3.ipynb** → Jupyter Notebook containing the complete code, visualizations, and explanations.  
- **DA5401_CH22B007_Assignment3 PDF.pdf** → PDF export of the notebook for easy readability and submission.  

---

## 📝 Problem Statement
You are working with a highly imbalanced **credit card fraud detection dataset**, where fraudulent transactions represent only a tiny fraction of all transactions.  
Traditional classifiers achieve high accuracy by focusing on the majority class but fail to detect fraudulent cases effectively.  

The goal of this assignment is to:  
1. Explore **resampling methods** to address class imbalance.  
2. Apply **clustering-based oversampling (CBO)** and **clustering-based undersampling (CBU)** to create more representative training sets.  
3. Compare these approaches with **baseline (imbalanced)** training and **naive oversampling (SMOTE)**.  
4. Train and evaluate a **Logistic Regression classifier** on each dataset.  
5. Analyze performance using **Precision, Recall, and F1-score** for the **minority class (fraudulent transactions)**.  

---

## 🚀 Key Steps
- **Data Preprocessing**: Splitting into train/test sets and handling imbalance.  
- **Baseline Model**: Logistic Regression on imbalanced data.  
- **SMOTE**: Naive oversampling of minority class.  
- **CBO**: K-Means clustering on minority class, oversampling within clusters.  
- **CBU**: K-Means clustering on majority class, proportional undersampling from clusters.  
- **Performance Comparison**: Precision, Recall, and F1-score comparison across models with visualizations.  

---

## 📊 Results Overview
- **Baseline**: High accuracy, but many fraud cases missed.  
- **SMOTE**: High recall, but poor precision (many false positives).  
- **CBO**: Balanced performance with improved F1-score compared to SMOTE.  
- **CBU**: Very high recall but extremely low precision.  

The notebook includes detailed metrics, confusion matrices, and bar charts comparing the four approaches.  

---

## ✅ Conclusion
Clustering-based resampling (especially **CBO**) provides a more balanced trade-off between precision and recall compared to naive methods like SMOTE.  
Such approaches are useful in **fraud detection**, where catching more fraud (high recall) must be balanced against minimizing false alarms (precision).  
