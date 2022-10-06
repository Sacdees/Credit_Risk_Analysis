# Credit_Risk_Analysis

## Analysis Overview
Credit Risk is difficult to predict, many time the Low Risk loans far out number the High Risk loans.  In this analysis we were tasked with helping predict whether applicants are to be considered low or high risk status.  Several methods can be used by data analysis to create a model to evaluate these applicants.  In this analysis we were tasked to use Imbalanced-learn and Scikit-learn functions to evaluate the sample data.  We will evaluate the performance of these function to determine a recommendation on predicting credit risk.

-----------------------

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
Here the balanced accuracy score is down to about 66%.<br>High Risk is 70 compared to 31<br>Resulting a similar prediction accuracy of 99%.
<br><br>

### Combination Sampling / SMOTEENN
<p align="center">
  <img src="Resouces\combo.png">
</p>
The balanced accuracy score is about 62%.<br>The high_risk precision is still 1% only with 68% sensitivity which makes a F1 of only 2%.<br>Due to the high number of false positives, the low_risk sensitivity is 57%.
<br><br>

-----------------------


### BalancedRandomForestClassifier model
<p align="center">
  <img src="Resouces\brfc.png">
</p>
The balanced accuracy score improved <br>High Risk Loans are still low<br> With a lower number of false positives the data is improved.
<br><br>

### EasyEnsembleClassifier model
<p align="center">
  <img src="Resouces\easy.png">
</p>
Data set has the highest balanced accuracy.<br>Also has a lower number of false positives compared to other techniques 
<br><br>
 
 ------------------------

## Summary
Overall the models perform along very similar lines. The major differences are attributed to which amount of precision and sensitivity is wanted when evaluations for loan applicants.  While some models have improvies sensitivity for high risk loans, other models have better potential of accurately determining which of these loans are high risk.  Keep in mind that whichever direction is chosen that in general most low risk applicant will largely out weigh the high risk applications.  Because these differnt models can not undoubtedly predict a candidate risk factor, I would not recommend these sampling initiatives.  