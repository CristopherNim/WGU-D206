### NVM2 TASK 2: PREDICTIVE ANALYSIS
# **Part I: Research Question**

## .  Describe the purpose of this data mining report by doing the following:

1.  Propose **one** question relevant to a real-world organizational situation that you will answer using **one** of the following prediction methods:
	1.  The Telecommunication company is looking to identify which customers are more likely to churn. The company wants to increase its retention rate because it cost them ten times more to acquire customers than to retain an existing customer. I am going to use random forest algorithm to predict the churn column. 

	•  decision trees

	•  random forests

	•  advanced regression (i.e., lasso or ridge regression)

2.  Define **one** goal of the data analysis. Ensure that your goal is reasonable within the scope of the scenario and is represented in the available data.  
- The goal of the data analysis is to predict the churn column at a 80 percent accuracy.
 

# **Part II: Method Justification**

## B.  Explain the reasons for your chosen prediction method from part A1 by doing the following:

1.  Explain how the prediction method you chose analyzes the selected data set. Include expected outcomes.
- The prediction method chosen is Random Forest(RF). RF works like if, else statements. If it meets certain conditions then the statement might be true else it false. It creates various trees to meet all the conditions. The trees protect each other from individual errors. The way trees protect each other from making errors is that the trees have low correlation
- ![[Pasted image 20210527175835.png]]
3.  Summarize **one** assumption of the chosen prediction method.
- Usually there is no assumption on Random Forest. The only assumption is that it has a binary split. 
4.  List the packages or libraries you have chosen for Python or R, and justify how _each_ item on the list supports the analysis.  
- Numpy - Numpy contains statistical functions.
- pandas - creates the data frame and allow data manipulation.
 - sklearn - it contains the random forest algorithm function.
 - seaborn and matplotlib libaries will allow us to make visualizations. 

# **Part III: Data Preparation**

## C.  Perform data preparation for the chosen data set by doing the following:

1.  Describe **one** data preprocessing goal relevant to the prediction method from part A1.
- The columns with categorical values will be transformed into individuals columns with Pandas function get_dummies. one for yes and zero for no.
2.  Identify the initial data set variables that you will use to perform the analysis for the prediction question from part A1, and group _each_ variable as continuous or categorical. 
- ![[Pasted image 20210527182853.png]]
- ![[Pasted image 20210527183020.png]]
3.  Explain the steps used to prepare the data for the analysis. Identify the code segment for _each_ step.
- ![[Pasted image 20210527184602.png]]
- For the churn column the yes was replaced with 1 and no was replaced with 0.
- ![[Pasted image 20210527184741.png]]
- The categorical variables were divided by yes or no columns 
- ![[Pasted image 20210527184838.png]]
- Finally the data was split to 80% percent training and 20% testing.
- The model score is 89% 
- ![[Pasted image 20210527185042.png]]
 

# **Part IV: Analysis**

## D.  Perform the data analysis and report on the results by doing the following:

1.  Split the data into training and test data sets and provide the file(s).
✅
2.  Describe the analysis technique you used to appropriately analyze the data. Include screenshots of the intermediate calculations you performed.
- Chi-square test for relationship between categorical columns.
- ![[Pasted image 20210527200433.png]]
- The ANOVA test for relationship between churn and continuous columns 
- ![[Pasted image 20210527200547.png]] 
- ![[Pasted image 20210527200645.png]]
- ![[Pasted image 20210527200702.png]]
- ![[Pasted image 20210527200714.png]]
4.  Provide the code used to perform the prediction analysis from part D2.  
 ✅ EDA

# *Part V: Data Summary and Implications**

## E.  Summarize your data analysis by doing the following:

1.  Explain the accuracy and the mean squared error (MSE) of your prediction model.
- The first row in the array the column has 99% of being 0 and 1% percent chance of being 1. The second value has 39% chance 0 and 61 % of being yes. This is how the algorithm predicts its probabilities(mean accuracy).
![[Pasted image 20210527201448.png]]
###### MSE
![[Pasted image 20210527202054.png]]
- MSE is telling us that our model is 90 accurate(10.9% inaccurate)
2.  Discuss the results and implications of your prediction analysis.
-![[Pasted image 20210527203558.png]]
- The model accuracy for 
3.  Discuss **one** limitation of your data analysis.

4.  Recommend a course of action for the real-world organizational situation from part A1 based on your results and implications discussed in part E2.  
 

# **Part VI: Demonstration**

## F.  Provide a Panopto video recording that includes a demonstration of the functionality of the code used for the analysis and a summary of the programming environment.

## G.  Record the web sources used to acquire data or segments of third-party code to support the analysis. Ensure the web sources are reliable.  
 
https://towardsdatascience.com/understanding-random-forest-58381e0602d2

## H.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.  
 

## I.  Demonstrate professional communication in the content and presentation of your submission.