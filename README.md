# Life Insurance Risk Prediction

Deciding for Life Insurance for a person using machine learning based on a his/her health & history that includes BMI, Age, Ht, Wt, Employment_History, Insurance_History, Medical_History etc.

## Dataset

The [Prudential Life Insurance Assessment](https://www.kaggle.com/competitions/prudential-life-insurance-assessment/data) dataset has been used in this project.
This dataset consists of over a hundred variables describing attributes of life insurance applicants and over 50k rows (no. of applications).

## Exploratory Data Analysis

| For obvious reasons, <code>BMI</code> is the one of the most important factor for deciding the risk.  ![image](https://user-images.githubusercontent.com/56977388/182694178-86ee6883-70a7-49ab-928d-73283ced7c99.png) | Same for the <code>age</code> of person, more preferable option for insurance are young people.  ![image](https://user-images.githubusercontent.com/56977388/182695002-be654555-5a9f-407f-8b31-c65fcb356d1f.png) |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

Clearly shows most of people who got insurance had BMI between approx. 0.12 and 0.50
Rest features doesn't show any patterns.

<img alt="pairplot2" src="https://user-images.githubusercontent.com/56977388/182697908-573f4f72-ec48-4e3b-a758-a09ea3ecef07.png">

## ML Model

I used <code>Random Forest Classifier</code> model for prediction. Used <code>GridSearchCV</code> for hyperparameter tuning with <code>roc_auc</code> as scoring metric.
Acheved an accuracy of <code>80.8%</code> in training data and <code>80.4%</code> on test data.

| Confusion matrix for training data  ![image](https://user-images.githubusercontent.com/56977388/183244554-ac9685b5-84fc-4eec-bfa9-d1f65900b9e7.png) | Confusion matrix for test data  ![image](https://user-images.githubusercontent.com/56977388/183244582-13f13a59-f13d-4c20-9149-34a2c3a72f71.png) |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|


## Model Interpretation

| Important features for prediction  <p align="center">   <img alt="f_imp" src="https://user-images.githubusercontent.com/56977388/183244785-e3457575-b30f-49b0-b164-d597539c20c1.png"> </p> |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <p align="center">Understanding test model prediction using SHAP</p>  ![image](https://user-images.githubusercontent.com/56977388/183244842-00adca68-7b68-4874-9f09-a20ed1691f92.png)                                                 |
| ![image](https://user-images.githubusercontent.com/56977388/183244864-9262c99a-3cdd-4da3-8ee0-db93e0f4a79d.png)                                                                                      |
