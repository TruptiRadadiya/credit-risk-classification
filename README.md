# credit-risk-classification

## Credit Risk Analysis Report

### Overview of the Analysis

##### Purpose of the Analysis

The primary objective of this analysis is to build and evaluate a machine learning model that can identify the creditworthiness of borrowers using historical lending data. The goal is to predict whether a loan will be healthy or at high risk of defaulting, which is crucial for making informed lending decisions.

##### Financial Information and Prediction

The dataset contains historical lending activity data from a peer-to-peer lending services company. The financial information includes various features related to the borrower's profile and loan details, such as loan amount, interest rate, borrower income, and more. The target variable, `loan_status`, indicates the credit risk:

- A value of `0` means the loan is healthy.
- A value of `1` means the loan has a high risk of defaulting.

##### Variables Overview

The `loan_status` column is the label set (y), while the remaining columns form the features set (X). The `value_counts` of the `loan_status` column are as follows:

- Healthy loans (0): X instances
- High-risk loans (1): y instances

##### Machine Learning Process Stages

The machine learning process included the following stages:

1. <strong>Data Loading and Preparation:</strong> Read the data from `lending_data.csv` into a Pandas DataFrame.
2. <strong>Feature and Label Creation:</strong> Create the labels set (y) from the `loan_status` column and the features set (X) from the remaining columns.
3. <strong>Data Splitting:</strong> Split the data into training and testing sets using `train_test_split`.
4. <strong>Model Training:</strong> Fit a Logistic Regression model using the training data (X_train and y_train).
5. <strong>Model Prediction:</strong> Save the predictions for the testing data labels using the testing feature data (X_test).
6. <strong>Model Evaluation:</strong> Evaluate the model’s performance by generating a confusion matrix and printing the classification report.

##### Methods Used

- <strong>Logistic Regression:</strong> This algorithm was chosen for its simplicity and effectiveness in binary classification problems like predicting loan risk.

### Results

- <strong>Machine Learning Model 1:</strong> Logistic Regression

  - <strong>Accuracy:</strong> The model's accuracy score was `0.99`.
  - <strong>Precision:</strong> The precision score for predicting high-risk loans was `0.87`.
  - <strong>Recall:</strong> The recall score for predicting high-risk loans was `0.89`.

  - <strong>Confusion Matrix</strong>

    - <strong>True Positives (TP):</strong> 556
    - <strong>True Negatives (TN):</strong> 18759
    - <strong>False Positives (FP):</strong> 69
    - <strong>False Negatives (FN):</strong> 69

  - <strong>Classification Report</strong>

    - <strong>Precision:</strong>
      - <strong>Healthy loans (0):</strong> 1.00
      - <strong>High-risk loans (1):</strong> 0.87
    - <strong>Recall:</strong>
      - <strong>Healthy loans (0):</strong> 1.00
      - <strong>High-risk loans (1):</strong> 0.89
    - <strong>F1 Score:</strong>
      - <strong>Healthy loans (0):</strong> 1.00
      - <strong>High-risk loans (1):</strong> 0.88

### Summary

##### Model Performance

The Logistic Regression model performed exceptionally well in identifying both healthy and high-risk loans. The precision and recall scores indicate that the model is highly accurate in predicting loan statuses, with an overall accuracy of 99%.

##### Recommendations

- <strong>Best Performing Model:</strong> The Logistic Regression model is currently the best performing model based on its high accuracy, precision, and recall scores.
- <strong>Importance of Predictions:</strong> Depending on the business requirement, if predicting high-risk loans (1’s) is more critical, the model’s recall for high-risk loans should be prioritized. Conversely, if avoiding false positives (incorrectly predicting a loan as high-risk) is more important, precision should be prioritized.

##### Final Recommendation

Given the results, the Logistic Regression model is recommended for predicting loan risk. However, further tuning and testing with additional models might improve performance, especially if different aspects of model performance (precision vs. recall) are more important for specific business needs.
