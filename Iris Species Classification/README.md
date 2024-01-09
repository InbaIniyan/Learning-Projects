# Iris Species Classification Project

## Overview

This project aims to classify iris species based on sepal and petal characteristics using machine learning techniques. The dataset provides features such as sepal length, sepal width, petal length, and petal width, along with the corresponding iris species label.

## Steps

### 1. Import Libraries

Essential libraries are imported, including `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`, and `SVC` for Support Vector Classification.

### 2. Load & Explore Dataset

The Iris dataset is loaded, providing information about iris species' sepal and petal attributes. Class distribution is examined to understand the dataset's composition.

### 3. EDA (Exploratory Data Analysis)

#### (i) Histograms for Each Feature

Histograms are plotted to visualize the distribution of sepal and petal features, allowing us to understand the range and frequency of each attribute.

#### (ii) Box Plots for Feature Distributions by Class

Box plots are used to observe how sepal length varies across different iris species, providing insights into the characteristic differences.

#### (iii) Pair Plots

Pair plots visualize relationships between features, with species distinguished by color. This step aids in identifying patterns and potential separability.

#### (iv) Correlation Heatmap

The correlation heatmap displays the relationships between numerical features, helping to identify correlations that may influence the classification.

#### (v) Scatter Plots

Scatter plots illustrate relationships between two features, such as sepal length and petal length, providing a visual representation of data distribution.

### 4. Data Preprocessing

Features and labels are extracted, and the dataset is split into training and testing sets. Standardization is applied to ensure consistent scaling across features.

### 5. Training the Model

A Support Vector Classifier (SVC) with a linear kernel is chosen for its ability to handle multiclass classification. The model is trained on the scaled training data.

### 6. Testing the Model

The trained model is employed to predict iris species labels for the test dataset.

### 7. Model Evaluation

- **Confusion Matrix:** Analyzes true positives, true negatives, false positives, and false negatives.
  
- **Classification Report:** Provides precision, recall, and F1-score for each class.
  
- **Accuracy Score:** Quantifies the model's overall accuracy on the test set.

```python
1.) Confusion Matrix:
[[10  0  0]
 [ 0  8  1]
 [ 0  0 11]]

2.) Classification Report:

                 precision    recall  f1-score   support

    Iris-setosa       1.00      1.00      1.00        10
Iris-versicolor       1.00      0.89      0.94         9
 Iris-virginica       0.92      1.00      0.96        11

       accuracy                           0.97        30
      macro avg       0.97      0.96      0.97        30
   weighted avg       0.97      0.97      0.97        30

3.) Accuracy: 96.67%
```

## Conclusion

The Iris Species Classification project successfully implemented a Support Vector Classifier (SVC) with a linear kernel to predict iris species based on sepal and petal characteristics. Through a systematic approach encompassing data exploration, model training, and evaluation, several key findings and insights were derived.

### Key Achievements:

1. **Effective Classification:**
   - The Support Vector Classifier demonstrated commendable accuracy in classifying iris species, showcasing the model's capability to learn and generalize from the provided dataset.

2. **Feature Significance:**
   - Features such as sepal length, sepal width, petal length, and petal width were identified as crucial in distinguishing between different iris species. The model's ability to leverage these features contributed significantly to its predictive power.

3. **Robustness to Outliers:**
   - The absence of significant outliers in the dataset indicated that the model maintained robustness, exhibiting stability in predictions even when faced with extreme data points.

## How to Run

To run this project on your local environment, follow these steps:

1. Ensure you have the required libraries installed. You can install them using pip:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
2. Download the ![iris.csv](iris.csv) and place it in the directory.
3. Execute the provided Python script to run the project.

## Future Work:

1. **Hyperparameter Tuning:**
   - Further exploration of different kernel types and regularization parameters could be undertaken to fine-tune the SVC for optimal performance.

2. **Feature Engineering:**
   - Experimentation with additional features or transformations may enhance the model's discriminatory power, potentially leading to improved accuracy.

3. **Ensemble Methods:**
   - Investigation into ensemble methods, such as Random Forest or Gradient Boosting, could be considered to explore alternative approaches to iris species classification.
