# Credit_Risk_Analysis

**Project Overview**
The purpose of this project is to employ different techniques to train and evaluate models with unbalanced classes. With the credit dataset from LendingClub, several different algorithms are used to predict credit risk. The performance of these different models are compared, classified and recommendations are  based on the outcomes of the samples.

**Software**
Python 3.7
SciPy latest version as @ March 6th 2022
Scikit-learn version as @ March 6th 2022
imbalanced-learn version as @ March 6th 2022

**Results**
Below are the resampling models have been used in this project and their individual results.

**Oversampling: Native Random Oversampling**

In random oversampling, instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced.
Balanced Accurracy Score: 0.65
High-Risk Precision: 0.01
High-Risk Recall: 0.71
![1st Random Oversampling](https://user-images.githubusercontent.com/93059601/156943760-80cab878-53a0-4afe-8a2a-541b258465b4.PNG)


**Oversampling: SMOTE**
Synthetic Minority Oversampling Technique (SMOTE) is an oversampling approach to deal with unbalanced datasets.

Balanced Accurracy Score: 0.66
High-Risk Precision: 0.01
High-Risk Recall: 0.63
![SMOTE Oversampling](https://user-images.githubusercontent.com/93059601/156943874-4bc349ff-e4ca-4c6c-b040-89508332d985.PNG)


**Undersampling: Random Undersampling**
In random undersampling, instances are randomly selected from the majority class and removed until the size of the majority class is reduced (typically to the size of the minority class).

Balanced Accurracy Score: 0.66
High-Risk Precision: 0.01
High-Risk Recall: 0.63

![Random Undersampling](https://user-images.githubusercontent.com/93059601/156943914-288000eb-a08b-46c9-94ad-c7c620d50fc4.PNG)


**Combination Sampling: SMOTEENN**
SMOTEENN is combination of SMOTE and Edited Nearest Neighbor (ENN) algorithms. This involves a two step process:

**Oversample the minority class with SMOTE.**
Clean the resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.
Balanced Accurracy Score: 0.64
High-Risk Precision: 0.01
High-Risk Recall: 0.72

![SMOTEENN Sample](https://user-images.githubusercontent.com/93059601/156943972-d0d5ecd5-f36d-4a72-a551-d57fca6c79fa.PNG)

**Balanced Random Forest Classifier**
A Balanced Random Forest is an ensemble method that randomly under-samples to achieve balance.

Balanced Accurracy Score: 0.78
High-Risk Precision: 0.03
High-Risk Recall: 0.70

![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/93059601/156944046-c5009368-8528-4b41-88f7-2058fc64b668.PNG)


**Easy Ensemble AdaBoost Classifier**
Bag of balanced boosted learners also known as EasyEnsemble. The balancing is achieved by random under-sampling.

Balanced Accurracy Score: 0.93
High-Risk Precision: 0.09
High-Risk Recall: 0.92

![Easy Ensemble AdaBoost Classifier](https://user-images.githubusercontent.com/93059601/156944157-eb056ec2-c08c-4819-9f97-2ab3d7250fc4.PNG)

**Easy Ensemble AdaBoost Classifier** has the highest Balanced Accuracy Score out of all of the techniques in this project. EasyEnsemble also has the highest precision, recall, and F1 scores as proven by the imbalanced classification reports printed for each model throughout this deployment.

If one of the models in this project must be used to predict credit risk, it is recommended to use Easy Ensemble AdaBoost Classifier. EasyEnsemble model performed the best in this sampling, its precision for high-risk data points is still only 0.09. This shows that very few of positive predictions are true (False Positives). 

Author:Mark Okoli
For all questions and inquiries, please contact me on LinkedIn.
https://www.linkedin.com/in/mark-okoli-74380258/
