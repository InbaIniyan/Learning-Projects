# Diabetes Prediction Project

## Overview

This project focuses on predicting diabetes based on various health-related features. It utilizes machine learning techniques to analyze a dataset containing information about individuals, aiming to build a model that can accurately classify whether a person is likely to have diabetes or not.

## Steps

### 1. Importing Libraries

Essential libraries such as `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`, and `RandomForestClassifier` are imported to handle data manipulation, visualization, and machine learning tasks.

### 2. Load & Explore Dataset

The dataset is loaded from 'dataset/diabetes.csv', and initial exploration is conducted to understand its structure. Basic statistics and information about missing values are displayed to gain insights into the dataset.

### 3. EDA (Exploratory Data Analysis)

#### (i) Histograms for Numerical Features

Histograms are plotted to visualize the distribution of numerical features in the dataset.

#### (ii) Box Plots for Outlier Detection

Box plots are generated to identify potential outliers in the numerical features.

#### (iii) Correlation Matrix

A correlation matrix is created to visualize relationships between different features in the dataset.

#### (iv) Pair Plots (Scatter Matrix)

Pair plots are generated to explore relationships between selected features, with outcomes differentiated by color.

#### (v) Pairwise Scatter Plots with the Target Variable

Pair plots with the hue set to the 'Outcome' variable provide insights into the relationships between features and the target variable.

### 4. Data Preprocessing

The data is split into features (X) and the target variable (y). Standardization is applied to the feature data to ensure consistent scaling.

### 5. Choose a Machine Learning Algorithm

A Random Forest Classifier is chosen as the machine learning algorithm due to its versatility and effectiveness in classification tasks.

### 6. Train the Model

The Random Forest Classifier is trained on the training data.

### 7. Hyperparameter Tuning

Grid search is utilized to find the best hyperparameters for the Random Forest Classifier, enhancing the model's performance.

### 8. Model Evaluation

The trained model is evaluated on the test data, and metrics such as accuracy, confusion matrix, and classification report are displayed.

### 9. Model Assessment

#### (i) Confusion Matrix Heatmap

A heatmap of the confusion matrix provides a visual representation of the model's performance.

#### (ii) ROC Curve

The ROC curve is plotted to assess the trade-off between true positive and false positive rates.

#### (iii) Precision-Recall Curve

The Precision-Recall curve is generated to analyze the precision-recall trade-off.

#### (iv) Probability Distribution

Histograms of predicted probabilities for both classes are plotted to visualize the distribution.
