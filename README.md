# Credit_Risk_Analysis
Machine Learning

# Credit_Risk_Analysis

## Analysis Overview
Credit Risk is difficult to predict, many time the Low Risk loans far out number the High Risk loans.  In this analysis we were tasked with helping predict whether applicants are to be considered low or high risk status.  Several methods can be used by data analysis to create a model to evaluate these applicants.  In this analysis we were tasked to use Imbalanced-learn and Scikit-learn functions to evaluate the sample data.  We will evaluate the performance of these function to determine a recommendation on predicting credit risk.

## Results (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports)

### Naive Random Ovesampling
<p align="center">
  <img src="Resouces\naive_random.png">
</p>
The balanced accuracy score is 64%.<br>Predicted High Risk is 70 where Low Risk is 31<br>With the low risk population out performing the high risk, the predictions accuracy is nearly 99%.
<br><br>

### SMOTE model
<p align="center">
  <img src="Resouces\smote_oversample.png">
</p>
The results are almost mirror of our first data set.<br>The balanced accuracy score is 66%.<br>High Risk is 64 compared to 37<br>Resulting a similar prediction accuracy of 99%.
<br><br>

### Undersampling
<p align="center">
  <img src="Resouces\undersample.png">
</p>
Here the balanced accuracy score is down to about 52%.<br>The high_risk precision is still 1% only with 63% sensitivity which makes a F1 of 1%.<br>Due to the high number of false positives, the low_risk sensitivity is only 40%.
<br><br>

### SMOTEENN model
<p align="center">
  <img src="">
</p>
The balanced accuracy score is about 62%.<br>The high_risk precision is still 1% only with 68% sensitivity which makes a F1 of only 2%.<br>Due to the high number of false positives, the low_risk sensitivity is 57%.
<br><br>

### BalancedRandomForestClassifier model
<p align="center">
  <img src="">
</p>
The balanced accuracy score improved to about 79%.<br>The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.<br>Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.
<br><br>

### EasyEnsembleClassifier model
<p align="center">
  <img src="">
</p>
Now, the balanced accuracy score is high to about 93%.<br>The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.<br>Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.
<br><br>

## Summary
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.\
The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.\
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.\
For those reasons I would not recommend the bank to use any of these models to predict credit risk.