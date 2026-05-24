# 🏠 AI/ML Internship — Week 5: Supervised Learning (Classification)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-orange?logo=scikit-learn)
![Week](https://img.shields.io/badge/Week-5%20of%208-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

**Name:** Usman Asif  
**Date:** 24th May, 2026  
**Program:** AI/ML Internship — Digitech Offerings  
**Instructor:** Zain Ul Abideen  

---

## 📌 Project Overview

This project focuses on **Titanic Survival Prediction using Classification Algorithms**. Four machine learning models are trained, tuned, and compared to predict whether a passenger survived based on demographic and travel-related features.

The workflow includes full ML pipeline implementation: data preprocessing, feature engineering, model training, hyperparameter tuning using GridSearchCV, cross-validation, evaluation metrics, and final model deployment using `joblib`.

---

## 📊 Dataset

| Property | Detail |
|---|---|
| **Dataset** | Titanic - Machine Learning from Disaster |
| **Samples** | 1,460 |
| **Target Variable** | Survived (0 = No, 1 = Yes) |
| **Key Features** | Pclass, Sex, Age, Fare, SibSp, Parch, Embarked |
| **Engineered Features** | FamilySize, IsAlone, log(Fare) |
| **Source** | Kaggle |

---

## 🤖 Models Trained

| # | Model | Description |
|---|---|---|
| 1 | Logistic Regression | Linear baseline classifier |
| 2 | K-Nearest Neighbors (KNN) | Distance-based classification |
| 3 | Decision Tree | Rule-based interpretable model |
| 4 | Random Forest | Ensemble model (best performer) |

---

## 🏆 Best Model Results

> **Best Model: Random Forest Classifier**

| Metric | Value |
|---|---|
| **Test Accuracy** | *see notebook output* |
| **Test F1 Score** | *see notebook output* |
| **ROC-AUC Score** | *see notebook output* |

**Key Insight:**  
Random Forest performed best due to its ability to capture nonlinear relationships, handle feature interactions, and reduce overfitting through ensemble learning. It consistently outperformed individual models across all evaluation metrics.

---

## 📁 Repository Structure
```text
AIML-Internship-Week5-UsmanAsif/
│
├── Week5_Final_Notebook.ipynb
├── week5_dashboard.png
├── week5_best_model.pkl
├── decision_tree_analysis.png
└── README.md
---

## 📋 Notebook Contents (18 Steps)

### Part A — Data Preparation & Baseline Model
- Step 1 — Libraries import, dataset loading, class balance check  
- Step 2 — Missing value handling, feature engineering, encoding  
- Step 3 — Train-test split with stratification + StandardScaler  
- Step 4 — Evaluation utility functions (metrics + plotting)  
- Step 5 — Logistic Regression baseline + threshold analysis  

### Part B — Model Training & Comparison
- Step 6 — KNN optimization (k selection + distance metrics)  
- Step 7 — Decision Tree depth tuning + visualization  
- Step 8 — Feature importance comparison  
- Step 9 — Random Forest n_estimators analysis  
- Step 10 — GridSearchCV tuning for Random Forest  
- Step 11 — Final model comparison table (4 models)  

### Part C — Evaluation & Validation
- Step 12 — Confusion matrix + error analysis  
- Step 13 — ROC & Precision-Recall curves  
- Step 14 — Stratified 5-fold cross-validation  
- Step 15 — Learning curves (bias vs variance analysis)  

### Part D — Dashboard, Predictions & Report
- Step 16 — 6-chart evaluation dashboard (`week5_dashboard.png`)  
- Step 17 — Predictions dataframe + joblib model saving  
- Step 18 — Full written analysis report (7 sections)  

---

## 📈 Dashboard Preview

<img width="2400" height="2700" alt="week5_dashboard" src="https://github.com/user-attachments/assets/b23aaab9-c344-4c7f-9cc5-f71dc811e9d2" />



---

## 🛠 Tools & Libraries

- scikit-learn — models, metrics, GridSearchCV, Pipeline  
- pandas — data manipulation  
- numpy — numerical operations  
- matplotlib — visualization  
- seaborn — plots and heatmaps  
- scipy — statistical analysis  
- joblib — model saving  

---

## ▶️ How to Run

1. Open Google Colab or Jupyter Notebook  
2. Upload `Week5_UsmanAsif.ipynb`  
3. Run all cells  
4. Ensure dataset is available (train.csv or Kaggle load)  
5. Outputs will generate automatically  

---

## 📚 Key Learnings

- Feature engineering improves classification accuracy  
- Stratification prevents class imbalance issues  
- Ensemble models outperform single estimators  
- ROC-AUC and F1-score are critical evaluation metrics  
- Hyperparameter tuning significantly improves performance  
- Visualization helps interpret model behavior  

---

## 👤 Author

**Usman Asif**  
AI/ML Internship Cohort — Digitech Offerings  
Instructor: Zain Ul Abideen  

---

⭐ Week 5 of 8 — Supervised Learning (Classification)
