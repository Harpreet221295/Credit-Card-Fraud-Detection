# Credit-Card-Fraud-Detection
## Link to the competition and dataset - https://www.kaggle.com/mlg-ulb/creditcardfraud

In this competition, we are given a dataset of credit card transactions for two days period. A transaction is assigned a class 1 if it is fraudulent transaction otherwise 0. We are given the Amount, Time and 28 PCA features. Our Goal is to classify a transaction as fraudulent or non-fraudulent.

This is an imbalanced dataset since fraud transactions only accounts for 0.172% and non-fraudulent transactions account for 99.828%.
In this notebook I have covered extensive exploratory data analysis and feature engineering. Since we are not provided with the test data, 15% of the training data is used for testing purpose. 

I have implemented two approaches for modeling - 
1. Trained a Decision Tree Classifier
2. Oversampling using Synthetic Minority Oversampling Technique(SMOTE) and training decision tree classifier on oversampled training dataset
For both of these approaches Hyperparameter Tuning has been performed using Randomized Search over range of different values of parameters.

Cross validation is also performed separately using two different metrics for scoring -  
1. roc-auc score
2. f1 score

Performance of the best model selected by cross-validation in each case is reported on test data using various metrics - area under precision-recall curve, auc-roc, classification report(precision, recall and f1 score) 
