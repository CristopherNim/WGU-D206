

### NBM2 — NBM2 TASK 1: MULTIPLE REGRESSION FOR PREDICTIVE MODELING
# **Part I: Research Question**

## A.  Describe the purpose of this data analysis by doing the following:
1.  Summarize **one** research question that is relevant to a real-world organizational situation captured in the data set you have selected and that you will answer using multiple regression.
The telecommunication company wants to know if the data features can predict the customer's tenure.  If the company can expect tenure, the company can have a good idea of how long each customer will stay with the company before churning.
2.  Define the objectives or goals of the data analysis. Ensure that your objectives or goals are reasonable within the scope of the data dictionary and are represented in the available data.
- The goal of the model is to be off by no more than five months.
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
- Linear regression is an algorithm that uses two or more features to predict a numeric feature. It is easy to implement and understand. in addition, our features have normal distribution making it likely that the model will have high accuracy. 
  

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

1.  Construct an initial multiple regression model from _all_ predictors identified in Part C2.
- ![[Pasted image 20210528185224.png]]
2.  Justify a statistically based variable selection procedure and a model evaluation metric to reduce the initial model in a way that aligns with the research question.
![[Pasted image 20210531171635.png]]
The Kendall method is a good way for feature extraction. It assumes one feature is categorical and the other numeric. Since the feature we are trying to predict is numeric, we will only look at categorical features. From the image above, we see that Phone, multiple, streaming tv, and streaming movies have a low correlation to tenure. For this reason, we are going to remove those features and make a prediction. 
3.  Provide a reduced multiple regression model that includes _both_ categorical and continuous variables.
![[Pasted image 20210531172344.png]]
The Image above provides categorical and continuous features. 
![[Pasted image 20210531172355.png]]
The Image above provides the output for the reduced model along with the score.
_Note: The output should include a screenshot of each model._

## E.  Analyze the data set using your reduced multiple regression model by doing the following:
1.  Explain your data analysis process by comparing the initial and reduced multiple regression models, including the following elements:
![[Pasted image 20210531172758.png]]
![[Pasted image 20210531172814.png]]
The model that was not reduced has a strong correlation with the actual scores of tenure. At the same time, the reduced model has a weak correlation with the actual scores of the tenure features. 
![[Pasted image 20210531172958.png]]
The reduced model is a hit or miss when it comes to predicting the actual model scores. In addition, you can see from the table that the first model overall has a reasonable prediction rate. 

- The model evaluation metric is based on how close the prediction is to the churn column. The original model is off by +- ~2, while the reduced model is off by +- ~30 or +- ~2.
-  a residual plot
![[Pasted image 20210528204126.png]]
- from the visualization of the residual plot, we can conclude, for the most part, that the model is accurate.  
- Where the model is making errors is when it is predicting 10-20 months of tenure.  
- From the Q-Q plot, we can conclude that the prediction is missing points from the right side of the normal distribution. 

3.  Provide the code used to support the implementation of the multiple regression models.
✅️
 
# **Part V: Data Summary and Implications**

## F.  Summarize your findings and assumptions by doing the following:

1.  Discuss the results of your data analysis, including the following elements:
 - based on our theory thatPhone, multiple, streaming tv, and streaming movies were not essential features to predict tenure column. We can conclude that we were wrong and should include this column to indicate the tenure column. 
- a regression equation for the reduced model
Y = linear_line + col_A + Col_B.... + col_Z
![[Pasted image 20210528215051.png]]
- an interpretation of coefficients of the statistically significant variables of the model
	- ![[Pasted image 20210528185901.png]]
	- For example, if the person has internet service DSL, the prediction number is below the actual number. 
	- If it has a positive coefficient, the model will predict tenure number above the actual correct tenure number.
- the statistical and practical significance of the model
	- From the statistical data, we can conclude Bandwidth, phone, and tenure correlate to the tenure column. 
- the limitations of the data analysis
- The limitation of linear models is that it assumes there is a straight line. The tenure column has a normal distribution, but the data must be resampled to be turned into a normal curve. In addition, multiple regression is sensitive to outliers meaning for the model to remain accurate, we would need to clean the data often.
- In addition, not all the features are well balanced. Meaning if we enter data to balance out the data, the predictions might not be accurate.

2.  Recommend a course of action based on your results.
 - My recommendation that if we want to predict the tenure feature, the model will give us a good outlook on how long we can expect the customer to stay with the company. With this information, we can offer customers incentives to stay when the predicted tenure is close to the predicted rate to increase retention.
  


H.  List the web sources used to acquire data or segments of third-party code to support the application. Ensure the web sources are reliable.
N/A did not used any 

## I.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.

N/A did not used any