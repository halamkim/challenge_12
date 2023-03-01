## Overview of the Analysis

The purpose of this analysis is to use machine learning to train and compare a model so it can predict creditworthiness of borrowers more accurately. This model tests with raw data and improves the recall scores by resampling the training data. We first split our data into training and testing sets. We then went through the stages of model, fit, predict, evaluate to design our analysis. First we chose Logistic Regression as the model to use for our analysis. Then we fit that model to the training data and made predictions on the testing data. Finally we evaluated those predictions to see how they compared to the actual values. We then repeated this process with oversampled data by randomly oversampling the '1' class before modelling. This created Machine Learning Model 2. 

## Financial Data Used 
* In Resources Folder, there is a csv file of data on previous loans that includes a loan_status column. '0' means that the borrower is credit-worthy borrower, and '1' means that the borrower was at high-risk of paying back the loan. 
* Using this data, we created a model that can predict the loan-status. We compared it to the actual data and improved the model further. 

## Results

* Machine Learning Model 1:
  * Model 1 takes all the data as is which is 75036 data points for healthy loans and 2500 data points for high-risk loans. This was found by using 
  ```y.value_counts()```. 
  * With this model, the accuracy score was 94.5%.
  * For healthy loans, the precision score was 100%, and the recall score was 99%. 
  * For high-risk loans, the precision score was 85% and the recall score was 89%. 

* Machine Learning Model 2:
  * Using RandomOverSampler model, we resampled the data so there were 56260 data points for both high-risk and good loans. 
  * With this model, accuracy score was 99.3%. 
  * For healthy loans, the precision and recall scores stayed the same at 100% and 99% respectively. 
  * High-risk loan scores improved drastically. The recall score was 99% (was 89% from Machine Learning Model 1), although the precision score decreased from 85% to 84%. 


## Summary


* Of these two models, random oversampler data (Machine Learning Model 2) performed much better and is recommended over Model 1. It had a much higher accuracy score and recall score for the high-risk loans. If you're trying to predict '0's, the difference between two models will be minimum. However, when predicting to identify '1's, Machine Learning Model 2 is much more effective as it has a much higher accuracy score as well as the recall score. With the higher recall score, you're less likely to loan out to high-risk borrowers. 
