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

### Conclusion
Among the models, the **fourth model** using both `qual_space` and `GarageCars` resulted in the best prediction accuracy with the lowest RMSE.

## Testing
The trained model was tested on a Kaggle-provided test set. The following steps were used to prepare the test data:
1. Handle missing values by replacing NaN values with zero.
2. Create the `qual_space` predictor variable by multiplying overall quality by the total square footage.
3. Predict the `SalePrice` for each house using the final regression model.

The predictions were submitted in a `.csv` file, formatted for Kaggle.

## Practice Skills
- Regression model development and evaluation
- Root Mean Squared Error (RMSE) analysis for model performance
- Feature engineering for improved predictions
