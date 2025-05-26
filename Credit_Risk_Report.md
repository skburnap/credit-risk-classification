# Credit Risk Classification Report

## Executive Summary

* **Objective** – The goal of this analysis to determine if the Logistic Regression machine learning model can more accurately predict healthy loans versus high-risk loans using the original dataset or a dataset that is resampled to increase the size of the minority class.

* **Dataset Description** – The dataset used to perform the analysis consists of information on 77,536 loans. The data includes columns for  loan_size, interest_rate, borrower_income, debt_to_income ratio, number_of_accounts, derotatory_marks, total_debt, and loan_status. The target variable in this analysis is **loan_status**. The data provided in the remaining columns will be used as features to train the data and inform the predictions. 

* **Methodology** – The stages of the machine learning process are very scripted. If followed in order, they provide you with an accurate assessment of the model's ability to make predictions. The stages of the machine learning process are as follows:

    - Prepare the data - Import the file, establish the DataFrame, evaluate the columns and features. 
    
    - Separate the data into features and labels - The labels are what you are attempting to predict, is the status of the loan healthy (0) or high-risk (1). The features are all of the remaining data you will use to train and test the model.
    
    - Use the train_test_split function to separate the features and labels data into training and testing datasets. 
    
    - Import the machine learning model from the library - In this instance, we will be importing LogisticRegression from SKLearn. 
    
    - Instantiate the model.
    
    - Fit the model using the training data.
    
    - Use the model to make predictions using the features test data.
    
    - Evaluate the predictions - Evaluations are done by calculating and comparing metrics like accuracy score, a confusion matrix, and a classification report.
    
* **Modeling Techniques Applied** – 

    The primary model used in this analysis is:

    - LogisticRegression model from SKLearn
    
    Supporting functions used in this analysis are:
    
    - train_test_split from SKLearn
    
    Models are evaluated using the following functions:

    - confustion_matrix from SKLearn
    - classification_report from SKLearn

## Evaluation Results

The following summarizes the key evaluation metrics from the logistic regression model, including accuracy, precision, and recall scores.

* Machine Learning Model 1 - Logistic Regression:
  
  - Accuracy score: 0.99
  - Precision: Class 0: 1.00 Class 1: 0.85
  - Recall: Class 0: 0.99 Class 1: 0.91

## Conclusion

Overall, the Logistic Regression model demonstrated strong performance, particularly in predicting Class 0 (healthy loans). For the 0 class, both the precision and the recall were extremely close to perfect.

For the 1 class (high-risk loans), the model's precision is 0.84 the recall is 0.91. This indicates that the model more often gives false positives than false negatives.

These findings suggest that the Logistic Regression model is effective at predicting both healthy and high-risk loans, based on the selected training features. 

While the model shows promise, further validation using different datasets is necessary before deployment for production-level credit risk assessment.