# Handwritten Digit Recognition: Neural Networks

## Project Overview

This project focuses on predicting handwritten digits (0-9) using artificial neural networks (ANN) on the MNIST dataset. Two types of ANN models were developed and evaluated: Sequential models from Keras/TensorFlow and MLPClassifiers from scikit-learn. Various configurations of layers and nodes were tested to optimize accuracy while balancing computational time.

## Data Source

The dataset is available at [Kaggle - Digit Recognizer](https://www.kaggle.com/c/digit-recognizer).

## Analysis Steps

1. **Data Exploration**: 
   - The training dataset contains 42,000 rows and 785 columns, with 784 pixel values representing each image and one label column. The test dataset contains 28,000 rows and 784 columns without labels.

2. **Data Preparation**: 
   - We scaled the pixel values between 0 and 1 by dividing each pixel by 255.
   - The data was flattened for input into the neural networks.
   - The training data was split into training and validation sets (80% training, 20% validation) for model evaluation.

3. **Model Building**: 
   - **Sequential Neural Networks (Keras)**: We built and tested four Sequential models with {2, 4} layers and {50, 100} nodes, using early stopping to prevent overfitting.
   - **MLPClassifier (scikit-learn)**: We tested nine models with {1, 3, 5} layers and {10, 50, 100} nodes, exploring how the number of layers and nodes impacted model performance and computational time.

4. **Model Evaluation**: 
   - The performance of each model was measured based on training accuracy, testing accuracy, and Kaggle scores.
   - The best-performing models were:
     - **Sequential Model (2 layers, 50 nodes)**: Testing accuracy of 0.974, Kaggle score of 0.970.
     - **MLPClassifier Model (1 layer, 100 nodes)**: Testing accuracy of 0.99, Kaggle score of 0.973.
   - Models with fewer nodes trained faster, but models with 100 nodes generally achieved the highest accuracy.

## Conclusion

The artificial neural network models significantly improved the accuracy of handwritten digit recognition compared to previous approaches. The best models achieved testing accuracy of up to 0.99 and Kaggle scores as high as 0.973.

### Contributors
This project was completed by:

- Scott Jue
- Zach Watson
