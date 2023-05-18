# Credit Risk Analysis

## Overview of the Analysis

* Purpose of the analysis.

  The purpose is to build a model that can predict the creditworthiness of borrowers for a peer-to-peer lending services company using a historical lending activity Dataset. This model would identify the risk that a borrower will not pay back a loan or incorrectly identifying healthy loans as high-risk.

* What financial information the data was on, and what you needed to predict.

  The financial information that the data was on are loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks and total debt. We have to predict the loan status which is either healthy (value 0) or high risk (value 1).
  
* Basic information about the variables you were trying to predict (e.g., `value_counts`).

  After looking at the values in the loan status column by using value_counts function, There were more healthy loan data in the data set than the high risk. there were 75,036 healthy loans and only 2500 high risk loans. 

  After the data was oversampled, I did a value_counts again on the data and there were equal healthy and high risk loans (both 56271 each)

* Stages of the machine learning process you went through as part of this analysis.

  Splitting the data into Training and Testing samples, Fitting Logistic Regression Model, Resampling training data and also Analyzing the performance of the models

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

  Logistic Regression is able to predict the probability of a target variable in classification problems. Accuracy scores, balanced and imbalanced, were generated to assess for the number of correct predictions made by a model in relation to the total number of predictions made. A confusion matrix was also generated to compare the actual target values with those predicted by the models. A resampling method was completed on the Logistic Regression Model in order to better train and predict loan statuses.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
      * Confusion matrix - 56 False Positives (Actually Healthy predicted High Risk) and 102 False Negatives (Actually High Risk predicted Healthy)
      * Balanced Accuracy Score - 95%
      * Healthy Loan status  - Precision - 100% and Recall - 99%
      * High Risk Loan Status - Precision - 85% and Recall - 91%


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
      * Confusion matrix - 4 False Positives (Actually Healthy predicted High Risk) and 116 False Negatives (Actually High Risk predicted Healthy)
      * Balanced Accuracy Score - 99%
      * Healthy Loan status  - Precision - 100% and Recall - 99%
      * High Risk Loan Status - Precision - 84% and Recall - 99%

## Summary

The analysis shows it is better to use the Resampled model. The accuracy score is 99% which is more compared to 95% for the model on the original data. In identifying the healthy loan, both the models tend to have the same Precision of 100% and a Recall of 99%. But for high risk loans, the resampled data model has the comparably high Recall % which is 99% compared to the 91% for model on the original data. The number of false positives in the confusion matrix in the resampled model is also really less compared to the original data model. This will help the company identify high risk loans as high risk itself.

Hence, the most recommended model as per this analysis is the Resampled data Logistic Regression Model.
