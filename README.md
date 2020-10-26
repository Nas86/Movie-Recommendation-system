
# Module 3 Final Project:Credit Card Fraud Detection


## Introduction

Credit card fraud normally happens when consumers use their credit card number to unfamiliar individuals, when cards are lost or stolen, when mail is diverted from the intended recipient and taken by criminals, or when employees of a business copy the cards or card numbers of a cardholder. In this notebook I will develop a few ML models using anonymized credit card transaction data.

[Consumeraction](https://www.consumer-action.org/english/articles/questions_and_answers_about_credit_card_fraud/#:~:text=How%20does%20credit%20card%20fraud,card%20numbers%20of%20a%20cardholder.)

The datasets contains transactions made by credit cards in September 2013 by european cardholders.
This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation.  Features V1, V2, … V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.


## Problem Statement
The Credit Card Fraud Detection Problem includes modeling past credit card transactions with the knowledge of the ones that turned out to be fraud. This model is then used to identify whether a new transaction is fraudulent or not. my aim here is to detect 100% of the fraudulent transactions while minimizing the incorrect fraud classifications.

## Results and recommendations
I investigated the data, checking for data unbalancing, visualizing the features and understanding the relationship between different features. We then investigated 5 predictive models. The data was split in 2 parts, a train set and a test set. For the first three models, I used the Randomized Search and Adaboosting method.

<img src="/Picture/dis_time_amount.png">
<img src="/Picture/corr.png">
<img src="/Picture/dis.png"> 

Good prediction results can be achieved with imbalanced datasets as well as with balanced ones
Random Forest Classifiers has the best results being able to detect 70% fraud transactions and at the same time not classifying a lot of normal transactions as fraud
For testing data, Logistic regression and Supper vector Machine have the worst AUC among all the models. (AUC=50%), While the Random Forest has the highest AUC. (AUC=95%)
There is no perfect model and there will always be a trade-off between precision and recall. It is up to the company and its objectives to decide which approach is the best in each particular situation
