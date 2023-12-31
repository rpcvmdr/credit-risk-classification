# credit-risk-classification
Module 20 Challenge HW Assignment

CREATED BY: Michael Roberts, Nov. 19, 2023

==========================
This repository contains the folder Credit_Risk and this README.md file. The folder includes two files: 

1. lending_data.csv - The dataset used with this assignment 
2. credit_risk_classification.ipynb - The Jupyter file with the code to utilize a Logistic Regression Model to train a dataset to predict and identify records that represent healthy or at risk loans. 


CREDIT RISK ANALYSIS REPORT COMPONENT

[ANALYSIS OVERVIEW]

The purpose of this analysis is to describe the results of training and evaluating a Logistic Regression Model to determine the model's accuracy in identifying/predicting healthy and high risk loans from a company's dataset of loan activities. 

The LR model uses a CSV file dataset of 77,536 records of historical lending activity for this task. 

Each record includes 8 fields: loan_size, interest_rate, borrower_income, debt_to_income, number_of_accounts, derogatory_marks, total_debt and loan_status. 

The "loan_status" field has two possible categories: 0 = healthy status; 1 = high risk of defaulting. It is this loan_status field that the Logistic Regression Model will be used to correctly predict. 

[STAGES OF THE MACHINE LEARNING PROCESS/TRAINING PROCEDURE]

1. The CSV file "lending_data.csv" is read into a Pandas Dataframe and reviewed

2. The loan_status field is separated from the full dataset and assigned to the variable "y".

3. The loan_status field is removed from the original DataFrame. 

4. The revised DataFrame, now with 7 remaining fields - is assigned to the variable "X"

5. The dataset is divided into a Training Set (75% of the original dataset) and a Testing Set (25% of the original dataset) 
    using the train_test_split module. 

6. The LogisticsRegression module is imported, instantiated, fitted to the training data set
and saved with a name (lr_model)

7. The LR model is used to make a prediction of the test data and saved with the name: test_predictions

8. An accuracy score, confusion matrix (test_matrix) and a classification report (testing_report) are all 
    generated to evaluate the model using the testing data.

[ANALYSIS RESULTS]

[TESTING DATA USING LOGISTICS REGRESSION MODEL] 

  1. BALANCED ACCURACY - .944
  2. PRECISION - 99.6% (0 - Healthy Loans); 87.4% (1 - At Risk Loans)
  3. RECALL - 99.5% (0 - Healthy Loans); 89.2% (1 - At Risk Loans)

[SUMMARY]

1. The logistic regreesion model was extremely accurate in predicting 99.6% (18,679) - Almost Perfect High Precision Rate - of the 18,746 loans identified in 
    the dataset as healthy loans, were actually healthy loans.

2. The logistic regression model was also extremely accurate in predicting 99.5% (18,679) - Almost Perfect High Recall Rate - of the total amount of actual total healthy loans (18,759), were healthy loans.

3.  The logistic regression model was not as accurate, however, in terms of predicting high risk loans.

4.  The logistic regreesion model was able to correctly predict 87.4% (558) - Precision Rate - of the 638 loans identified in 
    the dataset as high risk loans were actually high risk loans. This means that 12.6% of the loans predicted by the model as high risk were not high risk loans.

5. The logistic regression model was was able to correctly predict 89% (558) - Recall Rate - of the total amount of actual high risk loans (625) were 
actually high risk loans. This means that the logistic regression model incorrectly predicted (missed/wrongly classified) 11% of true high risk loans to be healhy loans. 

[RECOMMENDATIONS]

1. The Logistics Regression Model is highly recommended for use in accurately predicting healthy loans at accuracy, precision and recall rates all above 99.5%.

2. However, the accuracy rates for predicting at risk loans is between 10 and 12% lower, in terms of recall and precision respectively than predicting healthly loans. The Logistics Regresssion Model should therefore not be used as the sole method of accurately predicting at risk loans.

3. 96.77% of the original dataset represents healthly loans, or 3.2% represents at risk loans.

4. However, relying on a model with 10-12% inaccuracies in predicting at risk loans potentially could lead to substantial lost revenue for the organization over time.  
