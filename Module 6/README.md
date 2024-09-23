# Handwritten Digit Recognition: Classification and Clustering Models

## Project Overview

This project uses the MNIST dataset to classify hand-drawn digit images ranging from 0 to 9. Several machine learning models were developed, including Random Forest, Principal Components Analysis (PCA) with Random Forest, and K-Means Clustering, to evaluate their performance in recognizing digits.

## Data Source

The dataset is available at [Kaggle - Digit Recognizer](https://www.kaggle.com/c/digit-recognizer).

## Data Preparation

1. **Exploratory Data Analysis (EDA)**: 
   - The dataset consists of 42,000 training images and 28,000 test images, each represented by 784 pixel values. 
   - Pixel values range from 0 (white) to 255 (black), with each row representing one image.

2. **Data Splitting**: 
   - The training dataset was split into an 80/20 training and testing set to validate model performance on unseen data.

3. **Feature Scaling**: 
   - StandardScaler was used to scale pixel values, improving model convergence and performance.

4. **Principal Components Analysis (PCA)**: 
   - PCA reduced the dimensionality of the dataset by transforming 784 pixel values into 154 principal components, representing 95% of the variability in the data.

## Model Building

Several machine learning models were developed to classify the digit images:

- **Random Forest**: Built using the full set of explanatory variables.
- **Random Forest with PCA**: Utilized the 154 principal components derived from PCA for classification.
- **K-Means Clustering**: Grouped observations into clusters and assigned digit labels based on the cluster numbers.

## Model Evaluation

- **Random Forest**: Achieved a Kaggle score of 0.966 with high precision and recall scores, making it the most effective model.
- **Random Forest with PCA**: Reduced dimensionality but slightly lower performance with a Kaggle score of 0.944.
- **K-Means Clustering**: The least effective model, with a Kaggle score of 0.896, but provided valuable insights for further exploration.

## Conclusion

The Random Forest model, both with and without PCA, performed well in classifying handwritten digits, with the best accuracy reaching 96.6%. K-Means clustering, while not as successful, provided an alternative approach to unsupervised learning for this task.

