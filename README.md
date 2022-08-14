# Credit Risk Analysis

## Overview

The purpose of this analysis is to apply machine learning to solve a real-world challenge: credit card risk. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. For this challenge, we will be employing different techniques to train and evaluate models with unbalanced classes. Specifically, we will be using imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, we used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Lastly, we evaluated the performance of these models and determined whether they should be used to predict credit risk.

## Results

### I. Naive Random Oversampling

The first model we used was Naive Random Oversampling. The results of our analysis can be seen below. In terms of the accuracy score, this model resulted in an accuracy score of roughly 0.67 meaning it was successful in accurately predicting about 67% of credit risks. 

<img width="379" alt="Screen Shot 2022-08-14 at 2 57 52 PM" src="https://user-images.githubusercontent.com/101564349/184551068-0b93f1fe-3a3b-4318-8701-e2f24452a7be.png">

When reviewing the classification report produced for this model, we see that the average F score falls at 0.76 with the high risk F score yielding only .02.

<img width="592" alt="Screen Shot 2022-08-14 at 3 00 01 PM" src="https://user-images.githubusercontent.com/101564349/184551123-13a85d8a-e84e-42d2-95eb-a164c15bf41f.png">

### II. Smote Oversampling

The next model we used was Smote Oversampling. The results of our analysis can be seen below. In terms of the accuracy score, this model resulted in an accuracy score of roughly 0.66 meaning it was successful in accurately predicting about 66% of credit risks.

<img width="308" alt="Screen Shot 2022-08-14 at 3 04 06 PM" src="https://user-images.githubusercontent.com/101564349/184551222-09d0d8ad-ff02-437d-a99f-e6e49987fafb.png">

When reviewing the classification report produced for this model, we see that the average F score falls at 0.80 with the high risk F score yielding only .02.

<img width="593" alt="Screen Shot 2022-08-14 at 3 04 46 PM" src="https://user-images.githubusercontent.com/101564349/184551232-365ccb3f-fad1-4b65-8b2e-74ce10bd549e.png">

### III. Cluster Centroids Undersampling

The next model we used was Cluster Centroids Undersampling. The results of our analysis can be seen below. In terms of the accuracy score, this model resulted in an accuracy score of roughly 0.54 meaning it was successful in accurately predicting about 54% of credit risks.

<img width="302" alt="Screen Shot 2022-08-14 at 3 05 31 PM" src="https://user-images.githubusercontent.com/101564349/184551256-15cc0470-d15f-4f25-9cc1-15e396cbe44c.png">

When reviewing the classification report produced for this model, we see that the average F score falls at 0.57 with the high risk F score yielding only .01.

<img width="599" alt="Screen Shot 2022-08-14 at 3 06 26 PM" src="https://user-images.githubusercontent.com/101564349/184551275-4a1d4727-87aa-4c08-9801-e4543bdf2304.png">

### IV. Combination Sampling

The next model we used was Combination Sampling. The results of our analysis can be seen below. In terms of the accuracy score, this model resulted in an accuracy score of roughly 0.65 meaning it was successful in accurately predicting about 65% of credit risks.

<img width="306" alt="Screen Shot 2022-08-14 at 3 07 18 PM" src="https://user-images.githubusercontent.com/101564349/184551300-7d8c4a78-596d-454f-aee0-793860651426.png">

When reviewing the classification report produced for this model, we see that the average F score falls at 0.72 with the high risk F score yielding only .02.

<img width="591" alt="Screen Shot 2022-08-14 at 3 07 56 PM" src="https://user-images.githubusercontent.com/101564349/184551315-86dd7a61-83e1-43c2-aed1-0983737b58fa.png">

### V. Balanced Random Forest Classifier

The next model we used was Balanced Random Forest Classifier. The results of our analysis can be seen below. In terms of the accuracy score, this model resulted in an accuracy score of roughly 0.76 meaning it was successful in accurately predicting about 76% of credit risks.

<img width="301" alt="Screen Shot 2022-08-14 at 3 09 07 PM" src="https://user-images.githubusercontent.com/101564349/184551340-3fb89567-3192-4295-93be-9bde1a293561.png">

When reviewing the classification report produced for this model, we see that the average F score falls at 0.92 with the high risk F score yielding .06.

<img width="597" alt="Screen Shot 2022-08-14 at 3 09 34 PM" src="https://user-images.githubusercontent.com/101564349/184551356-5acf56e8-1dff-4ecf-ac67-5d435762dbe8.png">

### VI. Easy Ensemble AdaBoost Classifier

The last model we used was Easy Ensemble Adaboost Classifier. The results of our analysis can be seen below. In terms of the accuracy score, this model resulted in an accuracy score of roughly 0.93 meaning it was successful in accurately predicting about 93% of credit risks.

<img width="303" alt="Screen Shot 2022-08-14 at 3 10 27 PM" src="https://user-images.githubusercontent.com/101564349/184551383-83c941cd-5148-4a93-9966-d3909a7181ac.png">

When reviewing the classification report produced for this model, we see that the average F score falls at 0.97 with the high risk F score yielding .16.

<img width="591" alt="Screen Shot 2022-08-14 at 3 10 57 PM" src="https://user-images.githubusercontent.com/101564349/184551396-fb87f783-7244-471d-bf49-711d1bc9d217.png">

## Summary

In summary, the model that yielded the best results was the Easy Ensemble AdaBoost Classifier. The analysis resulted in the highest accuracy score, average F score, and high-risk F score. Out of all the models used in this analysis, I would recommend the Easy Ensemble AdaBoost Classifier. However, I do believe predicting credit risks deserves an algorithm that results in better values, specifically the high risk prediction F score. 
