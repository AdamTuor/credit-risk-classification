# credit-risk-classification

## Overview of the Analysis

* The purpose of this analysis was to create a model to predict creditworthiness of borrowers
* The input of this model included the amount of the loan, interest rate, income of the borrower, a debt to income ratio, number of accounts, derogatory marks, and the borrower's total debt.
* The goal of the model was to predict if the loan would be "healthy"(0) or "high-risk"(1).
* The data was split into training and test sets and fit to a LogisticRegression model for analysis.
* Resampling was done due to the imbalanced nature of the data, which initially had 75000 "healthy" loans and only 2500 "high-risk" loans.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * This model did extremely well predicting healthy loans, but had some trouble identifying high-risk loans since only 85% of the predictions were true positives.

|    | precision | recall | f1-score | support |
|----|-----------|--------|----------|---------|
|  0 |   1.00    |  0.99  |   1.00   |  18765  |
|  1 |   0.85    |  0.91  |   0.88   |   619   |
|----|-----------|--------|----------|---------|
|    |           |        |          |         |
|accuracy|         |        |   0.99   |  19384  |
|macro avg|   0.92    |  0.95  |   0.94   |  19384  |
|weighted avg| 0.99 |  0.99  |   0.99   |  19384  |




* Machine Learning Model 2:
  * The second model performed exactly the same on the healthy loans, but saw a significant increase on recall for high-risk loans. Precision went down slighly.
|    | precision | recall | f1-score | support |
|----|-----------|--------|----------|---------|
|  0 |   1.00    |  0.99  |   1.00   |  18765  |
|  1 |   0.84    |  0.99  |   0.91   |   619   |
|----|-----------|--------|----------|---------|
|    |           |        |          |         |
|accuracy|         |        |   0.99   |  19384  |
|macro avg|   0.92    |  0.99  |   0.95   |  19384  |
|weighted avg| 0.99 |  0.99  |   0.99   |  19384  |


## Summary

* The second model seems to perform better overall with higher recall for both loan categories.
* For a financial institute I belive the second model would be preferred.  I believe that, for the business, it would be more important to identify high-risk loans, which the second model did with 99% recall.  Those customers who fall into the 16% of false positives could appeal the decision which would not be a huge deal.


