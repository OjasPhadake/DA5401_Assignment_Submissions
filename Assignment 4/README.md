# DA5401 - Assignment 4  

**Name:** Ojas Phadake  
**Roll No:** CH22B007  

---

## 📂 Repository Contents
This repository contains the solutions for **Assignment 4** of the course **DA5401**.  
The assignment focuses on addressing **class imbalance** in fraud detection using a **Gaussian Mixture Model (GMM)** for synthetic minority data generation and evaluating its impact on classifier performance.  

- **DA5401_CH22B007_Assignment4.ipynb** → Jupyter Notebook containing the complete code, visualizations, and explanations.  
- **DA5401_CH22B007_Assignment4 PDF.pdf** → PDF export of the notebook for easy readability and submission.  

---

## 📝 Problem Statement
You are working with a highly imbalanced **credit card fraud detection dataset**, where fraudulent transactions represent only a tiny fraction of all transactions.  
Traditional classifiers tend to focus on the majority class, leading to poor detection of fraudulent cases.  

The goal of this assignment is to:  
1. Implement a **Gaussian Mixture Model (GMM)** to generate synthetic samples for the minority (fraudulent) class.  
2. Create a training set that allows a classifier to learn the nuances of the minority class effectively without overfitting.  
3. Compare GMM-based synthetic data augmentation with a **baseline (imbalanced) model**.  
4. Train and evaluate a **Logistic Regression classifier** on each dataset.  
5. Analyze performance using **Precision, Recall, and F1-score** for the **fraudulent transactions**.  

---

## 🚀 Key Steps
- **Data Preprocessing**: Splitting into train/test sets and handling class imbalance.  
- **Baseline Model**: Logistic Regression trained on the original imbalanced dataset.  
- **GMM-based Oversampling**: Fit a Gaussian Mixture Model on the minority class and generate synthetic samples to augment the training set.  
- **Performance Evaluation**: Compare baseline and GMM-augmented models using **Precision, Recall, and F1-score**.  
- **Visualization**: Confusion matrices and bar charts to illustrate the impact of synthetic data on model performance.  

---

## 📊 Results Overview
- **Baseline Model**: High accuracy on the majority class, poor detection of fraudulent transactions.  
- **GMM-Augmented Model**: Improved recall and F1-score for the minority class, demonstrating the effectiveness of model-based synthetic oversampling.  

The notebook includes detailed metrics, confusion matrices, and visualizations comparing the baseline and GMM-augmented approaches.  

---

## ✅ Conclusion
Using **Gaussian Mixture Models (GMM)** to generate synthetic samples provides a more balanced training set, improving the classifier's ability to detect fraudulent transactions without overfitting.  
This model-based oversampling approach is effective for **fraud detection tasks** where the minority class is critical but underrepresented.  
