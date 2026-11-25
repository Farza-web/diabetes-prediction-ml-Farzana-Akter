# Diabetes Prediction System

## Project Overview

This project is a machine learning-based Diabetes Prediction System developed as part of an academic project. The main goal is to predict whether a survey record indicates diabetes or prediabetes based on different health and lifestyle-related features.

In this project, I explored the dataset, performed data preprocessing, trained multiple machine learning models, and compared their performance using different evaluation metrics.

**Note:** This project is developed for educational purposes only. It is not a medical diagnosis system.

## Dataset

I used the **CDC Diabetes Health Indicators Dataset**, which is based on the 2015 Behavioral Risk Factor Surveillance System (BRFSS) survey.

- Dataset source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/891)
- Total records: 253,680
- Input features: 21
- Target variable: `Diabetes_binary`

### Target Classes

- `0`: No diabetes indicator
- `1`: Diabetes or prediabetes indicator

The dataset includes health and lifestyle-related information such as BMI, Age, General Health, High Blood Pressure, Physical Activity, and other indicators.

## Data Preprocessing

The following preprocessing steps were performed:

1. Checked missing values and duplicate records.
2. Checked data types and feature values.
3. Separated input features and target variable.
4. Split the dataset into 80% training and 20% testing data using stratified sampling.
5. Used preprocessing pipelines for feature preparation and scaling where needed.
6. Handled class imbalance using class weights in the classification models.

## Machine Learning Models

Three machine learning algorithms were trained and compared:

- Logistic Regression
- Linear Support Vector Machine (SVM)
- Random Forest

## Model Comparison

The models were evaluated using Accuracy, Precision, Recall, F1-score, ROC-AUC, and PR-AUC.

| Model | Accuracy | Precision (Class 1) | Recall (Class 1) | F1-score (Class 1) | ROC-AUC | PR-AUC |
|---|---:|---:|---:|---:|---:|---:|
| Logistic Regression | 0.7316 | 0.3108 | 0.7612 | **0.4414** | **0.8196** | 0.3926 |
| Linear SVM | 0.7275 | 0.3083 | **0.7686** | 0.4400 | 0.8194 | 0.3936 |
| Random Forest | **0.8361** | **0.4120** | 0.4127 | 0.4127 | 0.8123 | **0.3998** |

### Selected Model

Logistic Regression was selected for the educational prediction demonstration because it achieved the highest positive-class F1-score (0.4414).

Although Random Forest achieved higher accuracy, Logistic Regression identified a larger proportion of positive cases.

## Exploratory Data Analysis Findings

Some important observations from the dataset:

1. The dataset contains approximately 86.07% negative-class records and 13.93% positive-class records.
2. The diabetes indicator rate generally increases across age categories.
3. The diabetes indicator rate increases with poorer general health.
4. Respondents with high blood pressure have a higher observed diabetes indicator rate than those without high blood pressure.

## How to Run the Project

### Requirements

- Python 3.x
- Jupyter Notebook or Kaggle Notebook

### Steps

1. Download the dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/891).
2. Open the project notebook in Jupyter Notebook or Kaggle.
3. Add the dataset to your Kaggle notebook if you are using Kaggle.
4. Update the dataset file path if necessary.
5. Run the notebook cells in order.
6. Review the model comparison and try the prediction demonstration.

## Limitations

- The dataset is based on self-reported survey responses from 2015.
- The dataset may contain reporting errors.
- The model has not been clinically validated.
- Class imbalance affects model performance.

## Responsible Use Disclaimer

This project is developed strictly for educational and academic purposes. The predictions and estimated probabilities are based on historical survey data and must not be used for medical diagnosis, treatment decisions, or personal healthcare decisions.

## Author

**Name:** Farzana Akter  
**Project:** Diabetes Prediction System  
**Repository:** diabetes-prediction-ml-farzana-akter
