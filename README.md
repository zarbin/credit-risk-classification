# Credit Risk Classification - Homework 20
UTA DataViz Bootcamp <br>
03/23/2023

# Summary

In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

The dataset provided by the bank contains 77,536 records with seven key indicators.

* Size of the loan
* Interest rate on the loan
* Borrower's income
* Debt_to_Income ratio
* The number of of accounts that the borrower uses regularly
* Derogatory marks on the borrower's credit report
* The borrower's total debt
* loan status ('1' indicates that the borrower defaulted, a '0' indicates a healthy loan)


# Work and Findings

Data Preview

![image](https://user-images.githubusercontent.com/36682023/227839168-06bdc7af-7381-4630-9eeb-97e286232813.png)


## Create a Logistic Regression Model with the Original Data

Machine Learning Model **1**, Logistic Regression **using raw data**:

  Balanced Accuracy Score 0.9520479254722232

    Confusion Matrix results
          True positive:  18663   
          False positive: 56
          True negative:  563
          False negative: 102

---

                    precision   recall  f1-score   support

       0                1.00      0.99      1.00     18765
       1                0.85      0.91      0.88       619

        accuracy                            0.99     19384
        macro avg       0.92      0.95      0.94     19384
        weighted avg    0.99      0.99      0.99     19384


**Question:** How well does the logistic regression model predict both the `0` (healthy loan) and `1` (high-risk loan) labels?

**Answer:** The prediction model show a high accuracy of 99%. Precision in predicting loan defaults is 85%.  While good, there might be room for imporovement here and likely why we are doing the below additional work :)   

Precision for healthy loans is nearly perfect. The accuracy of the model is also high. 

## Predict a Logistic Regression Model with Resampled Training Data

Machine Learning Model **2**, Logistic Regression **using raw data and Random Oversampling**:

  Balanced Accuracy Score 0.9936781215845847

    Confusion Matrix results
          True positive:  18649  
          False positive: 4
          True negative:  615
          False negative: 116

---

                      precision   recall  f1-score   support

         0                1.00      0.99      1.00     18765
         1                0.84      0.99      0.91       619

          accuracy                            0.99     19384
          macro avg       0.92      0.99      0.95     19384
          weighted avg    0.99      0.99      0.99     19384


**Question:** How well does the logistic regression model, fit with oversampled data, predict both the `0` (healthy loan) and `1` (high-risk loan) labels?

**Answer:** For the oversampled data, the model was extremely accurate at 99%.  Also there was improvment in model accuraccy as it predicted 99% of the laons that actually did default.  With only 4 false positives and 116 false negatives this model is reliable for predicting loans and an improvement on what our original training model. 

