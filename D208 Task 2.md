
### NBM2 TASK 2: LOGISTIC REGRESSION FOR PREDICTIVE MODELING
# **Part I: Research Question**

## A.  Describe the purpose of this data analysis by doing the following:

1.  Summarize **one** research question that is relevant to a real-world organizational situation captured in the data set you have selected and that you will answer using logistic regression.
-  The Telecommunication company is looking to identify which customers are more likely to churn. The company wants to increase its retention rate because it cost them 10 times more to acquire customers than to retain an existing one 1    

2. Define the objectives or goals of the data analysis. Ensure that your objectives or goals are reasonable within the scope of the data dictionary and are represented in the available data.
- The goal of the analysis is to make model that is able to predict the churn at a 80 percent accuracy. 
  

# **Part II: Method Justification**

## B.  Describe logistic regression methods by doing the following:

1.  Summarize the assumptions of a logistic regression model.
- First, Binary logistic regression requires the dependent variables to be binary and ordinal. 
- The data observations need to be independent of each other. 
- The independent variables should not have high correlation.
- The dataset needs to have more than 10 row.
2.  Describe the benefits of using the tool(s) you have chosen (i.e., Python, R, or both) in support of various phases of the analysis.
- The team has chosen python because it is the most used tool for data analysis. It can be combined with SQL if more records need to be used. 
3.  Explain why logistic regression is an appropriate technique to analyze the research question summarized in Part I.
- Logistic regression is able to predict binary columns. It is easy to implement coding wise. Most importantly logistic regression has a lower bias than naive bayes that will be used later on the project.
  

# **Part III: Data Preparation**

## C.  Summarize the data preparation process for logistic regression by doing the following:

1.  Describe your data preparation goals and the data manipulations that will be used to achieve the goals.
- During the data exploration the data analysis team ran chi square test and ANOVA test for feature extraction. The image below is the columns that are statistically significant to the churn column. Meaning that the columns are significant and we can be confident that they help predict the churn values
-  ![[Pasted image 20210517185746.png]]
2.  Discuss the summary statistics, including the target variable and _all_ predictor variables that you will need to gather from the data set to answer the research question.
- The Target variable is the churn column. The churn column is 75% No (the customer is still with the company) and 25% Yes (customer churn the company). The predictor variable.
- The predictor variables will help predict the churn column. According to chi-square and ANOVA test the columns have a relationship with the churn column. The other columns that were rejected do not have a relationship with the churn column. Therefore, they will not be used to predict the churn column. 
3.  Explain the steps used to prepare the data for the analysis, including the annotated code.

4.  Generate univariate and bivariate visualizations of the distributions of variables in the cleaned data set. Include the target variable in your bivariate visualizations.

5.  Provide a copy of the prepared data set.

  

# **Part IV: Model Comparison and Analysis**

## D.  Compare an initial and a reduced logistic regression model by doing the following:

1.  Construct an initial logistic regression model from _all_ predictors that were identified in Part C2

2.  Justify a statistically based variable selection procedure and a model evaluation metric to reduce the initial model in a way that aligns with the research question.

3.  Provide a reduced logistic regression model.

_Note: The output should include a screenshot of each model._

## E.  Analyze the data set using your reduced logistic regression model by doing the following:

1.  Explain your data analysis process by comparing the initial and reduced logistic regression models, including the following elements:

	•  the logic of the variable selection technique

	•  the model evaluation metric

2.  Provide the output and _any_ calculations of the analysis you performed, including a confusion matrix.

_Note: The output should include the predictions from the refined model you used to perform the analysis._ 

3.  Provide the code used to support the implementation of the logistic regression models.

  

# **Part V: Data Summary and Implications**

## F.  Summarize your findings and assumptions by doing the following:

1.  Discuss the results of your data analysis, including the following elements:

	•  a regression equation for the reduced model

	•  an interpretation of coefficients of the statistically significant variables of the model

	•  the statistical and practical significance of the model

	•  the limitations of the data analysis

2.  Recommend a course of action based on your results.

  

# **Part VI: Demonstration**

## G.  Provide a Panopto video recording that includes _all_ of the following elements: review link

•  a demonstration of the functionality of the code used for the analysis

•  an identification of the version of the programming environment

•  a comparison of the **two** logistic regression models you used in your analysis

•  an interpretation of the coefficients

## H.  List the web sources used to acquire data or segments of third-party code to support the application. Ensure the web sources are reliable.

## I.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.

## J.  Demonstrate professional communication in the content and presentation of your submission.