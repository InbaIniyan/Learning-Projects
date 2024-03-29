# Churn Prediction Project

## Project Overview

This project focuses on creating a robust spam detection model using machine learning techniques. The goal is to accurately identify and classify emails as either "ham" (non-spam) or "spam." The code provided encapsulates the entire process, from loading and preprocessing the dataset to training a machine learning model and evaluating its performance.

## Steps

### 1. Importing Libraries

In this step, essential libraries are imported to facilitate various tasks throughout the project. `pandas` is utilized for data manipulation, `matplotlib` for data visualization, `WordCloud` for visualizing word frequencies, and `scikit-learn` for machine learning functionalities, including the Naive Bayes classifier.

### 2. Loading Dataset

The dataset, stored in the 'spam.csv' file, is loaded using `pandas`. Columns with unnecessary information ('Unnamed: 2', 'Unnamed: 3', 'Unnamed: 4') are dropped, streamlining the dataset for further analysis.

### 3. Data Preprocessing

Email text and labels are extracted from the dataset. The 'v2' column containing email text is assigned to `X`, while the 'v1' column with labels (ham or spam) is assigned to `y`.

### 4. EDA (Exploratory Data Analysis)

#### (i) Class Distribution

A bar chart is generated to visually represent the distribution of classes (ham and spam). Understanding the class distribution is crucial for assessing the balance of the dataset.

#### (ii) Email Length Analysis

Histograms are created to analyze the distribution of email lengths for both ham and spam classes. This step provides insights into the typical length of emails in each category.

#### (iii) Word Frequency Analysis

Word clouds are generated to visualize the most frequent words in both ham and spam emails. This allows for a qualitative understanding of the content associated with each class.

### 5. Splitting the Data

The dataset is split into training and testing sets using `scikit-learn`'s `train_test_split` method. This separation ensures the model's performance is evaluated on unseen data.

### 6. Text Vectorization

CountVectorizer is employed to convert the email text into a numerical format suitable for machine learning models. This step involves creating a matrix of word counts for each email, allowing the model to work with the text data.

### 7. Build & Training the Model

A Multinomial Naive Bayes model is selected for its effectiveness in text classification tasks. The model is trained on the vectorized training data.

### 8. Make Predictions

The trained model is used to make predictions on the test set, classifying emails as ham or spam.

### 9. Model Evaluation

The accuracy of the model is calculated using `accuracy_score`, and a detailed classification report is generated using `classification_report`. These metrics provide a comprehensive assessment of the model's performance on the test set.

```python
Accuracy: 0.9838565022421525

Classification Report:

              precision    recall  f1-score   support

         ham       0.98      1.00      0.99       965
        spam       0.99      0.89      0.94       150

    accuracy                           0.98      1115
   macro avg       0.98      0.95      0.96      1115
weighted avg       0.98      0.98      0.98      1115
```
## Conclusion

In conclusion, this project successfully implemented a spam detection model using machine learning techniques. The journey through the various stages, from data loading and preprocessing to model training and evaluation, has provided valuable insights into the characteristics of spam and non-spam emails.

### Key Findings

1. **Class Distribution Analysis:** The initial exploratory data analysis revealed the distribution of classes, emphasizing the importance of handling class imbalances in training the model.

2. **Email Length Analysis:** The examination of email lengths for both ham and spam classes highlighted potential differences in communication styles between the two categories.

3. **Word Frequency Analysis:** Word clouds provided a visual representation of frequently occurring words in ham and spam emails, contributing to a better understanding of the distinctive features of each class.

4. **Model Performance:** The implemented Multinomial Naive Bayes model demonstrated [accuracy]% accuracy on the test set, as indicated in the classification report. Further fine-tuning and experimentation with different models or hyperparameters could enhance performance.

## How to Run

To run this project on your local environment, follow these steps:

### 1. Prerequisites

Ensure you have the required libraries installed. You can install them using pip:
```bash
pip install pandas matplotlib seaborn wordcloud scikit-learn
```
### 2. Dataset
Download the dataset ![spam.csv](spam.csv) and place it in the project directory.

### 3. Execute the Code
Execute the provided Python script to run the project.

## Future Work

1. **Feature Engineering:** Exploring additional features, such as sender information or email metadata, could enhance the model's ability to distinguish between ham and spam.

2. **Model Optimization:** Experimenting with other machine learning algorithms and optimizing hyperparameters may further improve the model's performance.

3. **Deployment:** Consideration for deploying the model in a real-world scenario, perhaps as part of an email filtering system, could be a valuable next step.

This project serves as a foundation for continued exploration and improvement in the field of spam detection. Contributions, feedback, and collaboration are welcome as we strive to create more effective and efficient models for identifying and mitigating spam emails.
