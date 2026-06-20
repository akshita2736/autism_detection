# 🧠 Autism Detection Using Machine Learning

A machine learning project that predicts Autism Spectrum Disorder (ASD) based on screening questionnaire responses and demographic information. The project focuses on data preprocessing, class imbalance handling using SMOTE, model training, and performance evaluation.

---

## 📌 Project Overview

Early identification of Autism Spectrum Disorder (ASD) can help improve access to support and intervention. This project uses machine learning techniques to classify whether an individual is likely to have ASD based on responses to a screening questionnaire and related attributes.

The workflow includes:

- Data Cleaning & Preprocessing
- Handling Missing Values
- Label Encoding of Categorical Features
- Exploratory Data Analysis (EDA)
- Correlation Analysis
- Class Imbalance Handling using SMOTE
- Model Training and Evaluation

---

## 📊 Dataset

**Dataset:** Autism Screening Adult Dataset

The dataset contains:

- Screening questionnaire responses (A1–A10)
- Age
- Gender
- Ethnicity
- Jaundice history
- Family history of autism
- Country of residence
- Previous app usage
- Relationship information

**Target Variable:**
- `Class/ASD`
  - 0 → No ASD
  - 1 → ASD

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)
- XGBoost

---

## ⚙️ Data Preprocessing

### 1. Data Cleaning
- Removed irrelevant columns
- Handled missing values
- Converted data types where required

### 2. Label Encoding
Categorical features were transformed into numerical representations using LabelEncoder.

### 3. Exploratory Data Analysis
- Distribution analysis
- Correlation heatmap
- Target variable analysis

### 4. Class Imbalance Handling
The dataset was imbalanced, so **SMOTE (Synthetic Minority Oversampling Technique)** was applied to the training set.

Before SMOTE:

| Class | Count |
|---------|---------|
| 0 | 412 |
| 1 | 151 |

After SMOTE:

| Class | Count |
|---------|---------|
| 0 | 412 |
| 1 | 412 |

---

## 🤖 Models Implemented

### Decision Tree Classifier
A tree-based classification model used as a baseline.

### Random Forest Classifier
An ensemble learning method that combines multiple decision trees for improved performance and robustness.

### XGBoost Classifier
A gradient boosting algorithm known for high predictive performance.

---

## 📈 Model Evaluation

Performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- 5-Fold Cross Validation

### Random Forest Cross Validation Results

```text
Fold Scores:
[0.9645, 0.9645, 0.9504, 0.9858, 0.9357]

Mean Accuracy: 96.02%
Standard Deviation: 1.67%

While the held-out test split achieved perfect accuracy, the cross-validation score (~96%) provides a more realistic estimate of model generalization.
```

---

## 🔍 Key Insights

- Screening questionnaire responses are highly predictive of ASD classification.
- SMOTE effectively addressed class imbalance.
- Random Forest and XGBoost demonstrated strong predictive performance.
- 5-Fold Cross Validation achieved an average accuracy of approximately 96%.

---

## 📚 Future Improvements

- Hyperparameter tuning using GridSearchCV
- Feature selection techniques
- Explainable AI using SHAP
- Deployment using Streamlit or Flask

