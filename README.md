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
Acheved an accuracy of <code>81%</code> in training data and <code>80%</code> on test data.

| Confusion matrix for training data  ![image](https://user-images.githubusercontent.com/56977388/182699281-3479f7f3-ec3a-40ab-b2de-021f0a1e0cbf.png) | Confusion matrix for test data  ![image](https://user-images.githubusercontent.com/56977388/182699316-b2b6bf59-c8c2-48d8-b709-5ab60dd9d6b5.png) |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|


## Model Interpretation

| Important features for prediction  <p align="center">   <img width=750 alt="f_imp" src="https://user-images.githubusercontent.com/56977388/182700282-1c04bd2b-be81-4e12-989c-1aaee5a47838.png"> </p> |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <p align="center">Understanding test model prediction using SHAP</p>  ![image](https://user-images.githubusercontent.com/56977388/182701404-81e933d7-597d-4746-bb11-5be9a3bcdd11.png)                                                 |
| ![image](https://user-images.githubusercontent.com/56977388/182702739-99633f7f-bc72-4cc0-b1fa-e5e8e7d028be.png)                                                                                      |
