
### NBM2 TASK 2: LOGISTIC REGRESSION FOR PREDICTIVE MODELING
# **Part I: Research Question**

## A.  Describe the purpose of this data analysis by doing the following:

1.  Summarize **one** research question that is relevant to a real-world organizational situation captured in the data set you have selected and that you will answer using logistic regression.
-  The telecommunications company is looking to identify which customers are more likely to churn. The company wants to increase its retention rate because it cost them ten times more to acquire customers than to retain an existing one.

2. Define the objectives or goals of the data analysis. Ensure that your objectives or goals are reasonable within the scope of the data dictionary and are represented in the available data.
- The analysis aims to make a model that can predict the churn at an 80 percent accuracy.  In addition, the team wants to know what features, when true, lead to the customer churning. 
  

# **Part II: Method Justification**

## B.  Describe logistic regression methods by doing the following:

1.  Summarize the assumptions of a logistic regression model.
- First, Binary logistic regression requires the dependent variables to be binary.
- The data observations need to be independent of each other. 
- The independent variables should not have a high correlation.
- The dataset needs to have more than ten rows.
- Little or no Multicollinearity among the independent variables.
2.  Describe the benefits of using the tool(s) you have chosen (i.e., Python, R, or both) in support of various phases of the analysis.
- The team has chosen python because it is the most used tool for data analysis. It can be combined with SQL if more records need to be used. 
3.  Explain why logistic regression is an appropriate technique to analyze the research question summarized in Part I.
- Logistic regression can predict binary columns. It is easy to implement coding-wise. Most importantly, logistic regression has a lower bias than Naive Bayes.
  

# **Part III: Data Preparation**

## C.  Summarize the data preparation process for logistic regression by doing the following:

1.  Describe your data preparation goals and the data manipulations used to achieve the goals.
- During the data exploration, the data analysis team ran a chi-square test and ANOVA test for feature extraction. The image below is the columns that are statistically significant to the churn column. Meaning that the columns are substantial, and we can be confident that they help predict the churn values
-  ![[Pasted image 20210517185746.png]]
2.  Discuss the summary statistics, including the target variable and _all_ predictor variables you will need to gather from the data set to answer the research question.
- The Target variable is the churn column. The churn column is 75% No (the customer is still with the company) and 25% Yes (customer churn the company)—the predictor variable.
- The predictor variables will help predict the churn column. According to the chi-square and ANOVA test, the columns have a relationship with the churn column. The other columns that were rejected do not have a relationship with the churn column. Therefore, they will not be used to predict the churn column. 
3.  Explain the steps used to prepare the data for the analysis, including the annotated code.
- We used Chi-squared and ANOVA to select the essential features
	- ![[Pasted image 20210525132122.png]]
	- ![[Pasted image 20210525132154.png]]
- We then created a new Spreadsheet with only these columns.
![[Pasted image 20210525132051.png]]
4.  Generate univariate and bivariate visualizations of the distributions of variables in the cleaned data set. Include the target variable in your bivariate visualizations.
 - ![[Pasted image 20210525132532.png]]
 - ![[Pasted image 20210525132555.png]]
 - ![[Pasted image 20210525132603.png]]
 - ![[Pasted image 20210525132617.png]]
 - ![[Pasted image 20210525132627.png]]
- ![[Pasted image 20210525132634.png]]
-  ![[Pasted image 20210525132656.png]]
-  ![[Pasted image 20210525132716.png]]
 

# **Part IV: Model Comparison and Analysis**
 ## D.  Compare an initial and a reduced logistic regression model by doing the following:

1.  Construct an initial logistic regression model from _all_ predictors that were identified in Part C2
![[Pasted image 20210526181936.png]]
2.  Justify a statistically based variable selection procedure and a model evaluation metric to reduce the initial model in a way that aligns with the research question.
- we could eliminate Tenure and bandwidth GB year to eliminate columns correlation. 
3.  Provide a reduced logistic regression model.
![[Pasted image 20210526193056.png]]
_Note: The output should include a screenshot of each model._

## E.  Analyze the data set using your reduced logistic regression model by doing the following:

1.  Explain your data analysis process by comparing the initial and reduced logistic regression models, including the following elements:
- The initial model had an accuracy of 90% and the reduced model had a 65%.


	•  the logic of the variable selection technique
		- I selected the model based off the ANOVA test and chi-squared test.
		- I decided to remove bandwidth and tenure for the reduced model since the two columns had correlation.
		
	•  the model evaluation metric
	- The metric for the two models was mean accuracy. 

2.  Provide the output and _any_ calculations of the analysis you performed, including a confusion matrix.
##### regular model 
![[Pasted image 20210526195320.png]]
##### reduced model
![[Pasted image 20210526195355.png]]

_Note: The output should include the predictions from the refined model you used to perform the analysis._ 
  

# **Part V: Data Summary and Implications**

## F.  Summarize your findings and assumptions by doing the following:

1.  Discuss the results of your data analysis, including the following elements:

•  a regression equation for the reduced model
- ![[Pasted image 20210526195925.png]]

•  an interpretation of coefficients of the statistically significant variables of the model
- ![[Pasted image 20210527163310.png]]
- From our Logistic Regression model, we can see that most features have negative coefficients. Negative coefficient means that customer is less likely to churn if the feature is true. The customer is more likely to churn from the image if the customer has streaming TV(True), streaming Movie (True), and has a month-to-month contract. 

•  the statistical and practical significance of the model
- The model has essential statistical and practical significance because it lets the company focus on critical factors and what factors lead to churning.


•  the limitations of the data analysis
- The limitation of the model is that the churn column is not balanced.
The logistic regression model's primary limitation is that it assumes the linearity between the dependent and independent variables. 
- Logistic regression may lead to overfitting in the training sets. 


2.  Recommend a course of action based on your results.
I would recommend collecting more rows on customers who have to churn the company or resampling more data to create more rows with customers that have to churn the company.

# **Part VI: Demonstration**



## H.  List the web sources used to acquire data or segments of third-party code to support the application. Ensure the web sources are reliable.
- N/A 
## I.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.
- N/A