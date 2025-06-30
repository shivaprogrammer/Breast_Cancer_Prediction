# Breast Cancer Prediction using Supervised Learning

## 👩‍⚕️ Project Overview

This project focuses on early and accurate **detection of breast cancer** using a supervised learning approach, specifically the **Random Forest Classifier**. Breast cancer remains one of the leading causes of mortality among women, and timely diagnosis is crucial for improving survival outcomes. This project demonstrates how machine learning techniques can help automate and improve diagnostic accuracy using real-world clinical data. The model not only achieves high accuracy but also handles imbalanced data, visualizes patterns in tumor characteristics, and evaluates feature importance for robust medical interpretation.

---

## 📌 Team Members

- **Akshat Gupta** (CSB20038)  
- **Shivani Tiwari** (CSB20044)  
- **Tanushree Das** (CSB20092)  

---

## 🎯 Objective

- Predict whether a tumor is **malignant (1)** or **benign (0)** using ML.
- Use data visualization, preprocessing, and model evaluation for optimal results.
- Implement and tune a **Random Forest Classifier** to achieve high precision and recall.
- Evaluate performance using metrics like **Accuracy, Precision, Recall, F1 Score**, and **Confusion Matrix**.

---

## 🧪 Dataset Description

- **Source:** UCI Breast Cancer Wisconsin Diagnostic Dataset  
- **Features:** Radius, Texture, Perimeter, Area, Smoothness, Compactness, Concavity, Concave Points, Symmetry, Fractal Dimension  
- **Target Variable:** `diagnosis` (0 = benign, 1 = malignant)  


---

## 🧰 Technologies Used

- Python (Colab)
- Libraries: `scikit-learn`, `pandas`, `matplotlib`, `seaborn`, `SMOTE`
- Model: `RandomForestClassifier` from `sklearn`

---

## ⚙️ Methodology

### 1. Data Collection & Cleaning
- Loaded `data.csv` and handled missing values
- Converted categorical labels (M, B) into numerical format using **Label Encoding**
- Split into `train:test = 80:20`

### 2. Data Visualization
- **Heatmaps** for correlation
- **Box plots** for outlier detection
- **Distribution plots** to study the variation of features for benign vs malignant tumors

### 3. Balancing the Dataset
- Handled class imbalance using **SMOTE** (Synthetic Minority Oversampling)

### 4. Feature Selection
- Performed feature importance ranking using Gini index from the Random Forest
- Selected **top 15 most informative features**

### 5. Model Training
- Trained **Random Forest** using `GridSearchCV` for best `n_estimators`
- Compared results on:
  - Original dataset
  - Balanced dataset
  - Reduced feature set

---

## 📊 Results

### 🔸 Initial Model (Raw Data)
- Accuracy: **98.25%**
- Class '0' (Benign): Precision 100%, Recall 97%
- Class '1' (Malignant): Precision 95%, Recall 100%

### 🔸 After Balancing (SMOTE)
- Accuracy: **98.60%**
- Both classes showed >97% precision and recall
- Only 2 misclassifications out of 143 samples

### 🔸 After Feature Selection
- Accuracy: **98.00%**
- Top features led to model interpretability and minimal drop in accuracy
- Gini importance helped reduce model complexity

---

## 📈 Evaluation Metrics

| Metric       | Description |
|--------------|-------------|
| **Accuracy** | Overall correct predictions |
| **Precision** | True positives / (true positives + false positives) |
| **Recall**   | True positives / (true positives + false negatives) |
| **F1 Score** | Harmonic mean of precision and recall |
| **Confusion Matrix** | TP, FP, FN, TN counts |

---

## 📂 Project Structure

```plaintext
Breast_Cancer_Prediction/
├── breast_cancer_prediction.py       # Full source code
├── Breast_Cancer_Prediction.pdf      # Extended report with methodology and results
├── _CSB20038_44_92_.pdf              # Mini project document
└── README.md                         # This file
