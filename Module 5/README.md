# Company Bankruptcy Prediction Project 

## Project Overview

This project builds on a previous analyses to predict company bankruptcy using a Kaggle dataset. In addition to initial models, this iteration explores advanced machine learning techniques, including Random Forest, Gradient Boosted Trees, Gradient Boosting with Early Stopping, and Extra Trees models.

## Data Source

The dataset is available at [Kaggle - Company Bankruptcy Prediction](https://www.kaggle.com/datasets/fedesoriano/company-bankruptcy-prediction).

## Analysis Steps

1. **Data Exploration**: 
   - The dataset contains 6,819 samples and 96 features, with no missing values. The target variable `Bankrupt?` shows a significant imbalance.

2. **Feature Selection**: 
   - Features were selected using Sequential Feature Selector, identifying the top 15 predictors through a step-wise approach.

3. **Data Preparation**: 
   - Anomalies were removed using Isolation Forest, and the dataset was stratified to ensure balanced training and testing splits.

4. **Model Building**: 
   - Several advanced machine learning models were developed:
     - **Random Forest**: Achieved an accuracy score of 0.97 and an F1-score of 0.22.
     - **Gradient Boosted Trees**: Best-performing model with an F1-score of 0.41 and an accuracy score of 0.97.
     - **Gradient Boosting with Early Stopping**: Improved recall but slightly lower F1-score.
     - **Extra Trees**: Highest accuracy at 0.98 but low true positive rate.

## Conclusion

This expanded analysis shows improvement in model performance, with the maximum F1-score increasing from 0.28 to 0.41. Future work may focus on hyperparameter tuning, reintroducing SMOTE, and refining variable selection methods.
