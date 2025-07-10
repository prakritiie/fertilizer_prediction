
# 🌾 Fertilizer Prediction using XGBoost | Kaggle Playground S5E6

[![Kaggle](https://img.shields.io/badge/Kaggle-Playground%20Series%20S5E6-blue?logo=kaggle)](https://www.kaggle.com/competitions/playground-series-s5e6/overview)

This repository contains my solution for the Kaggle competition **Playground Series - Season 5, Episode 6**. The task was to predict the **recommended fertilizer type** based on soil, crop, and environmental data using supervised machine learning techniques.

---

## 📘 Competition Overview

- **Objective**: Classify which type of fertilizer (among 10 classes) is recommended given certain features like soil moisture, crop type, humidity, etc.
- **Metric**: `Mean Average Precision @ 3 (MAP@3)`

📎 [Competition Link](https://www.kaggle.com/competitions/playground-series-s5e6/overview)

---

## 🔍 Dataset Description

The dataset includes features like:

- `Temperature`
- `Humidity`
- `Moisture`
- `Soil Type` (Categorical)
- `Crop Type` (Categorical)
- `Nitrogen`, `Phosphorous`, `Potassium` values

The target variable is:

- `Fertilizer Name` (10-class categorical label)

---

## 📂 Repository Structure

```bash
.
├── predict-fertilizer.ipynb     # Main notebook with EDA, modeling, and submission
├── submission_xgb_cv.csv        # Final submission file from XGBoost model with CV
├── README.md                    # You're here!
```

---

## ⚙️ Approach

1. **EDA & Preprocessing**:
    - Checked for nulls, value distributions
    - Label encoding of `Soil Type`, `Crop Type`, and target
2. **Feature Engineering**:
    - Basic feature scaling
    - Correlation checks
3. **Modeling**:
    - Used **XGBoostClassifier** with cross-validation
    - Stratified K-Fold (5 folds)
4. **Evaluation**:
    - Used average of fold predictions for submission

---

## 📊 Results

| Score Type | Value   |
|------------|---------|
| Public     | 0.31549 |
| Private    | 0.31498 |

✅ **Consistent performance across public and private test sets.**

---

## 🛠 Libraries Used

- `Pandas`, `NumPy`
- `Scikit-learn`
- `XGBoost`
- `Matplotlib`, `Seaborn`

---

## 🚀 How to Run

Clone the repo and run the notebook:

```bash
git clone https://github.com/yourusername/fertilizer-prediction-xgb.git
cd fertilizer-prediction-xgb
```

Open and run `predict-fertilizer.ipynb` in Jupyter Notebook or any Python IDE with the required packages installed.

---

## 📌 Future Improvements

- Try other models like LightGBM, CatBoost, or ensemble strategies
- Feature importance and SHAP analysis

---



