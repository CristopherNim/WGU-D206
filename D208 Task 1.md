

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
- ![[Pasted image 20210528183338.png]]
- ![[Pasted image 20210528183349.png]]
- The numeric features follow a normal distribution (bell curve).
- ![[Pasted image 20210528183428.png]]
- ![[Pasted image 20210528183436.png]]
- ![[Pasted image 20210528183447.png]]
- ![[Pasted image 20210528183501.png]]
- ![[Pasted image 20210528183510.png]]
- ![[Pasted image 20210528183518.png]]
- Techie, Churn, Gender contract, and phone are the only columns that are not balance well. 

3.  Explain the steps used to prepare the data for the analysis, including the annotated code.
- The only step to prepare the data is to turn the categorical columns into numeric as stated above. 
![[Pasted image 20210528184030.png]]
4.  Generate univariate and bivariate visualizations of the distributions of variables in the cleaned data set. Include the target variable in your bivariate visualizations.
- ![[Pasted image 20210525132532.png]]
 - ![[Pasted image 20210525132555.png]]
 - ![[Pasted image 20210525132603.png]]
 - ![[Pasted image 20210525132617.png]]
 - ![[Pasted image 20210525132627.png]]
- ![[Pasted image 20210525132634.png]]
-  ![[Pasted image 20210525132656.png]]
-  ![[Pasted image 20210525132716.png]]
5.  Provide a copy of the prepared data set.
✅️
# **Part IV: Model Comparison and Analysis**

## D.  Compare an initial and a reduced multiple regression model by doing the following:

1.  Construct an initial multiple regression model from _all_ predictors that were identified in Part C2.
- ![[Pasted image 20210528185224.png]]
2.  Justify a statistically based variable selection procedure and a model evaluation metric to reduce the initial model in a way that aligns with the research question.
- ![[Pasted image 20210528185901.png]]
- In order to reduce the model we first need to identify the import factors that most affect the outcome. The coefficient let's us visualize the important features.
- The columns that have little impact on the outcome are:
	- Bandwidth GB per year
	- Phone
	- Techie 
1.  Provide a reduced multiple regression model that includes _both_ categorical and continuous variables.
- we will remove Bandwidth GB per year, Phone and techie.
- ![[Pasted image 20210528192705.png]]
  

_Note: The output should include a screenshot of each model._

## E.  Analyze the data set using your reduced multiple regression model by doing the following:
1.  Explain your data analysis process by comparing the initial and reduced multiple regression models, including the following elements:
- ![[Pasted image 20210528195045.png]]
- From the table you can deduct that the original model is the more accurate one just by looking at the first 9 rows. The columns removed were pivotal to predicting the Tenure column. 
- ![[Pasted image 20210528195416.png]]
- The median from the columns let's us know that the original model is the more accurate of the two models.
- The logic of the variables selection were based off the coefficients visualization. 
- The model evaluation metric is based off how close the prediction is to the churn column. The original model is off by +- ~2 while the reduced model is off by +- ~30.
-  a residual plot

2.  Provide the output and _any_ calculations of the analysis you performed, including the model’s residual error.
_Note: The output should include the predictions from the refined model you used to perform the analysis._ 

3.  Provide the code used to support the implementation of the multiple regression models.
✅️
 
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