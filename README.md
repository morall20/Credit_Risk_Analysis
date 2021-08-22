# Credit Risk Analysis

![credit-risk-managment-training](https://user-images.githubusercontent.com/82338072/130371189-307fc294-6d09-42e1-a154-d2d53586ba3b.png)


## Overview of the Analysis

You've been asked to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once I'm done, I evaluated the performance of these models and made a written recommendation on whether they should be used to predict credit risk.

## Resources

- Software: Juypter Notebook, imbalaced-learn & scikit-learn libraries, Python
- Data: LoanStats_2019Q1.csv

## Results

### Credit Risk Resampling

***Naive Random Oversampling***

![NRO](https://user-images.githubusercontent.com/82338072/130370919-941cb297-bd20-4015-b8ec-5273f99f9b89.PNG)


- Balance accuracy score - 65%
- Precision scores <> high-risk 0.01 <> low-risk 1.00
- Recall scores <> high-risk 0.64 <> low-risk 0.65
- Avg/Total 99% for precision & 65% for recall


***SMOTE Oversampling***

![smote](https://user-images.githubusercontent.com/82338072/130370929-1b13bbec-475a-4597-9dde-214fb940d56e.PNG)


- Balance accuracy score - 66%
- Precision scores <> high-risk 0.01 <> low-risk 1.00
- Recall scores <> high-risk 0.67 <> low-risk 0.65
- Avg/Total 99% for precision & 65% for recall 


***Cluster Undersampling***

![cluster_Undersample](https://user-images.githubusercontent.com/82338072/130370949-0e700ace-e1af-41af-a698-1134ad4d1cab.PNG)


- Balance accuracy score - 51%
- Precision scores <> high-risk 0.01 <> low-risk 1.00
- Recall scores <> high-risk 0.57 <> low-risk 0.46
- Avg/Total 99% for precision & 46% for recall 



***SMOTEENN Combination Over & Under Sampling***

![smotteenn_combo_ over_under](https://user-images.githubusercontent.com/82338072/130370955-1369ac7c-7371-45cc-9506-b524fa92f645.PNG)


- Balance accuracy score - 51%
- Precision scores <> high-risk 0.01 <> low-risk 1.00
- Recall scores <> high-risk 0.70 <> low-risk 0.58
- Avg/Total 99% for precision & 58% for recall 



#### Credit Risk Ensemble
***Balanced Random Forest Classifier***

![credeit_risk_ensemble](https://user-images.githubusercontent.com/82338072/130370965-b02511b0-0971-4b22-b32f-572c02da6ac9.PNG)


- Balance accuracy score - 78%
- Precision scores <> high-risk 0.04 <> low-risk 1.00
- Recall scores <> high-risk 0.67 <> low-risk 0.91
- Macro avg 52% for precision & 79% for recall
- Weighted avg 99% for precision & 91% for recall 


***Easy Ensemble Ada Boost Classifier***

![easy_ensamble](https://user-images.githubusercontent.com/82338072/130370969-5c54ad42-bc9b-489f-ad1e-9dd6faa5ba90.PNG)


- Balance accuracy score - 93%
- Precision scores <> high-risk 0.07 <> low-risk 1.00
- Recall scores <> high-risk 0.91 <> low-risk 0.94
- Avg/Total 99% for precision & 94% for recall



## Summary

The results indicate that, in this case, the Easy AdaBoost Classifier is the most effective model with a 93% balance accuracy score test (model's performance). The average/total sensitivity is 94%. Sensitivity is more important than precision in order to detect fraudulent credit card risk results. False positives can be ruled out by contacting applicants directly to evaluate discrepancies. This model also shows that it is well balanced between sensitivity and precision, due to high yield F1 score (avg/total 97%).

For these reasons, I would recommend the use of this model in this case.



 
