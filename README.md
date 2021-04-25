# Credit Risk Analysis

## Overview
____
### Technologies used:

- Python 3.7.9
- Scikit Learn
- Imbalanced Learn
- NumPy
- Pandas

____

This analysis is a showcase of multiple supervised machine learning models and techniques to assess the risk of defaulting on credit card payments. We couple a Logistic Regression analysis with oversampling, undersampling, and combination sampling techniques, to produce predictive models with varying performance, and summarize these using basic characterizing metrics like Balanced Accuracy, Precision, and Recall
____
## Results

Below we summarize the performance of all six machine learning models tested in this analysis:

| Model                             | Balanced Accuracy | Precision | Recall |
|-----------------------------------|-------------------|-----------|--------|
| Native Random Sampling            | 0.678             | 0.01      | 0.72   |
| SMOTE (oversampling)              | 0.674             | 0.01      | 0.71   |
| Cluster Centroids (undersampling) | 0.655             | 0.01      | 0.71   |
| SMOTEENN (combination sampling)   | 0.670             | 0.01      | 0.71   |
| Balanced Random Forest            | 0.790             | 0.03      | 0.70   |
| Easy Ensemble (AdaBoost)          | 0.932             | 0.09      | 0.92   |

_____

## Summary

As seen above, the Easy Ensemble (AdaBoost) model produced the highest metrics for Balanced Accuracy, Precision, and Recall. 

A model with a 92% recall, can be expected to predict defaulting on credit card payments 92% of the time. However, it trades off this high recall with low precision. In other words, althoguh it can predict positivity 92% of the time, there is only a 9% chance that this prediction is actually correct. This model therefore has a **high false positivity rate**. 

Functionally, this is not useful for a bank to predict credit card defaulting from a customer-service perspective. From a bank's perspective, they would have to investigate a large majority of cases, but would predict those who will defualt 92% of the time. The ultimate decision as to the extent of using this model would be up to the individual organization.