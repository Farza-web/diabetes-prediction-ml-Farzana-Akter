# Diabetes Prediction System
**Project Summary**

### 1. Problem Statement

Diabetes is an important health concern, and identifying patterns related to diabetes can help us better understand the factors associated with it. The main objective of this project is to develop a machine learning system that can classify whether a survey record indicates diabetes or prediabetes based on different health and lifestyle-related features. This project is developed for educational purposes and does not provide medical diagnoses.

### 2. Dataset Description

For this project, I used the CDC Diabetes Health Indicators dataset, which is based on the 2015 Behavioral Risk Factor Surveillance System (BRFSS) survey. The dataset contains 253,680 records, 21 input features, and one target variable named `Diabetes_binary`. The target has two classes: 0 represents no diabetes indicator, while 1 represents diabetes or prediabetes. The dataset includes information such as BMI, age, general health, high blood pressure, physical activity, and other health-related indicators.

### 3. Data Preprocessing

First, I checked the dataset for missing values, duplicate records, data types, and possible invalid values. No missing values were found. I kept the original records rather than removing duplicate rows without proper justification. Then, I separated the input features from the target variable and divided the data into 80% training and 20% testing sets using stratified sampling. A preprocessing pipeline was used to prepare the features and apply scaling where needed.

### 4. Model Training and Best Model

I trained and compared three machine learning algorithms: Logistic Regression, Linear SVM, and Random Forest. Among these models, Logistic Regression achieved the highest positive-class F1-score and was selected for the prediction demonstration.

Its test performance was:

- Accuracy: **73.16%**
- Precision: **31.08%**
- Recall: **76.12%**
- F1-score: **44.14%**
- ROC-AUC: **0.8196**
- PR-AUC: **0.3926**

Although Random Forest achieved higher accuracy (83.61%), its positive-class recall was lower (41.27%). Therefore, I considered positive-class F1-score and recall instead of selecting a model based only on accuracy.

### 5. Major Findings from EDA

The exploratory data analysis showed three important observations:

1. **Age:** The diabetes indicator rate generally increased across age categories, reaching approximately 21.85% in age category 11 before decreasing slightly in the following categories.

2. **General Health:** The diabetes indicator rate increased from 2.52% in the best general health category to 37.89% in the poorest general health category.

3. **High Blood Pressure:** The diabetes indicator rate was approximately 6.04% among respondents without high blood pressure, compared with 24.45% among respondents with high blood pressure.

These findings show associations between health-related features and the diabetes indicator in the dataset. They do not prove cause-and-effect relationships.

### 6. Limitation

One major limitation of this project is that the dataset is based on self-reported survey responses from 2015. Therefore, the information may contain reporting errors and may not represent current health conditions. The model has not been clinically validated and should not be used for medical diagnosis or treatment decisions.

**Conclusion:** Through this project, I learned how to explore a real-world dataset, prepare data, train machine learning models, compare their performance, and understand the importance of evaluating models on imbalanced data. The project also helped me understand why accuracy alone is not enough to select the best classification model.
