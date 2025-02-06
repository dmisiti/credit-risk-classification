# Credit Risk Classification

## Overview of the Analysis

In this analysis, a logistic regression model was used to evaluate a dataset with historical lending activity, and make predictions about the creditworthiness of borrowers.

The data included information such as: loan size, interest rate, borrower income, and total debt, which all factored in to the model's determination of whether a loan was deemed healthy or high-risk.

The `loan_status` column of the data served as the variable the model was trying to predict. A negative output (0) correlates to a healthy loan, while a positive output (1) correlates to a high-risk loan.

The modeling process included:
1. Reading the data into a Jupyter Notebook via CSV.
2. Setting the `loan_status` column as the label `y` variable, and setting the rest of the data features in the `X` variable.
3. Splitting the data into training and testing datasets using `train_test_split`.
4. Fitting a logistic regression model by using the training data (`X_train` and `y_train`).
5. Saving the predictions for the testing data labels by using the testing feature data (`X_test`) and the fitted model.
6. Evaluating the model's performance via generation of a confusion matrix and classification report.

## Results

The model returned the following results:
* Overall accuracy: 99%
* Predicting healthy loans
    * Precision: 100%
    * Recall: 100%
* Predicting high-risk loans
    * Precision: 87%
    * Recall: 95%

## Summary

The model is very good at making predictions overall, with the overall accuracy rate being 99%. 

The model is especially good at predicting healthy loans, with precision and recall rates both nearly perfect (~100%). This means that whenever the model predicts a loan to be healthy, it is virtually always correct, and it virtually never overlooks any loans that should have been classified as healthy. 

Meanwhile, the model is still good at predicting high-risk loans, but not as good at predicting healthy loans. It has an 87% precision rate for high-risk, leaving 13% of the time that the model is incorrectly identifying a loan as high-risk. And it has a 95% recall rate for high-risk, leaving just 5% of the time that the model has overlooked a loan that should have been classified as high-risk.

Thus, the model is especially at its best when it is attempting to label loans in the healthy category, and it would be highly recommended to use the model for such purpose, though it also can certainly be used with confidence to a slightly less accurate degree in labeling loans in the high-risk category.
