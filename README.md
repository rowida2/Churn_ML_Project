# Churn_ML_Project
## Bank Customer Churn Prediction

Predicting which bank customers will leave (Exited = 1), with EDA and a comparison of classic ML models.

## Dataset
File: Churn_Modeling.csv
Size: 10,000 customers, 14 columns, no missing values
Target: Exited (about 20% churn, so the classes are imbalanced)
Dropped: RowNumber, CustomerId, Surname (identifiers, no predictive value)

## What's Inside
Section	Topics
EDA	Distributions, churn by feature, correlations
Loss Functions	Cross-Entropy
Gradient Descent	Batch, Mini-batch and SGD, built from scratch
Models	Logistic Regression, KNN, SVM, Decision Tree, Naive Bayes

## Results (test set)
Model	ROC-AUC	Recall	F1

SVM (RBF)	0.853	0.74	0.58
Decision Tree	0.838	0.76	0.58
KNN	0.811	0.18	0.30
Logistic Regression	0.777	0.70	0.50
Naive Bayes	0.746	0.06	0.11
## Key Takeaways
Age, NumOfProducts, IsActiveMember and Geography (Germany) matter most for churn.
Non-linear models beat linear ones, because the relationships aren't linear.
Accuracy is misleading here (always predicting "stay" already gives about 80%), so Recall, F1 and AUC are used instead.
Scaling is essential for KNN, SVM, PCA, K-Means and gradient-based models.
