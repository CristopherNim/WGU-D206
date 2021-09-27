### NVM2 TASK 1: CLASSIFICATION ANALYSIS
# **Part I: Research Question**

## A.  Describe the purpose of this data mining report by doing the following:

.  Propose **one** question relevant to a real-world organizational situation that you will answer using **one** of the following classification methods:
- The telecommunications company is looking to identify which customers are more likely to churn. The company wants to increase its retention rate because it cost the company ten times more to acquire customers than to retain an existing customer. The company intends to use the data to build a model to predict what customers will churn. The model algorithm is going to be Naive Bayes. 

2.  Define **one** goal of the data analysis. Ensure that your goal is reasonable within the scope of the scenario and is represented in the available data.  
 - The goal of the data analysis is to predict the churn column at an 80 percent accuracy.
 

# **Part II: Method Justification**

## B.  Explain the reasons for your chosen classification method from part A1 by doing the following:
- The reason Naive Bayes algorithm was chosen that our numerical columns have a normal distribution. 

1.  Explain how the classification method you chose analyzes the selected data set. Include expected outcomes.
- Naive Bayes calculates the posterior probability for each class(Churn). The class with the highest posterior probability is the outcome of the prediction.
- The outcome I expect is that it would predict 20% customers churning and 80% staying with the company  
2.  Summarize **one** assumption of the chosen classification method.
- Assumption of independence among predictors. It assumes that a feature in a class is unrelated to the presence of another type. In real life, it almost impossible that we have a set of predictors that are entirely unrelated. If we get a set of independent predictors that are not related, the model accuracy should be high. 
3.  List the packages or libraries you have chosen for Python or R, and justify how _each_ item on the list supports the analysis.  
 - Numpy - Numpy contains statistical functions.
- pandas - create the data frame and allow data manipulation.
 - sklearn -  Contains the Naive Bayes algorithm function.
 - seaborn and matplotlib libraries will allow us to make visualizations. 



# **Part III: Data Preparation**

## C.  Perform data preparation for the chosen data set by doing the following:

Describe **one** data preprocessing goal relevant to the classification method from part A1.
- The columns with categorical values will be transformed into individuals columns with Pandas function get_dummies. one for yes and zero for no.
2.  Identify the initial data set variables that you will use to analyze the classification question from part A1, and classify _each_ variable as continuous or categorical.
- ![[Pasted image 20210527182853.png]]
- ![[Pasted image 20210527183020.png]]
3.  Explain _each_ of the steps used to prepare the data for the analysis. Identify the code segment for _each_ step.
- ![[Pasted image 20210527184602.png]]
- For the churn column the yes was replaced with 1 and no was replaced with 0.
- ![[Pasted image 20210527184741.png]]
- The categorical variables were divided by yes or no columns 
- ![[Pasted image 20210527184838.png]]
- ![[Pasted image 20210528162839.png]]
4.  Provide a copy of the cleaned data set.  
 ✅

# **Part IV: Analysis**

## D.  Perform the data analysis and report on the results by doing the following:

1.  Split the data into training and test data sets and provide the file(s).
- ![[Pasted image 20210528162855.png]]
2.  Describe the analysis technique you used to analyze the data appropriately. Include screenshots of the intermediate calculations you performed.
- ![[Pasted image 20210528163606.png]]
- ![[Pasted image 20210528163618.png]]
- ![[Pasted image 20210528163626.png]]
- The accuracy score is 89.6% accurate
- The model mislabeled 208 rows in the churn column based on the customer's information. 
- The model has a high true positive rate meaning it has high accuracy. 
3.  Provide the code used to perform the classification analysis from part D2.  
 ☑️

# **Part V: Data Summary and Implications**

## E.  Summarize your data analysis by doing the following:
1.  Explain the accuracy and the area under the curve (AUC) of your classification model.
- The model has an accuracy rate of 89.6%
- ![[Pasted image 20210528164245.png]]
- The model Area under the curve is 87%. Meaning that is labeling the correct label 87% of the time.
2.  Discuss the results and implications of your classification analysis.
- ![[Pasted image 20210528164645.png]]
- Out of 2000 rows, the model:
	- The model is labeling 111 false negatives (meaning the labeled should be 1=yes)
	- the model labeled 97 false positives (meaning the labeled should be 0=no)
	- labeled 1765 correct labels 
3.  Discuss **one** limitation of your data analysis.
 - The main limitation, as stated above, is that the Naive Bayes assumes independent predictors.  Tenure and Monthly charge some correlation. It is hard to find sets (columns) of data in actual-world data that do not correlate with the prediction column. 
 - Another limitation is that it assumes that all columns have a normal distribution. 
4.  Recommend a course of action for the real-world organizational situation from part A1 based on your results and implications discussed in part E2.  
 - My recommendation based on the model is that we should look for another model with a lower false-negative rate. Those are 111 customers that could be lost and cost the company to lose revenue. 

## H  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.
N/A