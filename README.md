# Credit_Risk_Analysis

## Overview
The goal of this analysis is to assess a variety of machine learning models to decide whether they should be used to predict credit risk. All models were tested with the same sample loan data from Q1 of 2019 and set to the same random state. Because there are many more good loans than risky loans in the data, 4 different logistic regression models were used with different resampling algorithms, specifically a random naive oversampling, a Synthetic Minority Oversampling algorithm (SMOTE), a cluster centroids algorithm, and a SMOTE with Edited Nearest Neighbors (SMOTEENN) algorithm. In addition to the logistic regression models, two more models using ensemble methods, a balanced random forest classifier and an Adaboost classifier, were also tested.

## Results

Below are screenshots of accuracy scores, confusion matrices, and classification reports. For classifcation reports, relevant abbreviations are as follows: pre (precision) rec (recall/sensitivity) spe (specificity) and f1 (harmonic mean of pre and rec).

* ![Naive_Random_Oversampling.png](https://github.com/deklund76/Credit_Risk_Analysis/blob/main/resources/Naive_Random_Oversampling.png) _Naive Random Oversampling_
* ![SMOTE.png](https://github.com/deklund76/Credit_Risk_Analysis/blob/main/resources/SMOTE.png) _SMOTE_
* ![Undersampling.png](https://github.com/deklund76/Credit_Risk_Analysis/blob/main/resources/Undersampling.png) _Undersampling_
* ![SMOTEENN.png](https://github.com/deklund76/Credit_Risk_Analysis/blob/main/resources/SMOTEENN.png) _SMOTEENN_
* ![Random_Forest.png](https://github.com/deklund76/Credit_Risk_Analysis/blob/main/resources/Random_Forest.png) _Random Forest_
* ![AdaBoost.png](https://github.com/deklund76/Credit_Risk_Analysis/blob/main/resources/AdaBoost.png) _AdaBoost_

## Summary

Because a defaulted loan costs the lender the entire principle while a denied loan only costs the lender potential profit from interest, it is most important that a credit risk assessment model correctly identifies high risk loans. Among these models, those that implement some form of oversampling (Naive Random Oversample, SMOTE, and SMOTEENN) performed best in this regard as evidenced by their higher sensitivity scores with regard to high risk loans. Even so SMOTEENN led that group with only 72% sensitivity and an accuracy score of just 64%. Given these limitations, none of these models can be recommended as they would allow a far higher proportion of high risk loans through and deny many more low risk loans.
