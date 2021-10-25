# Credit_Risk_Analysis
Machine Learning
## Overview
Purpose is to create a model for Machine Learning to predict credit risk based off a very imbalanced dataset with "low-risk" of 51,366 points and "high-risk" at only 246. To effectively seperate the data into test and training sets oversampling, undersampling and ensemble models have to be applied. Then after LogisticRegression model is fitted to the modified test sets the accuracy, precision and recall scores are compared to give a reccomenedation of which Machine Learning Model was most effiicient for a bank to determine credit risk.
### Resources
  #### Data
  - Lending Club [loan stats data](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/LoanStats_2019Q1.csv)
  
  #### Tools
  - Jupyter Notebook
  - mlenv

## Results
### Oversampling using RandomOverSampler  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/1_Acc_sc_Random_OversSampling.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/1_cm_Random_OverrSampling.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/1_classif_report_OverSampling.png)  
- Accuracy Score: 66.63%
- Precision of High-Risk: 1%
- Sensitivity of High-Risk: 70%
- Precision of Low-Risk: 100%
- Sensitivity of Low-Risk: 63%

### Oversampling using SMOTE  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/2_Acc_sc_SMOTE_OverSampling.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/2_cm_SMOTE_OverSampling.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/2_classif_report_SMOTE_OverSampling.png)  
- Accuracy Score: 66.23%
- Precision of High-Risk: 1%
- Sensitivity of High-Risk: 63%
- Precision of Low-Risk: 100%
- Sensitivity of Low-Risk: 69%

### Undersampling using ClusterCentroids  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/3_Acc_sc_UnderSampling.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/3_cm_UnderSampling.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/3_classif_report_UnderSampling.png)  
- Accuracy Score: 54.47%
- Precision of High-Risk: 1%
- Sensitivity of High-Risk: 69%
- Precision of Low-Risk: 100%
- Sensitivity of Low-Risk: 40%

### Over and Under Sampling using SMOTEENN  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/4_Acc_sc_Comb.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/4_cm_Combo.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/4_classif_report_Combo.png)  
- Accuracy Score: 54.47%
- Precision of High-Risk: 1%
- Sensitivity of High-Risk: 69%
- Precision of Low-Risk: 100%
- Sensitivity of Low-Risk: 40%%

### Ensemble Learner using BalancedRandomForestClassifier  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/5_Acc_sc_Bal_random_Forest.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/5_cm_Bal_random_Forest.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/5_classif_report_Bal_random_Forest.png)  
- Accuracy Score: 79.6%
- Precision of High-Risk: 4%
- Sensitivity of High-Risk: 68%
- Precision of Low-Risk: 100%
- Sensitivity of Low-Risk: 91%

### AdaBoost using EasyEnsembleClassifier  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/6_Acc_sc_AdaBoost.png)   
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/6_cm_AdaBoost.png)  
![img](https://github.com/LauraHaq/Credit_Risk_Analysis/blob/main/Images/6_classif_report_AdaBoost.png)  
- Accuracy Score: 92.54%
- Precision of High-Risk: 7%
- Sensitivity of High-Risk: 91%
- Precision of Low-Risk: 100%
- Sensitivity of Low-Risk: 94%

## Summary 
To determine how well the model predicts, the accuracy score of the six models shows Adaptive Boosting proves to be effective giving the highest Accuracy Score of 92.54%. The next closest accuracy Score was also an Ensemble Classifier of 79.6% using the Balanced Random Forest Classifier. All other models showed scores in the 50's and 60's by over- or undersampling without boosters. For this dataset Ensemble models with boosters proved to be effective in increaseing predictability. However, to recommend a model would be determine on what is the most beneficial for the company. All models produced 100% precision for Low-Risk. So, if the goal is to only ensure that all customers predicted "low-risk" are actually "low-risk" then all the models would be appropriate for use. If the goal is to ensure all possible customers are able to be receive business who are able eligible then none of the models are recommended as the best score for Sensititivity was 94% still showed a loss of over 900 eligible customers. I would base my reccomendation on the outcome requested between the two. 
