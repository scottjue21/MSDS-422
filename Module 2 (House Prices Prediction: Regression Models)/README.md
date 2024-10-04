# House Prices Prediction: Regression Models

This phase of the project builds on the **exploratory data analysis (EDA)** from the previous assignment, expanding into predictive modeling using various linear regression models. The goal is to predict house prices based on key features from the dataset.

## Dataset Overview
The dataset includes 79 variables that describe the various attributes of residential homes in Ames, Iowa. For more information on the dataset, visit:  
[House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)

## Objective
The goal in this assignment is to develop **linear regression models** using specific features that have high correlation with the sale price. Models are evaluated using **Root Mean Squared Error (RMSE)**.

## Regressions

### Linear Regression Model One
**Predictors:**  
- `OverallQual`
- `GrLivArea`
- `GarageCars`

This model uses the three variables with the highest correlation to predict house prices. The model's RMSE was **28,262.72**.

### Linear Regression Model Two
**Predictor:**  
- `OverallQual`

This simpler model only uses the `OverallQual` feature. The RMSE for this model was **34,507.57**.

### Linear Regression Model Three
**Predictor:**  
- `qual_space` (calculated by multiplying total square footage by overall quality)

This model introduces a new feature `qual_space`, created by combining the quality of the house with its total square footage. The RMSE for this model was **29,434.79**.

### Linear Regression Model Four
**Predictors:**  
- `qual_space`
- `GarageCars`

The final model combines `qual_space` and `GarageCars`. This model produced the best fit with the lowest RMSE of **27,481.54**.

## Techniques Used
- Development and evaluation of regression models
- Model performance assessment using Root Mean Squared Error (RMSE)
- Feature engineering for improved predictions

## Conclusion
Among the models, the **fourth model** using both `qual_space` and `GarageCars` resulted in the best prediction accuracy with the lowest RMSE.

## Contributors
This project was completed by:

- Scott Jue
- Zach Watson
