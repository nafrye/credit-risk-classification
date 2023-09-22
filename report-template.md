# Module 12 Report Template

## Overview of the Analysis

This analysis examined potential factors for predicting loan status (healthy or at risk of default). Predictor variables were:
* loan size
* interest rate
* income of borrower
* debt to income ratio of borrower
* number of accounts
* derogatory marks
* total debt of borrower

Data provided included 77536 loans, of which 75036 were healthy and 2500 were in danger of default. Data were split into training and testing subsets, using loan status as a stratification variable. Two logistic regression models were developed. The second model used resampled training data for developing the model. 


## Results

The first model had a balanced accuracy rating of 94%. Likely due the the imbalance in types of loans, the model performed better in predicting healthy loans than it did in predicting loans in danger of defaulting. 
* All loans predicted to be healthy were healthy (100% precision)
* 15% of loans predicted to be in danger of default were not in danger of default (85% precision)
* Nearly all loans that were healhy were predicted as such (99% recall)
* 9% of loans that were in danger of default were not flagged as such (91% recall)

The second model, which used resampled data for training, performed better. The balanced accuracy of this model was nearly 100% (99.597%). This model also performed better with respect to healthy loans than those in danger of default.
* All loans predicted to be healthy were healthy (100% precision)
* 13% of loans predicted to be in danger of default were not in danger of default (87% precision)
* All loans that were healthy were predicted as such (100% recall)
* All loans that were in danger of default were flagged as such (100% recall)

## Summary

The second model, with resampled data for training, is recommended. Although this model has a risk of frustrating some customers, who will have their loans incorrectly flagged as potentially unhealthy, it correctly flagged all loans that were in fact in danger of default. 

In this model, errors in falsely flagging loans as potentially unhealthy may frustrate customers who would pay back their loans. At the same time, errors missing unhealthy loans might cost the lender money. In the second model, the 87% preceision with respect to potentially unhealthy loans suggests that some potential customers might be frustrated. But the 100% recall for unhealthy loans suggests that all unhealthy loans would be caught.

I would therefore recommend using the second model, provided that the lender has enough potential customers to not worry about the 13% who might be annoyed that they would be flagged as potentially defaulting.

If you do not recommend any of the models, please justify your reasoning.
