# Credit_Risk_Analysis

## Overview

The purpose of this analysis is to be able to predict credit risk by comparing six different machine learning models and determining which one is most accurate in making this prediction. An existing credit risk dataset will be used to train and test the models and the output of each model will be used to compare them all.

## Results
* Naive Random Oversampling
  * Balanced accuracy: 0.65
  * High-risk Precision: 0.01
  * High-risk Recall: 0.72
  * The random oversampling model produces true high-risk and true low risk results 65% of the time. Additionally, out of all high-risk loan predictions, only 1% of them are actually high-risk. Lastly, of all the high and low risk predictions, 72% of them are correct.

<img width="786" alt="Oversampling" src="https://user-images.githubusercontent.com/88349443/146711784-8c8238c0-6bfb-477a-a761-7635a1c011ac.png">

* SMOTE Oversampling
  * Balanced accuracy: 0.66
  * High-risk Precision: 0.01
  * High-risk Recall: 0.63
  * The SMOTE oversampling model produces true high-risk and true low risk results 66% of the time. Additionally, out of all high-risk loan predictions, only 1% of them are actually high-risk. Lastly, of all the high and low risk predictions, 63% of them are correct. This model is slightly better at accurately predicting the risk of the loan, but the recall of high-risk loans is worse compared to the random oversampling model.

<img width="777" alt="SMOTE Oversampling" src="https://user-images.githubusercontent.com/88349443/146711806-c65b0617-d4b0-45ac-8e38-bc092bedf44e.png">

* Undersampling
  * Balanced accuracy: 0.54
  * High-risk Precision: 0.01
  * High-risk Recall: 0.69
  * The undersampling model produces true high-risk and true low risk results just 54% of the time. Additionally, out of all high-risk loan predictions, only 1% of them are actually high-risk. Lastly, of all the high and low risk predictions, 69% of them are correct. This model is much worse at accurately predicting the risk of the loan, but the recall of high-risk loans is slightly better compared to both the random oversampling and SMOTE oversampling model.

<img width="782" alt="Undersampling" src="https://user-images.githubusercontent.com/88349443/146711825-1513f303-4a01-45cf-a94c-622aa8a1402a.png">

* Combination (Over and Under) Sampling
  * Balanced accuracy: 0.65
  *	High-risk Precision: 0.01
  * High-risk Recall: 0.72
  * The combination model produces true high-risk and true low risk results 65% of the time. Additionally, out of all high-risk loan predictions, only 1% of them are actually high-risk. Lastly, of all the high and low risk predictions, 72% of them are correct. The results of this model are almost identical to the naïve random oversampling model.

<img width="777" alt="Combination" src="https://user-images.githubusercontent.com/88349443/146711844-cdbc5934-be5d-477a-ac0e-eacc0f3c4fc3.png">

* Balanced Random Forest Classifier
  * Balanced accuracy: 0.79
  * High-risk Precision: 0.03
  * High-risk Recall: 0.70
  * The balanced random forest classifier model produces true high-risk and true low risk results 79% of the time. Additionally, out of all high-risk loan predictions, only 3% of them are actually high-risk. Lastly, of all the high and low risk predictions, 70% of them are correct. The results produced by this model are an improvement over the previous four models.
  
<img width="776" alt="BRFC" src="https://user-images.githubusercontent.com/88349443/146712312-e096941e-4d83-46d1-b53b-b536d580ec92.png">

* Easy Ensemble AdaBoost Classifier
  * Balanced accuracy: 0.93
  * High-risk Precision: 0.09
  * High-risk Recall: 0.92
  * The easy ensemble adaboost classifier model produces true high-risk and true low risk results an impressive 93% of the time. Additionally, out of all high-risk loan predictions, 9% of them are actually high-risk. Lastly, of all the high and low risk predictions, 92% of the loans are correct This model is much better at accurately predicting the risk of the loan, and both the precision and the recall of high-risk loans is better compared to all the other models.

<img width="784" alt="EEC" src="https://user-images.githubusercontent.com/88349443/146842904-b307ed4e-75f3-4537-8cd7-b5231151a9fb.png">

## Summary

The goal of using a machine learning model is to be able to take in information about a loan and accurately predict whether the loan is high-risk or low-risk. Since there are always much fewer high-risk loans than low-risk, there is a large discrepancy between the number of data points for each being fed into a model. Therefore, the high-risk prediction metrics for precision and recall were used to evaluate the models.

Out of these 6 machine learning models, the easy ensemble adaboost classifier model produced the best results. It is able to accurately determine whether a loan is high or low risk 93% of the time (the rest were in the 60 and 70 percent range). While still quite low, the recall of this model at 9% was much better than the rest (most were 1%, the next best was 3%). Lastly, out of the predictions that this model made, 92% of them were correct predictions. 

Even though the recall appears to be quite low at just 9%, it is OK that it is not perfect because using the model has greatly reduced the total number of loans that will need to be evaluated for potentially being high-risk. Since the other two metrics are quite high, I would recommend this model be used.
