 Lung Cancer Risk Prediction
A machine learning project that predicts lung cancer risk based on patient data including smoking habits, symptoms, and environmental exposure factors.

📋 Overview
This project applies multiple classification models to predict whether a patient is at risk of lung cancer. It covers the full ML pipeline: data preprocessing, feature engineering, feature selection, model training, hyperparameter tuning, and evaluation.

🗂️ Dataset
File: lung_cancer.csv
Key features used:

age, smoker, cigarettes_per_day, smoking_years, pack_years
air_pollution_index, occupational_exposure
shortness_of_breath, chronic_cough, chest_pain
Target: lung_cancer_risk


⚙️ Feature Engineering
New features created from existing ones:
FeatureDescriptionsmoking_intensitycigarettes_per_day × smoking_yearsrisk_exposureair_pollution_index × occupational_exposurehealth_riskage × smokersymptom_scoreSum of breath, cough & chest painlog_pack_yearsLog-transformed pack yearsage_squaredAge²heavy_smoker1 if cigarettes/day > 20high_risk_job1 if occupational exposure > 0

🔄 Pipeline

Preprocessing — Label Encoding for categorical columns
Feature Selection — SelectKBest (top 10 features, ANOVA F-test)
Scaling — MinMaxScaler
Training — Multiple models with GridSearchCV
Evaluation — Accuracy, Precision, Recall, F1-Score


🤖 Models
ModelTuningLogistic RegressionGridSearchCV (C, solver)Random ForestDefaultSupport Vector Machine (SVC)DefaultXGBoostGridSearchCV (n_estimators, max_depth, learning_rate)

📦 Requirements
pandas
numpy
scikit-learn
xgboost
matplotlib
seaborn
Install with:
bashpip install pandas numpy scikit-learn xgboost matplotlib seaborn

🚀 How to Run
bashjupyter notebook Lung Cancer Risk Prediction.ipynb
Or open directly on Google Colab.


