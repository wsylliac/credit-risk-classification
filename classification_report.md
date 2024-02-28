# Credit Risk Analysis Report

![image](https://github.com/wsylliac/credit-risk-classification/assets/140991773/7f118bd5-e983-4a26-bd73-8cb01df491ae)


## Overview of the Analysis

Lending institutions provide funds or assets to individuals with the anticipation that these borrowers will either reimburse the borrowed amount or return the asset. The concept of Credit Risk emerges when a borrower fails to fulfill their obligation, resulting in potential financial losses for the lender. Lenders assess this risk through various metrics. In this classification challenege, I aimed to employ Machine Learning techniques to examine a dataset containing past lending transactions from a peer-to-peer lending platform. By doing so, there would be a model capable of evaluating the creditworthiness of borrowers based on historical patterns and attributes.

* Utilizing a machine learning approach, I aimed to discern between low-risk (healthy) and high-risk (non-healthy) loans based on the loan statuses provided by the lending company.

  * The Logistic Regression Algorithm emerges as the optimal tool for our machine learning endeavor, given its widespread application in predicting the probability of target variables in classification tasks.

* Employing the dataset furnished by the lending company, I constructed a Logistic Regression Model, achieving an accuracy score of 95%. However, despite the high accuracy, the model's recall value for non-healthy loans stands at 0.91, notably lower than the recall value of 0.99 for healthy loans. This discrepancy suggests that the model exhibits a stronger tendency to classify loans as healthy rather than non-healthy. This discrepancy can be attributed to the dataset's imbalance, wherein one class label (in this instance, healthy loans) significantly outweighs the other (non-healthy loans).

Based on the confusion matrix in step 3:

* For loans categorized as Healthy (low-risk), the model predicted 18,655 as Predicted Healthy Loans (low-risk) and 110 as Predicted Non-Healthy Loans (high-risk).

* For Non-Healthy Loans (high-risk), the model predicted 36 as Predicted Healthy Loans (low-risk) and 583 as Predicted Non-Healthy Loans (high-risk).



## Results

The Logistic Regression model trained on the Imbalanced DataSet accurately predicted healthy loans with 100% precision and non-healthy loans with 85% precision. In terms of recall scores, the model exhibited a 1% error rate in predicting healthy loans and a 9% error rate in predicting non-healthy loans.

The Logistic Regression model trained on the OverSampled DataSet accurately predicted healthy loans 100% of the time and non-healthy loans 84% of the time. Utilizing balanced (oversampled) data, the model demonstrates a significantly reduced likelihood of making the following mistakes:

* Misclassifying a healthy loan (low-risk) as a non-healthy loan (high-risk).
* Misclassifying a non-healthy loan (high-risk) as a healthy loan (low-risk).

According to the model's recall scores, it made a mere 1% error rate when predicting both healthy and non-healthy loans. The dataset's balance contributed to the model achieving an impressive accuracy score of 99%.

## Summary

A lending company seeks a model that accurately classifies healthy and non-healthy loans to mitigate potential losses:

* Misclassifying healthy loans as non-healthy may incur significant costs as it could lead to customer loss.
* Misidentifying non-healthy loans as healthy could also pose substantial financial risks for the lending company, resulting in potential losses of provided funds.

The Logistic Regression model trained on Oversampled data outperformed the model trained on Imbalanced data, mainly attributed to the balanced nature of the data. This resulted in a higher accuracy score and a superior recall, signifying fewer errors in classifying non-healthy loans.

Given the high risk associated with misclassifying non-healthy loans as healthy, the lending company likely prioritizes reducing False Positives. The confusion matrices below illustrate the model's correct and incorrect predictions of healthy and non-healthy loans.

Model fitted with Imbalanced Data:

    * 56 (FALSE POSITIVES) The observed value is categorized as healthy, while the forecasted value is classified as non-healthy.
    * 102 (FALSE NEGATIVES) The observed value is categorized as non-healthy, while the forecasted value is classified as healthy.


Model fitted with Balanced Data:

4 (FALSE POSITIVES) The observed value is categorized as healthy, while the forecasted value is classified as non-healthy.

116 (FALSE NEGATIVES) The observed value is categorized as non-healthy, while the forecasted value is classified as healthy.

As per the confusion matrices, there is a significant reduction in the number of False Positives, suggesting that the model is more accurate in classifying both healthy and non-healthy loans. Given this analysis, I would recommend utilizing Model 2, the Logistic Regression Model trained with Balanced (oversampled) data.
