🌧️ Rainfall Prediction Classifier
📌 Project Overview

This project builds a machine learning classifier to predict whether it will rain tomorrow in Melbourne, Australia.
Using historical weather data, the model applies feature engineering, preprocessing pipelines, and hyperparameter optimization to train robust classifiers.

Two models are implemented and compared:

✅ Random Forest Classifier

✅ Logistic Regression

The project is part of the IBM Machine Learning Capstone.

🎯 Objectives

Explore and preprocess a real-world weather dataset

Handle missing values and prevent data leakage

Engineer features (e.g., mapping dates to seasons)

Build pipelines with preprocessing + classifier

Optimize models with GridSearchCV and stratified cross-validation

Evaluate performance using:

Accuracy

Precision, Recall, F1-score

Confusion Matrix

Feature Importances

📂 Dataset

The dataset contains historical daily weather observations for Melbourne.
Key features include:

Temperature (MaxTemp, MinTemp, Temp3pm, etc.)

Humidity (Humidity9am, Humidity3pm)

Wind (WindGustDir, WindSpeed9am, WindSpeed3pm)

Sunshine, Evaporation, Rainfall

Pressure at 9am and 3pm

Target variable: RainTomorrow (Yes/No → encoded as 1/0)

⚙️ Project Steps
1️⃣ Data Preprocessing

Removed missing values

Considered data leakage (excluded features unavailable at prediction time)

Converted date into seasons and dropped original date column

2️⃣ Feature Engineering

Separated numerical and categorical features

Applied:

Scaling for numeric features

One-Hot Encoding for categorical features

3️⃣ Pipeline & Model Training

Built a scikit-learn pipeline combining preprocessing and classifier

Trained Random Forest Classifier with GridSearchCV

Compared performance with Logistic Regression

4️⃣ Model Evaluation

Random Forest Classifier:

Higher accuracy (~85%)

Better True Positive Rate (captured more rainy days)

Logistic Regression:

Simpler, but lower accuracy and TPR

5️⃣ Feature Importances

Humidity3pm was the strongest predictor of rain tomorrow.

Other useful predictors: Pressure3pm, Temp3pm, Sunshine.

Inefficient predictors: Evaporation, WindGustDir, MaxTemp, Humidity9am.

📊 Results

Class Distribution: Imbalanced (≈ 75% No Rain, 25% Rain).

Best Model: Random Forest Classifier.

Key Findings:

If we always predicted "No Rain," accuracy ≈ 75% (misleading due to imbalance).

Random Forest improved recall significantly, making it more useful for weather forecasting.

🚀 Future Improvements

Try additional models (e.g., Gradient Boosting, XGBoost, SVM).

Use SMOTE or other resampling techniques for class imbalance.

Experiment with feature selection and dimensionality reduction.

Engineer new features (e.g., moving averages of weather variables).

🛠️ Tech Stack

Python 3.9+

Pandas, NumPy for data wrangling

Matplotlib, Seaborn for visualization

Scikit-learn for ML pipeline, preprocessing, and modeling

📑 Author

Abhishek Kumar

Developed as part of the IBM Machine Learning Capstone Project
