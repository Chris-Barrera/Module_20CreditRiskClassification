# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

Explain the purpose of the analysis.

The purpose of this analysis is to find a model that can help predict whether a loan will be healthy or high-risk.

----------------------------------------------------------------------------------------------------------------------
Explain what financial information the data was on, and what you needed to predict.

The financial data included important variables to consisder like Income, debt-to-income loan size and total debt. With another model we can use the the weighted features function to find how much each variable contributed to a loan being healty or not.

----------------------------------------------------------------------------------------------------------------------
Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
 
At face value the information provided by the variables are pretty straight forward. Income refers to the amount that the person applying for the loan has declared, and loan size is how much the person is asking to borrow. Loan status is very important to our model because it becomes the target variable. 

----------------------------------------------------------------------------------------------------------------------
Describe the stages of the machine learning process you went through as part of this analysis.

Broadly speaking I first read in the data and got a sense of the data, I next identified the target variable and seperated it from the rest of the data. From there I used the train test split to begin the machine learning progress. Once fitted, predicted and scored I found some very good results.

----------------------------------------------------------------------------------------------------------------------
Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The LogisticRegression model works very good for our purpose here because we are ultimately looking a yes or no. 
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
         precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384

Our first model does a very good job finding out what a healthy loan looks like but the high-risk loans still need some catching up. 


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
          precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.99      0.91       619

    accuracy                           0.99     19384
   macro avg       0.92      0.99      0.95     19384
weighted avg       0.99      0.99      0.99     19384
Our second model with more exposure to high-risk loans via the RandomOverSampler, it can now better predict both types of loans.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
The second model performs better because while they both can identify healty loans the second model can identify high-risk loans much better. 
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )Performance does depend on the problem we are trying to solve and because we are trying to identify good loans from bad loans being able to identify both is very impotant.

The second model I believe does a great job at predicting future loans. With a high accuracy in identifying both healthy loans and high-risk this the second model does its job well.

If you do not recommend any of the models, please justify your reasoning.
