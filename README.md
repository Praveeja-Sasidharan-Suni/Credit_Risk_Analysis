# Credit_Risk_Analysis

## Overview
 Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. 
Therefore, we will need to employ different techniques to train and evaluate models with unbalanced classes.
In this project, we use Python to build and evaluate several machine learning models to predict credit risk.
We have adopted the following procedure:
- oversample the data using the **RandomOverSampler** and **SMOTE** algorithms.
- Undersample the data using the **ClusterCentroids** algorithm.
- Use a combinatorial approach of over- and undersampling using the **SMOTEENN** algorithm.
- Compare two machine learning models that reduce bias, **BalancedRandomForestClassifier** and **EasyEnsembleClassifier**.

We will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Resources
- Data Source: LoanStats_2019Q1.csv
- Software: Python 3.7.9, Anaconda Navigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3

## Results (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports)

### Deliverable1

#### RandomOverSampler model

  ![D1-1.PNG](https://github.com/Praveeja-Sasidharan-Suni/Credit_Risk_Analysis/blob/main/Images/D1-1.PNG?raw=true)

#### SMOTE model

![D1-2.PNG](https://github.com/Praveeja-Sasidharan-Suni/Credit_Risk_Analysis/blob/main/Images/D1-2.PNG?raw=true)

#### ClusterCentroids model

![D1-3.PNG](https://github.com/Praveeja-Sasidharan-Suni/Credit_Risk_Analysis/blob/main/Images/D1-3.PNG?raw=true)

### Deliverable2

#### SMOTEENN model 
![combined.PNG](https://github.com/Praveeja-Sasidharan-Suni/Credit_Risk_Analysis/blob/main/Images/combined.PNG?raw=true)

### Deliverable3

#### BalancedRandomForestClassifier model
![D3-1.PNG](https://github.com/Praveeja-Sasidharan-Suni/Credit_Risk_Analysis/blob/main/Images/D3-1.PNG?raw=true)

#### The features are sorted in descending order.
![sorted.PNG](https://github.com/Praveeja-Sasidharan-Suni/Credit_Risk_Analysis/blob/main/Images/sorted.PNG?raw=true)

#### EasyEnsembleClassifier model
![d3-2.PNG](https://github.com/Praveeja-Sasidharan-Suni/Credit_Risk_Analysis/blob/main/Images/d3-2.PNG?raw=true)

## Summary
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.\
The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.\
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely 
detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.\
For all models, utlizing **EasyEnsembleClassifier** is the most effective. Provides a highest Score for all Risk loans.
The precision is low or none for all the models. In General, above the 90% of the current analysis, utlizing **EasyEnsembleClassifier** will perform a High-Risk loan precision as a great value for the overall analysis. 
 
