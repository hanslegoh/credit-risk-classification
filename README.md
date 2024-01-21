# credit-risk-classification

**UCSD Data Science Bootcamp Module 20 Challenge**

## Overview of the Analysis

The purpose of this analysis is to create a supervised learning model that can identify the creditworthiness of borrowers and explain the effectiveness of it. The data is from a peer-to-peer lending services company of historical lending activities and it includes, but not limited to, the loan size, borrower's income, total debt, and most important, the loan status. The loan status is the dependent variable in our model and is considered healthy when the value is 0 and high-risk when it's 1. After the dependent and independent variables were split from the original data, both were split to create a training set and test set. A logistic regression model was used to fit and predict the data, and although a resampling method was attempted, there were continued import errors due to the discrepancies between the `imblearn` and `sklearn`modules.

## Results

* The accuracy, which illustrates a percentage of number of true positives and true negatives from the entire data, is 99%. Although this value is highly significant, it does not fully validate the effectiveness of the model because of its lack of focus in type I and type II errors.
* The precision for healthy loan status is the highest at 100%, which means that the model can correctly predict a healthy loan status with the given independent variables. The precision for high-risk loan status is 85%, which leaves room for type I errors and identify borrowers with healthy loan status as high-risk.
* The recall for healthy loan status is significantly high at 99%, so the model can avoid type I errors from truly healthy loan status borrowers. Similarly, the recall for high-risk loan status is 91%, which indicates that the model can be prone to type II errors.

## Summary

From the accuracy score of the logistic regression model alone, we can conclude that the model is effectively able to correctly identify the creditworthiness of borrowers. However, with a recall score of 91% for the high-risk loan status, falsely identifying high-risk borrwers as healthy can be detrimental to the company. 

Since most, if not all, financial services companies are structured as risk-averse, they would not want to risk lending money to a high-risk borrower who was falsely identified by the model. Moreover, the precision of high-risk loan status has less significance than the recall, even if the value is lower, because lenders would be more worried about lending money to high-risk borrowers than not lending money to healthy borrowers. There can be an argument that type I errors in the model are missed opportunities for the lenders, but because of the generally risk-averse nature of this business, the former argument is more significant for this analysis.

In conclusion, I recommend the use of this logistic regression model to identify the creditworthiness of borrowers after significant discussion and additional analysis on the precision and recall scores for high-risk borrowers. Since lenders are generally more focused on not lending money to high-risk borrowers (value 1 in the model) than lending money to healthy borrowers (value 0 in the model), the recall score for high-risk borrowers should be prioritized to be significantly close to or at 100%.

## Code Sources and Locations

- Starter code and data - from `Starter_Code` folder