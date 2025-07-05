# 🍷 Wine Classification Using Machine Learning

## 📌 Project Overview

This project aims to classify wines into one of three cultivars based on their chemical composition. It was developed as part of a data science/machine learning assignment using the classic Wine dataset from `sklearn.datasets.load_wine`.

The focus is on building an accurate and cost-effective classification system using fewer but highly informative features. We evaluate multiple models and recommend the most efficient approach for real-world implementation.

---

## 🎯 Objectives

- Identify key chemical properties that differentiate wine cultivars.
- Reduce the number of chemical tests required using feature selection techniques.
- Build and evaluate several machine learning classification models.
- Recommend the best-performing model for automation and cost-saving.

---

## 📂 Dataset

- **Source:** `sklearn.datasets.load_wine`
- **Samples:** 178
- **Features:** 13 chemical properties
- **Target:** 3 wine cultivars (Classes 0, 1, and 2)

---

## 🔍 Exploratory Data Analysis (EDA)

- Distribution patterns analyzed for each feature
- Detected right-skewed features like `proline`, `color_intensity`, and `malic_acid`
- Strong positive correlation found between `total_phenols` and `flavanoids` (r ≈ 0.86)
- No significant outliers were observed

---

## 🛠️ Feature Engineering & Selection

- **Recursive Feature Elimination (RFE)** used to identify top features:
  - `proline`, `flavanoids`, `color_intensity`, `od280/od315_of_diluted_wines`
- **Principal Component Analysis (PCA)** applied for dimensionality reduction
- Final model trained using only key features for cost-efficiency

---

## 🧪 Modeling & Evaluation

### Models Tested:
- K-Nearest Neighbors (KNN)
- Logistic Regression
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)

### Evaluation Strategy:
- 70/30 Train-Test Split
- 5-Fold Cross-Validation
- Out-of-Bag (OOB) scoring for Random Forest

### Model Accuracy Scores:

| Model               | Accuracy (%) |
|--------------------|--------------|
| KNN                | **98.1**     |
| Decision Tree      | 96.3         |
| Logistic Regression| 96.3         |
| SVM (RBF Kernel)   | 96.3         |
| Random Forest      | 92.6         |

---

## 📈 Results & Insights

- **KNN** performed the best, making it ideal for automation.
- Reducing features did not significantly impact accuracy.
- Key features like **Proline**, **Flavanoids**, and **Color Intensity** effectively separate wine classes.
- Wines can be classified with high accuracy using fewer lab tests — supporting cost-saving initiatives.

---

## ✅ Recommendations

- Adopt **KNN** for automated wine classification due to its high performance and simplicity.
- Limit lab testing to top chemical features for reduced operational costs.
- Integrate the model into the winery's quality control system for real-time classification.

---

## 🔚 Conclusion

Accurate wine classification is achievable using fewer chemical features. This project shows that with proper feature selection and a reliable model like KNN, wineries can automate cultivar identification efficiently and cost-effectively.
