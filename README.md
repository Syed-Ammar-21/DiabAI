# 🧠 DiabAI : Smart Diabetes Detection Using Deep Learning
A machine learning–based web application that predicts diabetes risk using basic health information.
Built with Python and Streamlit, the app also explains predictions using SHAP and permutation importance.

> This project is for educational purposes only and is not a medical diagnostic tool.

---

## 📌 Overview
This application allows users to enter health data and receive:
- Diabetes risk prediction
- Probability score
- Explanation of feature contributions

The model prioritizes Recall to reduce missed positive cases, which is important in healthcare-related problems.

---

## 📊 Dataset

- Source: National Institute of Diabetes and Digestive and Kidney Diseases
- Samples: 768
- Features: 9

---

### Features Used for Prediction
- Pregnancies
- Glucose
- BMI
- Insulin
- Age

Invalid zero values were treated as missing and handled during preprocessing.

---

## ⚙️ Model

- Algorithm: Random Forest Classifier

### Why Random Forest?
- Performs well on structured datasets
- Handles non-linear relationships
- Provides feature importance

### Training Approach
- Cross-validation instead of simple train/test split
- Model selection based on ROC AUC
- Threshold adjusted to improve Recall
- Hyperparameters optimized using Optuna

---

## 🧩 Feature Engineering

### Feature Engineering
- Creation of derived features:
  - RiskScore
  - PregnancyRatio
  - BMI-Age interaction

### WoE Encoding (Weight of Evidence)
- Converts selected features into informative categories
- Improves model interpretability

### Column Selection
- Keeps relevant engineered features
- Removes unnecessary columns

---

## ✨ Application Features

- Interactive health data input
- Real-time diabetes risk prediction
- Prediction probability display
- SHAP explanation plots:
  - Waterfall Plot
  - Force Plot
- Permutation importance analysis
- Performance metrics visualization

---

## 🚀 Installation

### Requirements
- Python 3.10+
- pip

### Setup
```bash
git clone https://github.com/Syed-Ammar-21/DiabAI.git
cd DiabAI
pip install -r requirements.txt
streamlit run main.py

