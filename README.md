# Credit Risk Analysis

## Overview:

The purpose of this loan prediction risk analysis is to develop machine learning model to predict credit risk for a company called LendingClub, a peer-to-peer lending services company. The machine learning will provide a quicker and more reliable loan experience to the customers. And also to provide a more accurate identification of good candidates for loans. The main objective of this analysis is therefore; first build machine learning model designed to predict credit risk. Once we developed the model, we will evaluated the performance to see how well the model predict the data. Since credit risk inherently has an unbalalnced classification, we will also utilize different techniques to train and evaluate models with unbalanced classes . 

## Resources
* Software: Python 3.9.15, Anaconda Navigator 2.3.2, Conda 23.1.0, Jupyter Notebook 6.5.2

## Result:

1. Oversampling

The result shown below indicates precision for the low-risk is very high however the the presision for high-risk is very low. The recall rate for high rcredit risk is 69% which is low recall rate. A low recall is an indicative of large number of false negative predicted to be low risk were actually high risk.
The accuracy of this model is 0.644.

![Oversampling](https://github.com/abraham-22/Credit_Risk_Analysis/blob/main/png/Oversampling.png)

2. SMET

As it can be seen below, the metrics of the low-risk (precision, recall, and F1 score) are slightly improved over those of random oversampling. However, the metrics for the high risk didn't show an improvement. The accuracy which is the weighted avaerage of the true positives of this model is 0.662 which is better compared to the Oversampling .

![SMOTE](https://github.com/abraham-22/Credit_Risk_Analysis/blob/main/png/SMOTE.png)

3. Undersampling

Overall, we didn't see a significant improvement of the metrics in undersampling compared to the above two resampling. The recall rate for high-risk 0.69 improved compared to undersampling which was 0.63. The recall for the low-risk showed a big drop to 0.40. This indicates the model predicted the true positive low-credit risk as false negative. The weighted average for the TP also didn't show an improvement 0.662. 

![Undersampling](https://github.com/abraham-22/Credit_Risk_Analysis/blob/main/png/Undersampling.png)

4. Combination

From the classification report shown below, some of the metrics show an improvement over undersampling. The recall for the high-rsik improved from 0.69 to 0.72 and also the recall for the low-risk showed slight improvement from 0.40 to 0.57. However, the accuracy score didn't show any improvement. It went down from 0.662 to 0.544. 

![Combination](https://github.com/abraham-22/Credit_Risk_Analysis/blob/main/png/Combination.png)

5. Ensemble Learners: Balanced Random Forest Classifier

Here the metrics (precision, recall, and F1 score) of the low-risk are significantly improved over those of random oversampling and undersampling techniques. The recall for the high-credit risk dropped slightly to from 0.72 to 0.70. The balanced accuracy score showed a significant improvement in this model with a score of 0.87. 

![Ensemble](https://github.com/abraham-22/Credit_Risk_Analysis/blob/main/png/balanced_ensemble.png)

6. Ensemble Learners:AdaBoost Classifier

As it can be seen below, the metrics of low-risk and high risk improved significantly over Balanced Random Forest Classifier. The recall for high-risk increased from 0.70 to 0.92. The recall for low-risk also showed a bigger jump from 0.87 to 0.94. A high recall rate indicates a small number of high credit risk false negative.  
This will provide a more accurate identification of candidates who are not good for the loan.

![Ensemble](https://github.com/abraham-22/Credit_Risk_Analysis/blob/main/png/adaboost_ensemble.png)

## Summary:

In conclusion, after reviewing all six models, the EasyEnsembleClassifer model yielded the best results with an accuracy rate of 94.2% . The recall rate for high credit risk was also the highest at 92% compared to the other models. The result for predicting "Low Risk" was also the highest with the recall rate at 94%. A higher recall rate is an indicative of small number of false negative. 

Therefore, based on the performance of the model, I would recommended a machine learning algorithm using EasyEnsembleClassifier to perform credict risk analysis to predict credit risk. 

