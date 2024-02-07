# credit-risk-classification
credit-risk-classification

# Credit Risk Classification: Analysis 

## Process Overview

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* The purpose of this anaylsis is to build a machine learning model which groups potential customers by their risk of default and to evaluate the reliability of the model created.  
* Using the dataset of past financial history provided by the lender, I built a logistic regression model to classify borrowers as high risk of default or low risk of default.  
* Evaluation of the initial model resulted in a balanced accuracy of 95%. However, reduced accuracy and recall of high-risk clients demonstrated that the model is better at identifying low risk loans than high risk loans. Examination of the data showed that this is due to an unbalanced data set, with low-risk entries greatly outweighing high-risk 
* To correct this, I balanced the data fed to the model using OverSample, which ensured there were an equal number of high and low risk loans, and produced a confusion matrix and classification report to compare models and determine which, if any, I would suggest to the lender. 
* 

## Results

* Machine Learning Model 1 (Unabalanced Data):
  
                  precision    recall      balanced accuracy  
   Low Risk       1.00       0.99     
   High Risk       0.85      0.91
                                           0.95 



* Machine Learning Model 2 (Balanced Data):
                    precision    recall     balanced accuracy 

    Low Risk       1.00      0.99          
   High Risk       0.84      0.99    
                                            0.99 

## Summary

* Model 2 is the more accurate of the 2 models, as evidenced by the improved recall and overall balanced accuracy. Though the second model's precision of high risk loans is 1% lower than Model 1, this is outweighed by the better overall accuracy of the second model. 
* If I were to reccomend one of these models, I would reccomend number two. The confusion matrix for model 2 shows that the model is particularly prone to false positives: 


False Positives:  102  Loan is low risk and predicted as high-risk
False Negatives: 56 Loan is high risk and prediected as low-risk  

However, False Negatives are the higher risk category for a lender: missing out on a potential client because they are identified as high risk when they are not is less costly than mistakenly aprroving a loan that has a high probability of default. So though the accuracy precision for high risk is limited, it poses limited risk for the client. 
