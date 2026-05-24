# 🏠 AI/ML Internship — Week 5: Supervised Learning (Classification)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-orange?logo=scikit-learn)
![Week](https://img.shields.io/badge/Week-5%20of%208-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 👤 Student Information

- **Name:** Usman Asif  
- **Date:** 24th May, 2026  
- **Program:** AI/ML Internship — Digitech Offerings  
- **Instructor:** Zain Ul Abideen  

---

# 📌 Project Overview

This project focuses on predicting Titanic passenger survival using multiple machine learning classification algorithms. The complete machine learning pipeline was implemented, including data preprocessing, feature engineering, model training, hyperparameter tuning, cross-validation, evaluation, visualization, and model deployment.

Four classification algorithms were trained and compared to determine the best-performing model for predicting passenger survival based on demographic and travel-related information.

The project demonstrates practical implementation of supervised machine learning classification techniques using Python and Scikit-learn.

---

# 📊 Dataset Information

| Property | Detail |
|---|---|
| **Dataset** | Titanic — Machine Learning from Disaster |
| **Source** | Kaggle |
| **Samples** | 891 |
| **Target Variable** | Survived |
| **Problem Type** | Binary Classification |
| **Key Features** | Pclass, Sex, Age, Fare, SibSp, Parch, Embarked |

---

# ⚙️ Feature Engineering

The following preprocessing and feature engineering steps were performed:

- Filled missing values in Age using median
- Filled missing Embarked values using mode
- Dropped irrelevant columns:
  - PassengerId
  - Name
  - Ticket
  - Cabin
- Encoded Gender:
  - male = 1
  - female = 0
- Applied One-Hot Encoding on Embarked
- Created new feature:
  - `FamilySize = SibSp + Parch + 1`
- Created binary feature:
  - `IsAlone`
- Applied logarithmic transformation on Fare:
  - `np.log1p(Fare)`
- Applied StandardScaler for feature normalization

---

# 🤖 Models Trained

| # | Model | Description |
|---|---|---|
| 1 | Logistic Regression | Linear baseline classifier |
| 2 | K-Nearest Neighbors (KNN) | Distance-based classification |
| 3 | Decision Tree Classifier | Rule-based interpretable classifier |
| 4 | Random Forest Classifier | Ensemble learning model |

---

# 🏆 Best Model Performance

## ✅ Best Model: Random Forest Classifier

| Metric | Value |
|---|---|
| **Test Accuracy** | 84.91% |
| **Precision** | 0.83 |
| **Recall** | 0.81 |
| **F1 Score** | 0.82 |
| **ROC-AUC Score** | 0.89 |

### 📌 Key Insight

Random Forest achieved the best overall performance because it effectively captured nonlinear relationships, reduced overfitting through ensemble averaging, and handled feature interactions better than individual models.

It consistently outperformed Logistic Regression, KNN, and Decision Tree across F1-score and ROC-AUC metrics.

---

# 📁 Repository Structure

```text
AIML-Internship-Week5-UsmanAsif/
│
├── Week5_UsmanAsif.ipynb
├── week5_dashboard.png
├── week5_best_model.pkl
├── decision_tree_analysis.png
└── README.md
```

---

# 📋 Notebook Contents (18 Steps)

## 🔹 Part A — Data Preparation & Baseline Model

### Step 1 — Environment Setup & Dataset Loading
- Imported required libraries
- Loaded Titanic dataset
- Checked dataset shape and statistics
- Analyzed class imbalance

### Step 2 — Feature Engineering & Preprocessing
- Handled missing values
- Encoded categorical variables
- Engineered FamilySize and IsAlone features
- Applied log transformation

### Step 3 — Train-Test Split & Scaling
- Performed stratified splitting
- Applied StandardScaler
- Verified scaling statistics

### Step 4 — Evaluation Utility Functions
- Created reusable evaluation functions
- Calculated regression-style metrics
- Created actual vs predicted plots

### Step 5 — Logistic Regression Baseline
- Trained Logistic Regression model
- Performed threshold analysis
- Evaluated confusion matrix
- Analyzed feature coefficients

---

## 🔹 Part B — Model Training & Comparison

### Step 6 — K-Nearest Neighbors (KNN)
- Tested k values from 1 to 30
- Compared distance metrics
- Optimized k using GridSearchCV

### Step 7 — Decision Tree Analysis
- Compared different tree depths
- Tuned max_depth using GridSearchCV
- Visualized decision tree
- Printed decision rules

### Step 8 — Decision Tree Feature Importance
- Plotted top feature importances
- Compared with Logistic Regression coefficients
- Analyzed overfitting behavior

### Step 9 — Random Forest Analysis
- Compared n_estimators values
- Evaluated training time
- Analyzed performance improvements

### Step 10 — Random Forest Hyperparameter Tuning
- Tuned:
  - n_estimators
  - max_depth
  - max_features
  - min_samples_split
- Selected best Random Forest model

### Step 11 — Final Model Comparison
- Compared all four classifiers
- Created ROC curve comparison
- Built grouped metric charts

---

## 🔹 Part C — Evaluation & Validation

### Step 12 — Confusion Matrix Deep Dive
- Residual analysis
- Histogram analysis
- Q-Q plots
- Shapiro-Wilk normality test

### Step 13 — ROC & Precision-Recall Curves
- Compared ROC curves
- Compared Precision-Recall curves
- Analyzed class imbalance impact

### Step 14 — Stratified Cross-Validation
- Applied 5-Fold Stratified CV
- Used Pipeline to prevent leakage
- Compared fold stability

### Step 15 — Learning Curves
- Diagnosed bias vs variance
- Compared train and validation scores
- Analyzed generalization behavior

---

## 🔹 Part D — Dashboard, Predictions & Report

### Step 16 — Complete Evaluation Dashboard
Created a 6-chart dashboard including:
- ROC Curves
- Precision-Recall Curves
- Confusion Matrix
- Feature Importances
- Cross-validation Boxplots
- Learning Curves

Saved as:
```python
week5_dashboard.png
```

### Step 17 — Predictions & Model Saving
- Generated predictions dataframe
- Saved best model using joblib
- Reloaded and verified saved model

Saved model:
```python
week5_best_model.pkl
```

### Step 18 — Written Analysis Report
Prepared complete professional report including:
1. Executive Summary
2. Feature Engineering Impact
3. Model-by-Model Analysis
4. Regularization Insights
5. Residual Analysis Findings
6. Best Model Recommendation
7. Reflection

---

# 📈 Dashboard Preview

<img width="2400" height="2700" alt="week5_dashboard" src="https://github.com/user-attachments/assets/b23aaab9-c344-4c7f-9cc5-f71dc811e9d2" />

---

# 🛠 Tools & Libraries Used

## Programming Language
- Python 3.x

## Libraries
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn
- joblib

## Scikit-learn Components
- LogisticRegression
- KNeighborsClassifier
- DecisionTreeClassifier
- RandomForestClassifier
- Pipeline
- GridSearchCV
- StandardScaler
- StratifiedKFold
- learning_curve

---

# 📊 Evaluation Metrics Used

The following metrics were used to evaluate classification performance:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix
- Cross-Validation Scores

Additional regression-style metrics:
- MAE
- MSE
- RMSE
- R² Score
- Adjusted R²
- MAPE

---

# ▶️ How to Run the Project

## Step 1
Clone the repository:

```bash
git clone https://github.com/your-username/AIML-Internship-Week5-UsmanAsif.git
```

## Step 2
Open Jupyter Notebook or Google Colab

## Step 3
Run:

```python
Week5_UsmanAsif.ipynb
```

## Step 4
Ensure Titanic dataset (`train.csv`) is available in the project directory.

## Step 5
Run all notebook cells sequentially.

---

# 📚 Key Learnings

- Feature engineering significantly improves model performance
- Stratified splitting preserves class distribution
- Ensemble methods outperform individual estimators
- Hyperparameter tuning improves generalization
- ROC-AUC and F1-score are critical for classification evaluation
- Cross-validation improves reliability of model evaluation
- Visualization helps interpret model behavior effectively

---

# 🔍 Major Insights

- Gender was the strongest predictor of survival
- First-class passengers had higher survival rates
- Traveling with small families improved survival probability
- Random Forest handled nonlinear relationships best
- KNN performance was highly dependent on feature scaling

---

# 🚀 Future Improvements

Possible future enhancements include:

- XGBoost and LightGBM implementation
- Advanced feature engineering
- Probability calibration
- SMOTE for imbalance handling
- Model deployment using Flask or FastAPI
- Streamlit dashboard application

---

# 👤 Author

## Usman Asif

AI/ML Internship Cohort — Digitech Offerings

### Instructor
Zain Ul Abideen

---

# ⭐ Final Conclusion

This project demonstrates a complete end-to-end machine learning classification workflow including:

- Data Cleaning
- Feature Engineering
- Model Training
- Hyperparameter Tuning
- Cross-Validation
- Model Evaluation
- Visualization
- Model Saving & Deployment

The Random Forest Classifier achieved the best performance and is recommended for deployment due to its robustness, stability, and strong predictive performance.

---

⭐ Week 5 of 8 — Supervised Learning (Classification)
