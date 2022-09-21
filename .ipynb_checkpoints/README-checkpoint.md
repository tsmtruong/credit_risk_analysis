# Credit Risk Analysis

## Overview
In this project we used Python to build and evaluate several machine learning models to predict credit risk. To do so we used the following methodologies:
- oversample the data using RandomOverSampler and SMOTE
- undersampled the data using ClusterCentroids
- used a combined approach of over and under sampling using SMOTEENN
- compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier

## Results

### RandomOverSample

![accuracy](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/ros_accuracy.jpg)
![confusion matrix](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/ros_cm.jpg)
![report](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/ros_report.jpg)

- The balanced accuracy score is 65%
- The high_risk precision is only 1% with a sensitivity of 62%


### SMOTE 

![accuracy](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/smote_accuracy.jpg)
![confusion](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/smote_cm.jpg)
![report](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/smote_report.jpg)

- The results are pretty similar to the previous model
- The balanced accuarcy score is 64%
- The high_risk precision is about 1% only with 63% sensitivity
- The precision is almost 100% with a sensitivity of 66%


### ClusterCentroids

![accuracy](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/cc_accuracy.jpg)
![confusion](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/cc_cm.jpg)
![report](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/cc_report.jpg)

- The balanced accuracy score is lower at 52%
- High risk precision is still at 1% with 63% sensitivity
- Due to a high number of false positives, the low risk sensitivty is only 40%


### SMOTEENN
![accuracy](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/smoteenn_accuracy.jpg)
![confusion](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/smoteenn_cm.jpg)
![report](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/smoteenn_report.jpg)

- The balanced accuracy score is about 62%
- The high_risk precision is still only 1% only with 68% sensitivty
- Due to high number of false positives, the low_risk sensitivity is 57%


### BalancedRandomForestClassifier
![accuracy](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/balran_accuracy.jpg)
![confusion](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/balran_cm.jpg)
![report](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/balran_report.jpg)

- Accuracy score imporved to about 79%
- High risk precision chaged to about 4% with 67% sensitivity
- Due to a lower number of false positives, the low rish sensitivity is now 91%


### EasyEnsembleClassifier

![accuracy](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/easy_accuracy.jpg)
![confusion](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/easy_cm.jpg)
![report](https://github.com/tsmtruong/credit_risk_analysis/blob/main/Resources/easy_report.jpg)

- Now, the balanced accuracy score is high to about 93%.
- The high_risk precision is still low at 7% only with 91% sensitivity
- Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.


## Summary

All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.
For those reasons I would not recommend the bank to use any of these models to predict credit risk.