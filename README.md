# Diabetes Prediction - Classification

## Project Overview

This project is a machine learning classification project that predicts whether a patient has diabetes or not based on medical features.

The goal of this project is to understand the full machine learning workflow, including data exploration, preprocessing, model training, evaluation, model comparison, threshold tuning, and model improvement.

---

## Problem Type

This is a Binary Classification problem.

The target column is `Outcome`:

- `0` = No diabetes
- `1` = Diabetes

---

## Dataset

The dataset contains medical features such as:

- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age
- Outcome

---

## Project Goal

The goal is to predict whether a patient has diabetes.

Since this is a medical classification problem, accuracy alone is not enough.

The project focuses especially on Recall for class 1 because class 1 represents diabetic patients.

Missing a diabetic patient can be risky, so reducing false negatives is important.

---

## Project Steps

The project followed these steps:

1. Data loading
2. Initial data understanding
3. Target distribution analysis
4. Exploratory Data Analysis
5. Checking unrealistic zero values
6. Replacing unrealistic zero values with missing values
7. Filling missing values using the median
8. Correlation analysis
9. Feature and target split
10. Train/test split
11. Feature scaling
12. Training multiple classification models
13. Model evaluation
14. Confusion matrix analysis
15. ROC-AUC evaluation
16. Threshold tuning
17. Cross validation
18. Hyperparameter tuning using GridSearchCV
19. Feature importance
20. Final model selection

---

## Data Preprocessing

Some medical columns had unrealistic zero values.

For example:

- Glucose = 0
- BloodPressure = 0
- BMI = 0
- Insulin = 0
- SkinThickness = 0

These values were treated as missing values and replaced with `NaN`.

Then, missing values were filled using the median because the median is more robust to outliers than the mean.

---

## Models Used

The following classification models were trained and compared:

- Logistic Regression
- K-Nearest Neighbors
- Decision Tree
- Random Forest
- Support Vector Machine
- Tuned Random Forest

---

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC-AUC

For this project, Recall was especially important because we want to detect as many diabetic patients as possible.

---

## Threshold Tuning

The default classification threshold is usually `0.5`.

In this project, I tested a lower threshold, such as `0.4`, to increase recall for class 1.

Lowering the threshold helped the model detect more diabetic patients, but it also increased false positives.

This trade-off can be acceptable in medical problems because missing diabetic patients is more risky than asking non-diabetic patients for further testing.

---

## Key Insights

- Glucose had the highest correlation with diabetes outcome.
- BMI also showed an important relationship with diabetes.
- Accuracy alone was not enough to evaluate the model.
- Recall was very important because false negatives mean missed diabetic patients.
- Threshold tuning improved the ability of the model to detect diabetic patients.
- Random Forest and Logistic Regression performed well compared to other models.

---

## Limitations

This project has some limitations:

- The dataset is relatively small.
- Some columns had many missing or unrealistic zero values, especially Insulin and SkinThickness.
- Median imputation is simple and may not be the best method for real medical data.
- The model is for learning purposes only.
- It should not be used for real medical diagnosis.

---

## What I Learned

From this project, I learned:

- How to build a binary classification project
- How to identify features and target
- How to analyze target distribution
- How to handle unrealistic zero values
- How to use median imputation
- How to scale numerical features
- How to train multiple classification models
- How to evaluate models using Precision, Recall, F1-score, and Confusion Matrix
- Why Recall is important in medical classification problems
- How to calculate ROC-AUC
- How to tune the classification threshold
- How to use Cross Validation
- How to use GridSearchCV
- How to interpret Feature Importance

---

## Final Note

This project is for educational purposes.

The model can help understand patterns in the data, but it cannot replace medical diagnosis or professional clinical judgment.
