# Cats vs Dogs Image Classification: Convolutional Neural Networks

## Project Overview

This project uses convolutional neural networks (CNN) to predict whether an image contains a cat or a dog, using the dataset from the Kaggle competition "Dogs vs. Cats Redux." Several CNN models were built and evaluated based on accuracy, training time, and generalization performance.

## Data Source

The dataset is available at [Kaggle - Dogs vs. Cats Redux: Kernels Edition](https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition).

## Exploratory Data Analysis (EDA)

The dataset contains 25,000 labeled training images of cats and dogs and 12,500 unlabeled test images. Each image was a color image with varying dimensions, roughly square, and ranging from about 250x250 pixels to 500x500 pixels. EDA confirmed that the training set was balanced, with 12,500 images of cats and 12,500 images of dogs. Sample images were visually inspected to confirm data quality. The category labels were assigned based on the filenames: images starting with ‘cat’ were labeled as 0 and images starting with ‘dog’ as 1.

## Data Preparation

The images were preprocessed using TensorFlow's `ImageDataGenerator` to convert image files into arrays, rescale pixel values (0-255) to a range of 0-1, and resize all images to 128x128 pixels. Data was augmented using random transformations such as rotation and zoom. A smaller dataset of 26,000 images was initially used for faster model training.

## Model Building

Three CNN models were built using Keras with TensorFlow, each with the same architecture but differing in the number of neurons (filters) in their convolutional layers. The models were trained with 10 epochs, using dropout regularization to prevent overfitting, and `rmsprop` as the optimizer.
   - Model 1: 64 neurons, achieved 0.725 accuracy.
   - Model 2: 128 neurons, achieved 0.698 accuracy.
   - Model 3: 256 neurons, achieved 0.723 accuracy.

## Final Model Training

The best-performing model (Model 1) was retrained using the full dataset of 25,000 images with 64 neurons. Due to time constraints in Google Colab, this model was trained for only 3 epochs, achieving an accuracy of 0.744 and a loss of 0.504.

## Model Evaluation

The final model was used to predict the labels for the Kaggle test dataset, yielding a Kaggle score of 8.75. Despite good performance on the training set, the model did not generalize well to the test data, indicating overfitting.

## Conclusion

The CNN models performed well on the training data but struggled to generalize to the test data. The best model achieved an accuracy of 0.744 on the training data but received a relatively low Kaggle score. Future improvements could include additional hyperparameter tuning and more extensive use of regularization techniques to improve generalization.

### Contributors
This project was completed by:

- Scott Jue
- Zach Watson


