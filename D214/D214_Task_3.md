# **Executive Summary and Implications**

#### Question and hypothesis 
**Research Question:** Can a machine learning model be created statistically significantly to predict if a nursing home will be fined a ticket?

The feature we are trying to predict is whether the nursing home is in danger of getting fined. The dataset contains other features that will aid in the prediction of the predictable variable. Some of the columns that will aid in the predicted column are the nursing home rating, the size of the nursing home, how many beds each nursing home has, and the number of complaints each nursing home has. There is enough valuable information with the features to try to answer the research question.

**Null Hypothesis**-: The independent variable cannot statistically significantly predict if a nursing home will be fined a ticket. The null hypothesis states that there is not enough valuable information in the features that will aid in the prediction of the number of fines.

**Alternate Hypothesis**-: The independent variable can statistically significantly predict if a nursing home will be fined a ticket. The alternative hypothesis states there is enough information valuable information in the features to predict the number of fines accurately.

**Summary of the data analysis and findings** 
- The main disadvantage of using chi-square is that the random forest model sometimes produces biases towards categorical features. The main advantage is that it allows us to remove the features that do not aid in predicting the number of fine features.
- The first to test the dataset using the chi-square is to grab all the categorical columns. The code below grabs only the categorical features.                                          ![[Pasted image 20210922140514.png]]
- The code below tests a relationship between the number of fines and all the other categorical features.
![[Pasted image 20210922140712.png]]
- The accepted list has features that do have a relationship with the number of fines feature. The rejected list has a feature that does not have a relationship with a number of fines features. 
![[Pasted image 20210922141129.png]]
- The Chi-square test allowed us to reduce the number of features used to predict the feature.  We started with 89 columns, including the feature we are predicting. We then used the chi-square test to remove the categorical features that do not aid in the prediction. After removing the categorical columns that did not have a relationship, we were left with only 57 columns. The disadvantage is that accuracy lower by 1 percent in the sample after removing features using the chi-square. Is it worth removing the features when the data is easy to collect, or will it be collected regardless?
 - ![[Pasted image 20210922140149.png]]
 - The feature importance plots the most important feature at the top. The most important features tell us which feature has the most influence on the prediction overall. The top feature that aids in the prediction is the health survey score. The feature that least helps is 'most_recent_health_inspection_more_than_2_years_ago'. We could remove the column to help lower the feature if collecting this specific data is difficult. 
 - ![[Pasted image 20210922154057.png]]
 - The Random Forest model confusion matrix labeled 1852 labels correctly and mislabeled 518 correctly. If the model labeled the row correctly, then it guesses right if the nursing was fined a ticket or not. The disadvantage is that number of labels correctly and incorrectly change depending on the sample grab to test the data. 
 - The AUC  (Area under the curve) score is 71%. The Area under the curve represents the True positive vs. false positive rate. The higher the above the curve, the more accurate our model is, the higher above the curve it is. Our model has an average true positive rate.
 - ![[Pasted image 20210922142503.png]]
- The Random Forest model has an accuracy of 78%.
- ![[Pasted image 20210920191458.png]]


**limitations**
- The limitation of using a random forest model is that it creates a biased with categorical values, and if the dataset rows increase, the model will take longer to train. Furthermore, increasing the accuracy of the model will be difficult even after changing the hyperparameters. 
- The disadvantage, as stated before, of the confusion matrix is that if we used a different data sample, the results would not be reproducible. 
- Area Under Curve limitation -accuracy scores used to build ROC curves may be challenging to assign. Without the knowledge of AUC, the user will not understand the graph since it is not easy to understand/read the graph. 

**a summary of proposed actions**
- The model had an accuracy of 78%, which is 8% more than the goal. The recommended course of action is that each nursing home should collect accurate data on the essential features to help predict fines. Furthermore, nursing should improve the rating cycle scores to help decrease the chance of getting fined. If the other features are not essential, they should not be collected unless the state needs to help collect the other essential features. 
- We could try using a different machine learning model like Logistic Regression. Using another model would most likely have to remove the numeric outliers in each numeric feature. After removing the outliers in the numeric features, we could use the coefficients of logistic regression to further look into the classes of each feature that produce a fined in a nursing home.
- Furthermore, we could use different hyperparameters with a model to increase the accuracy.

**expected benefits of the study**
- After building the model, we went from 89 features to 57 features. They are allowing nursing homes to collect only data on only the most vital features. As well know what the most critical features determine the outcome if nursing gets fined or not. 
	- For example, A good health survey score means that the nursing home has less chance of getting fined a ticket. 
	- Another example is that recent health inspections from two years ago do not factor in the prediction.
- The model has a ~80% accuracy score, which will allow the nursing home to take preventive measures to avoid getting fined. 
	- after testing the model with 2370 rows, the model labeled correctly 1852 rows and labeled incorrectly 518.

# Sources
All code in this repository is available under the [MIT License](https://opensource.org/licenses/MIT). Files in the `output/` directory are available under the [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (CC BY 4.0) license.

CMS.Gov (2021 April 21). Retrieved July 14, 2021, from https://data.medicare.gov/data/nursing-home-compare, https://github.com/BuzzFeedNews/2020-04-cms-nursing-homes