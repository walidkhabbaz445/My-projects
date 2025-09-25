# CE473 – Diabetes Detection & Diabetic Retinopathy Classification

This repository contains the full submission for **CE473 Project**, which is divided into two deliverables:

1. **PD1 – Diabetes Detection from a CSV File Using Machine Learning**
2. **PD2 – Diabetic Retinopathy Classification Using Fundus Images (Deep Learning)**

---

## 📌 Project Overview

### PD1 – Diabetes Detection (CSV Dataset)
- **Goal:** Predict whether a patient has diabetes using clinical and physiological data.  
- **Dataset:** Pima Indians Diabetes dataset (768 rows × 9 columns).  
- **Features:** Glucose, Insulin, BMI, Blood Pressure, Age, Skin Thickness, Pedigree Function.  
- **Pipeline:**
  - Exploratory Data Analysis (histograms, scatter plots, box plots, correlation heatmaps)
  - Preprocessing (scaling, imputation, outlier detection)
  - Model training with:
    - Logistic Regression
    - Random Forest Classifier
  - 5-fold cross-validation
- **Results:**
  - Logistic Regression: Accuracy ≈ 78%
  - Random Forest: Accuracy ≈ 82% (preferred model)
  - Top features: **Glucose, BMI, Insulin, Age**

---

### PD2 – Diabetic Retinopathy Classification (Fundus Images)
- **Goal:** Classify retinal images into **5 severity levels**:
  - 0 = No DR  
  - 1 = Mild  
  - 2 = Moderate  
  - 3 = Severe  
  - 4 = Proliferative DR  
- **Dataset:** Kaggle Fundus Images dataset (5 balanced folders for train/test).  
- **Pipeline:**
  - Image preprocessing & augmentation (flip, rotate, zoom, contrast)
  - Transfer learning with **MobileNetV2** backbone (pretrained on ImageNet)
  - Fine-tuning last layers for better generalization
  - Class weights applied to balance dataset
- **Results:**
  - Test Accuracy ≈ **61%**
  - Macro ROC AUC ≈ **0.90**
  - High recall for minority classes, but trade-offs in precision.

---

## ⚡ Challenges & Fixes
| Problem | Cause | Fix |
|---------|-------|-----|
| Outliers in tabular data (Insulin, Skin Thickness) | Extremely skewed distributions | Retained for generalization, noted in report |
| Class imbalance (both datasets) | Few samples in severe classes | Applied class weights, suggested SMOTE as future work |
| Shape mismatch loading EfficientNet | Some fundus images had 1 channel (grayscale) | Forced all images to 3-channel RGB |
| Weight loading errors | Keras expected (3,3,3) filters, got (3,3,1) | Switched backbone to MobileNetV2 |
| Large dataset size | Fundus images take GBs of space | Excluded datasets from repo, provided Kaggle links |

---

## 📊 Deliverables
- **Python Code**
  - `pd1_diabetes_ml.py` → Diabetes detection (PD1)
  - `train.py` → Retinopathy classification (PD2)
- **Report**
  - [CE473_Project_Report.pdf](./CE473_Project_Report.pdf) → merged PD1 & PD2 report
- **Outputs**
  - `outputs/metrics.json` → final metrics
  - `outputs/dr_model_final.keras` → saved trained model (optional)

---

## 🚀 How to Run

### PD1 – Diabetes Detection
```bash
python pd1_diabetes_ml.py
