# Zomato-Smart-Suggestions
# Sentiment Analysis on Zomato Bangalore Dataset

This project demonstrates how to perform **Sentiment Analysis** on restaurant reviews using the **Zomato Bangalore Dataset**. The analysis involves text preprocessing, feature engineering, and training a deep learning model (**LSTM**) for review-based rating prediction.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Preprocessing](#preprocessing)
4. [Model](#model)
5. [Training and Evaluation](#training-and-evaluation)
6. [Results](#results)
7. [Setup](#setup)
8. [Contributing](#contributing)

---

## Introduction

Sentiment analysis is the computational task of determining the sentiment expressed in a piece of text. It helps in summarizing vast textual data by identifying emotions or polarities (positive/negative).

### Objectives:
- Understand people’s preferences for cuisine, location, and dining type.
- Predict restaurant ratings based on review comments using an LSTM model.

---

## Dataset

- **Dataset Source:** Zomato Bangalore Dataset
- **Number of Entries:** 51,717
- **Key Columns:**
  - `reviews_list`: User reviews
  - `rate`: Ratings (target variable)
  - `cuisines`: Restaurant cuisines
  - `location`: Restaurant locations

### Preprocessing Steps
1. Remove redundant columns and duplicates.
2. Handle missing values.
3. Normalize the `rate` column by removing `/5`.
4. Clean `reviews_list` using:
   - Lowercasing
   - Removing punctuations, stopwords, and URLs

---

## Model

The sentiment analysis model is built using an **LSTM** architecture and pre-trained FastText word embeddings.

### Architecture:
1. **Input Layer:** Tokenized review sequences
2. **Embedding Layer:** Pre-trained 300-dimensional FastText embeddings
3. **Spatial Dropout:** Prevent overfitting
4. **Bi-directional LSTM:** Extract contextual features
5. **Global Pooling Layers:** Max and average pooling
6. **Dense Layers:** Fully connected layers for classification
7. **Output Layer:** Softmax activation for 9 possible rating classes

---

## Training and Evaluation

### Training Process
- **Optimizer:** Adam
- **Loss Function:** Categorical Crossentropy
- **Batch Size:** 512
- **Epochs:** 10
- **Metrics:** Accuracy

### Model Performance (Validation Set)
- **Accuracy Progression:**
  - Epoch 1: 78.01%
  - Epoch 5: 92.17%
  - Epoch 10: 94.73%

---

## Results

- **Final Validation Accuracy:** 94.73%
- The model successfully predicts ratings based on user reviews.

---

## Setup

### Prerequisites
- Python 3.8+
- Libraries:
  - pandas
  - numpy
  - scikit-learn
  - keras
  - tensorflow
  - matplotlib


