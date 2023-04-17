# Quora Insincere Questions Classification: Project Overview

This project aims to classify whether a question asked on Quora is sincere or not using pre-trained NLP text embedding models from TensorFlow Hub.

## Code and Resources Used
**Python Version:** 3.9  
**Project Inspiration:** [Coursera Project - Transfer Learning with NLP and TensorFlow Hub](https://www.coursera.org/projects/transfer-learning-nlp-tensorflow-hub)  
**Dataset:** [Quora Insincere Questions Classification on Kaggle](https://www.kaggle.com/c/quora-insincere-questions-classification/data)


## Data Preprocessing
- Class imbalance is treated with downsampling technique.
- The dataset is split into training and validation datasets with an 8:2 ratio.

## Model Building
The text classification model is built using pre-trained NLP text embedding models from Tensorflow Hub. The model architecture consists of the hub layer which includes the pre-trained model from Tensorflow Hub, followed by Dropout layers (with a dropout rate of 0.4) for regularization, and finally Dense layers for classification.

The pre-trained model used:
[universal-sentence-encoder-large](https://tfhub.dev/google/universal-sentence-encoder-large/5)

The hyperparameters used in the model training include:

- Optimizer: Adam optimizer (learning_rate=0.0001)
- Loss function: BinaryCrossentropy
- Metrics: accuracy
- Batch size: 32
- Number of epochs: 100
- Early stopping: EarlyStopping callback with a patience of 3

## Training and Validation Accuracy and Loss
The training and validation accuracy and loss are visualized in the following plots:

<img src="https://github.com/Gary0417/quora_insincere_questions_classification/blob/main/images/training_and_validation_loss.png">
<img src="https://github.com/Gary0417/quora_insincere_questions_classification/blob/main/images/training_and_validation_accuracy.png">

## Conclusion
Overall, the project aims to classify insincere questions on Quora using transfer learning with pre-trained NLP text embedding models, and the hyperparameters used during model training are optimized for the best performance. Further improvements could be made by exploring other NLP techniques and fine-tuning hyperparameters.
