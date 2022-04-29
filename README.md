# Credit_Risk_Analysis
## Overview of the analysis
The purpose of this project was to evaluate three machine learning models by using resampling to determine which is better at predicting credit risk. First,  the oversampling RandomOverSampler and SMOTE algorithms were used, and then the undersampling ClusterCentroids algorithm was used. Using  these algorithms, the dataset was resampled, the count of the target classes was viewed,  a logistic regression classifier was trained, the balanced accuracy score was calculated, a confusion matrix was generated, and  a classification report was created. 

## Results
### Resampling Models

### Naive RandomOverSampler model

![image](https://user-images.githubusercontent.com/96098938/165844795-564115a8-0a01-40bf-aa3d-eaeb21ca98e1.png)
![image](https://user-images.githubusercontent.com/96098938/165844864-e62238f8-f8a4-4750-80cb-29353629a741.png)
* The balanced accuracy score of this model is 64%.
* The high_risk precision is about 1% only with 60% sensitivity which makes a F1 of 2%. 
* Precision is almost 100% with a sensitivity of 68%.

### SMOTE oversampling model

![image](https://user-images.githubusercontent.com/96098938/165845334-88bcd049-3388-48dc-868c-7ed26d2b2537.png)
![image](https://user-images.githubusercontent.com/96098938/165845401-d2e06672-9900-4d8d-95fc-83ee487cd2e0.png)

* The balanced accuracy score of this model  is 64%.
* The high_risk precision is about 1% only with 60% sensitivity which makes a F1 of 2%. 
* Precision is almost 100% with a sensitivity of 68%.


### Undersampling model

![image](https://user-images.githubusercontent.com/96098938/165845564-5a14c69f-ae1d-4227-bb93-1766d9286e84.png)
![image](https://user-images.githubusercontent.com/96098938/165845620-1fa6e6a7-3178-4c0f-a7b4-ca18926a6ad3.png)

* The balanced accuracy score of this model  is down to about 53%.
* The high_risk precision is still 1%  with 61% sensitivity which makes a F1 of 1%. 
* The model has a high number of false positives (9,426), the low_risk sensitivity is only 45%.


### Combination model (over and undersampling)

![image](https://user-images.githubusercontent.com/96098938/165845686-697f60a3-8d36-4a7c-b79d-a1f8049d9627.png)
![image](https://user-images.githubusercontent.com/96098938/165845736-6ad795df-0ea8-4af3-948f-f6e2535d8dcc.png)

The balanced accuracy score is about 62%.
The high_risk precision is still 1% only with 70% sensitivity which makes a F1 of only  about 2%.
Due to the high number of false positives, the low_risk sensitivity is only 55%.


### Balanced Random Forest Classifier

![image](https://user-images.githubusercontent.com/96098938/165878869-6c17822c-29a8-49d9-9691-adc443a469d3.png)
![image](https://user-images.githubusercontent.com/96098938/165878979-0a93d5b8-90ff-4f54-98eb-3c67c739c546.png)

* The balanced accuracy score is about 79%.
* The high_risk precision is  4% with only 67% sensitivity which makes a F1 equal to 7%.
* The low_risk sensitivity is 91% with 100% presicion because of  a lower number of false positives, 


### Easy Ensemble AdaBoost Classifier

![image](https://user-images.githubusercontent.com/96098938/165879029-ff4e7dda-711d-45dc-ac75-63f5e4768f87.png)
![image](https://user-images.githubusercontent.com/96098938/165879063-406b1f44-399e-45a5-aecc-c5477631ca70.png)

* The balanced accuracy score is high, about 93%.
* The high_risk precision is  low at 7% only with 91% sensitivity which makes a F1 of 14%.
* Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.

## Summary

The focus of this project was to identify a model that could correctly predict high-risk credits. After the analysis, it is evident that all models show weak ability to identify high-risk credits. Two ensemble models, Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier, shown high_risk precision scores  of 4% and 7% respectively, which is better than 1% high_risk precision scores of resampling models. Ensemble AdaBoost Classifier is able to identify 91% of possibly high risk credit applications; however, the precision score is low at 7% with high amount of false positives, which would erroneously mark low-risk credits as high risk. After the review, none of the models explored seem to be able to identify high-risk credits with acceptable level of precision and it is advised that alternative models need to be explored. 
