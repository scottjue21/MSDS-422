# Disaster Tweet Classification

## Project Overview

This project focused on classifying tweets as either related to real disasters or not, using a dataset from the Kaggle competition "Natural Language Processing with Disaster Tweets." Two different model architectures were explored: Long Short-Term Memory (LSTM) models and Google's BERT (Bidirectional Encoder Representations from Transformers).

## Data Source

The dataset is available at [Kaggle - Natural Language Processing with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started/overview).

## Exploratory Data Analysis (EDA)

The training dataset consisted of 7,613 tweets with five features: id, keyword, location, text, and target. The target column indicated whether a tweet was related to a disaster (1) or not (0). Approximately 43% of the tweets were disaster-related, creating a slightly imbalanced dataset. Tweet lengths varied from 7 to 157 characters, with an average length of 101 characters. Common keywords and locations were identified, helping to understand the types of tweets associated with disasters.

## Data Preparation

Text data was preprocessed through a series of steps including punctuation removal, symbol conversion, and tokenization. URLs, mentions, and numbers were also replaced with text equivalents to normalize the tweet content. The data was then split into training and testing sets using an 80%-20% split.

## Model Building

### LSTM Models

Six LSTM models were built using different configurations of units (128, 256, 512) and batch sizes (32 or 64). These models were trained over several epochs and evaluated based on accuracy:
   - Model 1: 128 units, batch size 32, achieved the highest accuracy on the test data with a score of 0.777 and a Kaggle score of 0.765.
   - Other models had similar performance, with accuracy scores ranging from 0.747 to 0.777, indicating that the parameter adjustments did not significantly impact model performance.

### BERT Model

Google's BERT was also applied for disaster tweet classification. BERT's bidirectional nature allowed it to consider the full context of each token in a tweet. The model was fine-tuned for classification purposes and achieved a higher Kaggle score of 0.831. This performance demonstrated BERT's effectiveness in natural language processing tasks compared to RNN-based models.

## Model Evaluation

The LSTM models showed strong performance on the training data, with Model 1 achieving the best balance between accuracy and training efficiency. However, the BERT model outperformed the LSTM models on Kaggle's test data, suggesting that further exploration of transformer-based architectures could yield even better results.

## Conclusion

Both the LSTM and BERT models performed well on the disaster tweet classification task. The LSTM model achieved a Kaggle score of 0.765, while the BERT model achieved 0.831. Future work could involve further tuning of hyperparameters and deeper integration of transformer models for improved results in classifying disaster-related tweets.

