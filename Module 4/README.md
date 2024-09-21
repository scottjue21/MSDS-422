# Company Bankruptcy Prediction Project

## Project Overview

This project aims to predict company bankruptcy using a dataset from Kaggle. The dataset consists of 6,819 samples with 96 features, including various financial ratios and indicators.

## Data Source

The dataset is available at [Kaggle - Company Bankruptcy Prediction](https://www.kaggle.com/datasets/fedesoriano/company-bankruptcy-prediction).

## Analysis Steps

1. **Data Exploration**: 
   - Analyzed the dataset for missing values and determined that the target variable `Bankrupt?` had a significant class imbalance (3.3% bankrupt).

2. **Feature Selection**: 
   - Removed non-predictive features and identified the best predictors using SelectKBest.

3. **Data Preparation**: 
   - Used Isolation Forest to remove anomalies and applied SMOTE to balance the dataset.

4. **Model Building**: 
   - Built three machine learning models: Naïve Bayes, Logistic Regression, and SVM, with Naïve Bayes performing the best.

## Conclusion

The models show promising results, but potential overfitting was noted. Future work could involve refining feature selection and addressing overfitting.
