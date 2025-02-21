# ❤️ Heart Failure Prediction using Machine Learning

## 📌 Project Overview
This project focuses on predicting the risk of heart failure using machine learning models. It employs Random Forest and XGBoost classifiers, along with extensive data preprocessing, exploratory data analysis (EDA), and feature engineering to improve predictive accuracy. The best model is saved for future deployment.

---

## 🛠️ Technologies Used
- **Programming & Libraries**: Python, NumPy, Pandas, Matplotlib, Seaborn, Plotly
- **Machine Learning Models**: Random Forest, XGBoost
- **Data Preprocessing**: MinMaxScaler, Label Encoding, Handling Missing Data, Outlier Detection
- **Evaluation Metrics**: Confusion Matrix, Classification Report, Cross-Validation
- **Model Deployment**: Joblib for model serialization

---

## 📊 Dataset Overview
The dataset consists of 918 samples with 12 features related to heart health, including:
- **Age, Sex, Chest Pain Type**
- **Resting Blood Pressure, Cholesterol Levels**
- **Fasting Blood Sugar, Resting ECG Results**
- **Max Heart Rate, Exercise-Induced Angina**
- **ST Depression (Oldpeak), ST Slope**
- **Target Variable: Heart Disease (0 = No, 1 = Yes)**

---

## 🔍 Exploratory Data Analysis (EDA)
EDA was performed to understand data distribution and relationships. Key insights include:
- Most patients fall within the **50-60 age group**.
- **Asymptomatic chest pain** is the most common type.
- **Higher cholesterol and blood pressure levels** correlate with heart disease.
- **Oldpeak (ST Depression)** is a strong indicator of heart disease.

---

## 🏗️ Data Preprocessing
1. **Handling Missing Values**: Imputed missing values using median strategy.
2. **Outlier Detection & Removal**: Applied IQR method to remove extreme values.
3. **Feature Encoding**: Converted categorical features into numerical using Label Encoding.
4. **Feature Scaling**: Used MinMaxScaler to normalize numerical features.

---

## 🤖 Model Training & Evaluation
The dataset was split into **75% training and 25% testing** for model evaluation.

### **Random Forest Classifier**
- **Training Accuracy**: 100%
- **Testing Accuracy**: 89.80%
- **Cross-Validation Score**: 86.62%

### **XGBoost Classifier**
- **Training Accuracy**: 94.01%
- **Testing Accuracy**: 89.80%
- **Cross-Validation Score**: 86.74%

Both models performed well, with **Random Forest slightly outperforming XGBoost** in accuracy.

---

## 🎯 Key Findings
- **High cholesterol & blood pressure significantly contribute to heart disease.**
- **Exercise-induced angina & ST depression are strong predictors of heart risk.**
- **Random Forest performed best in predictive accuracy.**

---

## 🚀 Deployment
The trained **Random Forest model** is saved using Joblib for future deployment:
```python
import joblib
joblib.dump(model, 'RandomForestClassifier_model.sav')
