# Social Media Sentiment Analysis Project

## Overview

This project focuses on sentiment analysis of social media tweets. The goal is to build a model that can classify tweets into three sentiment categories: negative, neutral, and positive. The project involves data preprocessing, exploratory data analysis (EDA), text processing, model building, and evaluation.

## Steps

### 1. Importing Libraries

Essential libraries, including NumPy for numerical operations, Pandas for data manipulation, Matplotlib and Seaborn for data visualization, and WordCloud for creating visualizations, are imported. These libraries will facilitate various aspects of data analysis and model building.

### 2. Loading Dataset

The dataset containing social media tweets is loaded using Pandas. An initial exploration of the dataset is conducted to understand its structure, features, and characteristics. This step is crucial for gaining insights into the data that will inform subsequent processing.

### 3. Data Preprocessing

Relevant columns for sentiment analysis are selected from the dataset, focusing on "airline_sentiment" and "text." Sentiment labels are mapped to numerical values (0 for negative, 1 for neutral, and 2 for positive) to prepare the data for model training. Additionally, text preprocessing is performed to clean and standardize the tweet data.

### 4. Text Processing

Text processing involves tokenization, removing stopwords (commonly used words that do not contribute much to the meaning), and stemming (reducing words to their root form). These steps prepare the text data for analysis, improving the efficiency of the model in understanding sentiment-related features.

### 5. Splitting Data

The dataset is split into training and testing sets using the train_test_split function from scikit-learn. This separation allows for the development and evaluation of the sentiment analysis model on different subsets of the data.

### 6. EDA

Exploratory Data Analysis includes visualizations to gain insights into the distribution of sentiments, word frequency, tweet length patterns, and top words associated with each sentiment. These visualizations help in understanding the characteristics of the data and inform subsequent modeling decisions.

### 7. Building a Sentiment Analysis Model

A Multinomial Naive Bayes model is chosen for sentiment analysis. This model is implemented using scikit-learn's CountVectorizer for text vectorization. The choice of this model is based on its effectiveness in handling text data and classification tasks.

### 8. Predicting Sentiment for Sample Text

A function is created to predict the overall sentiment of a set of example texts using the trained model. This step demonstrates the practical application of the model on new data.

### 9. Model Evaluation

The performance of the sentiment analysis model is evaluated using classification metrics such as precision, recall, and F1-score. These metrics provide a comprehensive understanding of the model's ability to correctly classify sentiments.

```python
              precision    recall  f1-score   support

           0       0.80      0.95      0.87      1889
           1       0.68      0.41      0.51       580
           2       0.80      0.61      0.69       459

    accuracy                           0.79      2928
   macro avg       0.76      0.65      0.69      2928
weighted avg       0.78      0.79      0.77      2928
```

## Conclusion

### Key Achievements:

1. **Effective Classification:**
   - The Multinomial Naive Bayes model demonstrated accuracy in classifying social media sentiments.

2. **Insights from EDA:**
   - EDA provided valuable insights into sentiment distribution, word importance, and tweet length patterns.

3. **Robust Text Processing:**
   - Text preprocessing techniques enhanced the model's ability to discern sentiment-related features.
  

## How to Run

To run this project on your local environment, follow these steps:

1. Ensure you have the required libraries installed. You can install them using pip:

   ```bash
   pip install numpy pandas matplotlib seaborn wordcloud scikit-learn
   ```
2. Download the dataset ![Tweets.csv](Tweets.csv) and place it in the directory.
3. Execute the provided Python script to run the project.


### Future Work

1. **Hyperparameter Tuning:**
   - Experiment with different text vectorization techniques and model hyperparameters for further optimization.

2. **Deep Learning Approaches:**
   - Explore the application of deep learning models, such as recurrent neural networks (RNNs) or transformers, for improved sentiment analysis.

3. **Real-time Sentiment Analysis:**
   - Develop a system for real-time sentiment analysis to handle live data streams from social media platforms.

