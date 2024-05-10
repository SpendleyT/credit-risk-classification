# credit-risk-classification


The Task

The purpose of this exercise is to train and evaluate a model based on loan risk. Starting with a dataset of historical lending activity from a peer-to-peer lending services company, the task is to build a model that can identify the creditworthiness of borrowers.

The Data:
* The dataset used contained a number of facts about the loan and the borrower as potential measures of credit worthiness. These included:
    * The size of the loan in question
    * The interest rate for the loan
    * The borrower's total annual income
    * Their debt-to-income ratio
    * How many credit accounts they possessed
    * And how many times derogatory marks had appeared on the credit report
* The current loan status was also provided, and would be used in the validation of the model being developed.


The Process
* Step 1: Data preparation
    * Retrieve the data from the source (csv file), and review for irregularities.
    * Split the data into the measures (X) and the validation (y).
* Step 2: Test preparation
    * The next step was to split the data into the training and testing data sets (_train and _test). 
    * With the data split, it was ready to be used in fitting and executing the model.
* Step 3: Modeling
    * For this exercise, the Logisitic Regression model was used for determination of credit worthiness:
        * First, by fitting the model with training (_train) data to prepare it;
        * Second, by predicting the outcomes of the model with the test (X_test) data;
        * And last was to evaluate the model by comparing the prediciton results with the actual results in the y_test set.

The Results

The following are the results of the evaluation process (utilizing sklearns classification report):

* Logistic Regression:
    * Accuracy: the model correctly predicted 99% of the scores in the test data set.
    * Precision: The precision numbers showed a gap between the classes, with a Healthy rating matching 100% of the time, but the High-risk only hitting at an 85% rate. The far larger sample size of the healthy records (18765-619) meant the discrepency did not impact overall accuracy, but is something to take into consideration.
    * Recall: The gap for the recall scores were closer than the precision: 99%-91% for recall. 


## Summary

Based on the results, the Logisitic Regression model, would be an effective choice for determining credit-worthiness. 

* The model has an overall accuracy of 99%. More efficient models are unlikely to be found given the current data set.
* Additionally, the while the Healthy rating is consistently determined (100% precision, 99% recall), the High-Risk candidates have a higher recall score (91% recall, 85% precision). For financial security, it would be better to find every High-risk candidate, even if a few Healthy candidates are included in the group.


