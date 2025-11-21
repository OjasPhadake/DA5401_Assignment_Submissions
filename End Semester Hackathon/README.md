# **End Semester Hackathon Report**

**Name:** Ojas Phadake  
**Roll No:** CH22B007  

---

## **Overview**

This repository contains the complete workflow, experiments, and final solution developed for the **End Semester Hackathon** of the course **DA5401**.  
The challenge involved predicting a continuous score using a dataset of text responses paired with structured embeddings.

---

## **Tasks Completed**

### **1. Data Engineering & Preprocessing**
- Cleaned text responses and handled missing values.
- Standardized embeds, fixed shape mismatches, and prepared metric-learning compatible inputs.
- Implemented **balanced sampling** with augmentation for low-frequency score classes.

### **2. Exploratory Data Analysis (EDA)**
- Generated score distribution plots, length distributions, and embedding-wise variance analysis.
- Performed class imbalance visualization and PCA variance inspection.

### **3. Feature Engineering**
- Designed an advanced **metric-learning feature set** (cosine similarity, distances, Hadamard interactions, abs-diff).
- Introduced **Polynomial Feature Expansion** (degree=2).
- Applied **PCA dimensionality reduction** with optimized variance retention experiments.

### **4. Model Development & Selection**
- Evaluated multiple regressors (Linear Models, Gradient Boosting, Random Forest, LightGBM).
- Found **LightGBM + PCA(Poly Features)** to be the best-performing pipeline.
- Tuned hyperparameters for maximum generalization.

### **5. Hacks & Performance Optimizations**
- Designed custom augmentation logic for low-score samples.
- Used PCA variance sweep and high-speed SVD computation for dimensionality optimization.
- Implemented clipping and rounding strategies for stable predictions.

### **6. Final Model Performance**
- Achieved significant error reduction through:
  - PCA optimization  
  - Feature expansion  
  - LightGBM tuning  
- Final RMSE improved substantially from the baseline using the optimized pipeline.

---

## **Conclusion**
The hackathon project demonstrated a complete ML pipeline—from data preparation and visualization to advanced feature engineering and model optimization. Through metric-learning features, PCA-based compression, and a tuned LightGBM model, the final solution achieved strong predictive performance and high generalization. The workflow highlights practical machine learning problem-solving under real constraints.

---
