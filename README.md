# Credit Risk Analysis: Module 17 Challenge

## Overview of Project

### Background and Purpose

Fast Lending, a peer-to-peer lending services company, wants to use machine learning to predict credit risk. Management believes that this will provide a quicker and more reliable loan experience. It also believes that machine learning will lead to a more accurate identification of good candidates for loans, which will lead to low default rates. The company wants you to assist the lead data scientist to implement this plan. In your role, you will build and evaluate several machine learning models or algorithms, to predict credit risk. You will use techniques such as re-sampling and boosting, to make the most of your models and your data. Once you've designed and implemented these algorithms, you'll evaluate their performance and see how well your models predict data. To accomplish this task, you will dive headlong into machine learning algorithms, statistics, and data-processing techniques.

### Resources

- Data Sources: LoanStats_2019Q1.csv
- Software: Anaconda 4.13, Jupyter Notebook, Python 3.7.13, Visual Studio Code 1.68.1

## Results

### Machine Learning Models

In order to best predict credit risk, the following machine learning models were tested:

1. Naive Random Oversampling
2. SMOTE (Synthetic Minority Oversampling Technique) Oversampling
3. Cluster Centroids Undersampling
4. SMOTEENN (Synthetic Minority Oversampling Technique and Edit Nearest Neighbor) Combination (Over and Under) Sampling
5. Balanced Random Forest Classifier
6. Easy Ensemble AdaBoost Classifier

#### Naive Random Oversampling

*Figure 1: Naive Random Oversampling*

![NaiveRandomOversampling](https://user-images.githubusercontent.com/106830513/194416034-9a3915f7-1331-408a-bafd-6e393e7e6353.png)

+ Balanced Accuracy Score: 0.6504008094916134
    - This score shows that the model accurately predicted a person's credit risk (low or high) about 65% of the time.
+ High Risk Precision Score: 0.01; Low Risk Precision Score: 1.00
    - These scores indicate that the model is much more reliable at predicting low risk applications vs high risk applications.
+ High Risk Recall Score: 0.68; Low Risk Recall Score: 0.62
    - These scores indicate that the model's ability to find all the positive samples is 68% for high risk applications and 62% for low risk applications.

#### SMOTE Oversampling

*Figure 2: SMOTE Oversampling*

![SMOTEOversampling](https://user-images.githubusercontent.com/106830513/194416049-3d0e171b-0c06-4299-861b-dfc1c59c3bb3.png)

+ Balanced Accuracy Score: 0.6583599806425919
    - This score shows that the model accurately predicted a person's credit risk (low or high) about 66% of the time.
+ High Risk Precision Score: 0.01; Low Risk Precision Score: 1.00
    - These scores indicate that the model is much more reliable at predicting low risk applications vs high risk applications.
+ High Risk Recall Score: 0.63; Low Risk Recall Score: 0.68
    - These scores indicate that the model's ability to find all the positive samples is 63% for high risk applications and 68% for low risk applications.

#### Cluster Centroids Undersampling

*Figure 3: Cluster Centroids Undersampling*

![ClusterCentroidsUndersampling](https://user-images.githubusercontent.com/106830513/194416019-8bcf868b-e7fd-4d53-8fce-cdb049022c63.png)

+ Balanced Accuracy Score: 0.5447339051023905
    - This score shows that the model accurately predicted a person's credit risk (low or high) about 54% of the time.
+ High Risk Precision Score: 0.01; Low Risk Precision Score: 1.00
    - These scores indicate that the model is much more reliable at predicting low risk applications vs high risk applications.
+ High Risk Recall Score: 0.69; Low Risk Recall Score: 0.40
    - These scores indicate that the model's ability to find all the positive samples is 69% for high risk applications and 40% for low risk applications.

#### SMOTEENN Combination Sampling

*Figure 4: SMOTEENN Combination Sampling*

![SMOTEENNCombinationSampling](https://user-images.githubusercontent.com/106830513/194416044-2a04961b-dd70-4668-867e-a798468feb11.png)

+ Balanced Accuracy Score: 0.6449163069955265
    - This score shows that the model accurately predicted a person's credit risk (low or high) about 65% of the time.
+ High Risk Precision Score: 0.01; Low Risk Precision Score: 1.00
    - These scores indicate that the model is much more reliable at predicting low risk applications vs high risk applications.
+ High Risk Recall Score: 0.72; Low Risk Recall Score: 0.57
    - These scores indicate that the model's ability to find all the positive samples is 72% for high risk applications and 57% for low risk applications.

#### Balanced Random Forest Classifier

*Figure 5: Balanced Random Forest Classifier*

![BalancedRandomForestClassifier](https://user-images.githubusercontent.com/106830513/194416014-8a7ebd65-074e-4f52-93c2-45f57f01d20e.png)

+ Balanced Accuracy Score: 0.7885466545953005
    - This score shows that the model accurately predicted a person's credit risk (low or high) about 79% of the time.
+ High Risk Precision Score: 0.03; Low Risk Precision Score: 1.00
    - These scores indicate that the model is much more reliable at predicting low risk applications vs high risk applications.
+ High Risk Recall Score: 0.70; Low Risk Recall Score: 0.87
    - These scores indicate that the model's ability to find all the positive samples is 70% for high risk applications and 87% for low risk applications.

#### Easy Ensemble AdaBoost Classifier

*Figure 6: Easy Ensemble AdaBoost Classifier*

![EasyEnsembleAdaBoostClassifier](https://user-images.githubusercontent.com/106830513/194416023-03ac4ce2-6d00-4a55-8b33-f6c95738259c.png)

+ Balanced Accuracy Score: 0.9316600714093861
    - This score shows that the model accurately predicted a person's credit risk (low or high) about 93% of the time.
+ High Risk Precision Score: 0.09; Low Risk Precision Score: 1.00
    - These scores indicate that the model is much more reliable at predicting low risk applications vs high risk applications.
+ High Risk Recall Score: 0.92; Low Risk Recall Score: 0.94
    - These scores indicate that the model's ability to find all the positive samples is 92% for high risk applications and 94% for low risk applications.

## Summary

### High-Level Summary

All six models had varying balanced accuracy scores, with the Easy Ensemble AdaBoost Classifier model having the highest accuracy. The Easy Ensemble AdaBoost Classifier model also had the highest recall scores. However, while the precision scores for predicting low risk applications were very high across all six machine learning models tested, they were very low for predicting high risk applications - all less than 10%. A low precision score is indicative of a large number of false positives. This means that all six models were not accurately predicting high credit risk, and that some low risk applications were being falsely marked high risk.

### Model Recommendation

Out of all of the machine learning models, the Easy Ensemble AdaBoost Classifier model performed the best, with the highest accuracy, recall, and precision scores. Unfortunately, the Easy Ensemble AdaBoost Classifier model's precision score was still very low, at only 9% for predicting high risk applications. It is important for a lending company to predict a high risk application correctly. Based on these reasons, none of these machine learning models are recommended to use. The Easy Ensemble AdaBoost Classifier model is a good start, but may need more data, more cleaning, or another model parameter to improve its scores.
