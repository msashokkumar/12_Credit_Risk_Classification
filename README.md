# Credit Risk Classification

## Purpose of the Analysis

The purpose of the analysis is to identify the creditworthiness of borrowers for a peer-to-peer lending company.

### Problem Statement

Historical loan data was provided to predict `health loans` vs `high risk loans`.

### Variables

`value_counts` represents the count of majority class and the minority class. For a proper prediction model it is important to provide equal number of instances for both the classes.

### Stages of the machine learning

1. Preparing Data
2. Choosing a model -  Logistic Regression
3. Training the model
4. Evaluating the model
5. Parameter Tuning - Resampled Training Data
6. Predictions

### Methods Used

Logistic regression is a statistical model that in its basic form uses a logistic function to model a binary dependent variable, although many more complex extensions exist. In regression analysis, logistic regression[1] (or logit regression) is estimating the parameters of a logistic model (a form of binary regression). Mathematically, a binary logistic model has a dependent variable with two possible values, such as pass/fail which is represented by an indicator variable, where the two values are labeled "0" and "1". [Ref: Wikipedia]

In random oversampling, we randomly select instances of the minority class and add them to the training set until we’ve balanced the majority and minority classes.

## Results

* Logistics Regression with Original Data
    * Model was applied with the original available data
    * Accuracy:  0.9520479254722232
    * Precision: 0: 1.00 1: 0.85
    * Recall:    0: 0.99 1: 0.91
    
* Logistics Regression with Random Over Sampler
    * Model was applied with boosting traning values for unhealthy loans
    * Accuracy:  0.9947308560359689
    * Precision: 0: 0.99 1: 0.99
    * Recall:    0: 0.99 1: 0.99
    
## Summary

Both approaches provide unique insight into predict loan categories - healthy vs unhealthy. Since we are trying to solve a problem which is categorically imbalance, Random Over Sampler (Resampled Training Data) makes a better choice for this usecase.

With a better accuracy (0.99) and equal precision for both healthy and unhealthy loans makes its a good choice.



