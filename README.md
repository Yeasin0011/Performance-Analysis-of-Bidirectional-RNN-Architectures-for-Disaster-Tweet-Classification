# Performance Analysis of Bidirectional RNN Architectures for Disaster Tweet Classification

## Introduction
This study examines the use of bidirectional recurrent neural networks (BiLSTM and BiGRU) for classifying disaster-related tweets. The dataset consists of tweets labeled as either disaster (1) or not disaster (0). Using GloVe embeddings for feature representation, five models, including Shallow RNN, UniLSTM, BiLSTM, UniGRU, and BiGRU, were trained and evaluated on accuracy, precision, recall, and F1 score. The results provide insights into the strengths and weaknesses of each architecture, demonstrating their suitability for disaster communication analysis.

## Data Description
Our dataset comprises:
- **Tweet**: Text content of the tweet.
- **Label (event)**: Binary classification indicating disaster (1) or not disaster (0).
- **Dataset**: [Kaggle - NLP Getting Started](https://www.kaggle.com/competitions/nlp-getting-started/code)

## Data Preprocessing
The dataset is split into 90% training and 10% testing data, with 10% of the training data used for validation. Data preprocessing includes:
1. **Tokenizing**: Tweets are converted to sequences of integers using a tokenizer, creating a word index based on the frequency of unique words.
2. **Padding**: Ensures all sequences have equal length for efficient model training.

## Embedding with GloVe
Pre-trained GloVe embeddings (100-dimensional vectors) were used to represent the vocabulary. An embedding matrix was initialized, where each word's vector was mapped based on the GloVe representation. Approximately 56.2% of the vocabulary had corresponding embeddings, improving semantic representation for training.

## Conclusion
This analysis compared five models, with the following observations:
- **BiGRU**: Exhibited the best overall performance with the highest testing F1 score (0.7750) and strong generalization.
- **BiLSTM**: Balanced performance, showing consistent results across training and testing phases.
- **UniLSTM**: Good training metrics but significant recall drop during testing, indicating overfitting.
- **UniGRU and Shallow RNN**: Struggled to generalize, with notable gaps in performance between training and testing.

Future improvements include hyperparameter tuning, advanced regularization techniques, and optimizing recall to enhance model reliability for disaster classification tasks.
