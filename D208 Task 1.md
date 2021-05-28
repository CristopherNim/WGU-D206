

### NBM2 — NBM2 TASK 1: MULTIPLE REGRESSION FOR PREDICTIVE MODELING
# **Part I: Research Question**

## A.  Describe the purpose of this data analysis by doing the following:
1.  Summarize **one** research question that is relevant to a real-world organizational situation captured in the data set you have selected and that you will answer using multiple regression.
- The telecommunication company wants to know if the features on the data can predict the tenure of the customer. 
2.  Define the objectives or goals of the data analysis. Ensure that your objectives or goals are reasonable within the scope of the data dictionary and are represented in the available data.
- The goal of the model is to be off by no more than 5 months.
- see what features impact the tenure column the most.  

# **Part II: Method Justification**

## B.  Describe multiple regression methods by doing the following:
1.  Summarize the assumptions of a multiple regression model.
- All numeric variables follow a normal distribution (bell curve).
- data is homoscedastic. 
- there is almost no autocorrelation. 
- very little or no Multicollinearity.
2.  Describe the benefits of using the tool(s) you have chosen (i.e., Python, R, or both) in support of various phases of the analysis.
- python has various libraries that make it easy to implement the multiple linear regression model. 
	- Numpy - contains statistical functions.
	- pandas - create the data frame and allow data manipulation.
	- sklearn -  Contains the Naive Bayes algorithm function.
	- seaborn and matplotlib libraries will allow us to make visualizations. 
-  Explain why multiple regression is an appropriate technique to analyze the research question summarized in Part I.
- Linear regression is an algorithm that uses two or more features to predict a numeric feature. It is easy to implement and understand. in addition, our features have normal distribution making it likely that the model will have a high accuracy. 
  

# **Part III: Data Preparation**
## C.  Summarize the data preparation process for multiple regression analysis by doing the following:
1.  Describe your data preparation goals and the data manipulations that will be used to achieve the goals.
- Goals:
	- The categorical features are going to be turned into numbers with the pandas library functions. The pd.get_dummies functions will turn the columns into numeric from 1 = no and 1 =yes. 
	- The numeric columns will be tested to make sure they have a normal distribution.
2.  Discuss the summary statistics, including the target variable and _all_ predictor variables that you will need to gather from the data set to answer the research question.

3.  Explain the steps used to prepare the data for the analysis, including the annotated code.

4.  Generate univariate and bivariate visualizations of the distributions of variables in the cleaned data set. Include the target variable in your bivariate visualizations.

5.  Provide a copy of the prepared data set.

# **Part IV: Model Comparison and Analysis**

## D.  Compare an initial and a reduced multiple regression model by doing the following:

1.  Construct an initial multiple regression model from _all_ predictors that were identified in Part C2.

2.  Justify a statistically based variable selection procedure and a model evaluation metric to reduce the initial model in a way that aligns with the research question.

3.  Provide a reduced multiple regression model that includes _both_ categorical and continuous variables.

  

_Note: The output should include a screenshot of each model._

## E.  Analyze the data set using your reduced multiple regression model by doing the following:
1.  Explain your data analysis process by comparing the initial and reduced multiple regression models, including the following elements:
	•  the logic of the variable selection technique

	•  the model evaluation metric

	•  a residual plot

2.  Provide the output and _any_ calculations of the analysis you performed, including the model’s residual error.
_Note: The output should include the predictions from the refined model you used to perform the analysis._ 

3.  Provide the code used to support the implementation of the multiple regression models.

 
# **Part V: Data Summary and Implications**

## F.  Summarize your findings and assumptions by doing the following:

1.  Discuss the results of your data analysis, including the following elements:

	•  a regression equation for the reduced model

	•  an interpretation of coefficients of the statistically significant variables of the model

	•  the statistical and practical significance of the model

	•  the limitations of the data analysis

2.  Recommend a course of action based on your results.

  

#  **Part VI: Demonstration ==Review link== ** 

## G.  Provide a Panopto video recording that includes _all_ of the following elements:

•  a demonstration of the functionality of the code used for the analysis

•  an identification of the version of the programming environment

•  a comparison of the **two** multiple regression models you used in your analysis

•  an interpretation of the coefficients.


## I.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.