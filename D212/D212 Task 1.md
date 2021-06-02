# **Part I: Research Question**

### A.  Describe the purpose of this data mining report by doing the following:
1.  Propose **one** question relevant to a real-world organizational situation that you will answer using **one** of the following clustering techniques:
Telecommunication is looking to target customers who will not churn the company. With hierarchical clustering, we will be able to identify what customers to pursue. The question is, what customers should we target for our current product?


2.  Define **one** goal of the data analysis. Ensure that your goal is reasonable within the scope of the scenario and is represented in the available data.  
 The data analysis aims to identify what customers the company should target using hierarchical clustering. 

# **Part II: Technique Justification**

### B.  Explain the reasons for your chosen clustering technique from part A1 by doing the following:

1.  Explain how the clustering technique you chose analyzes the selected dataset. Include expected outcomes.
- clustering technique uses unsupervised learning. Clustering will divide the data into 2 or more clusters. 
- After the cluster are identified they are label and assigned to a group.
- The expected outcome is two have two different groups (clusters). One group will be the group that will churn the company. The other group is the customers that will stay with the company long term.
- The  Agglomerative Approach separated all the objects in the beginning. Then it keeps on merging until every object has a group.
2.  Summarize **one** assumption of the clustering technique.
 - There are no assumptions to hierarchical clustering.
 - One assumption we can presume is that there will be two groups of clusters. We will see if this assumption is true after we make the visualizations. 
3.  List the packages or libraries you have chosen for Python or R, and justify how _each_ item on the list supports the analysis.  
 - Numpy - Numpy contains statistical functions.
- pandas - create the data frame and allow data manipulation.
- sklearn - The library contains the normalize function to normalize our numeric columns
- Scipy - contains the cluster function that we will use.
- seaborn and matplotlib libraries will allow us to make visualizations. 
# **Part III: Data Preparation**

### C.  Perform data preparation for the chosen dataset by doing the following

1.  Describe **one** data preprocessing goal relevant to the clustering technique from part A1.
- We will turn our categorical columns into 1's and 0's. The panda's function get_dummies will turn the columns into binary. The 1's are for yes = True, and the 0's stand for no = False.

2.  Identify the initial dataset variables that you will use to analyze the clustering question from part A1, and label _each_ as continuous or categorical.
- ![[Pasted image 20210527182853.png]]
- ![[Pasted image 20210527183020.png]]

3.  Explain _each_ of the steps used to prepare the data for the analysis. Identify the code segment for _each_ step.
![[Pasted image 20210530210617.png]]
- First, we created a loop to grab the numeric features for the data frame. Then we hold those numeric features and put them into a list. We follow that up and create a new data frame with only numeric features. Finally, we normalize the numeric features and make a new data frame with the normalized numeric features. 
- ![[Pasted image 20210530210956.png]]
- We do the same for the categorical features, but instead, we turn the categorical features into binary columns using the get_dummies function. 
- ![[Pasted image 20210530211057.png]]
- Lastly, we merge the two data frames back into one using the pandas Concat function.
4.  Provide a copy of the cleaned dataset.  
 ✅️

# **Part IV: Analysis**

### D.  Perform the data analysis and report on the results by doing the following:

1.  Split the data into training and test data sets and provide the file(s).
✅️
2.  Describe the analysis technique you used to analyze the data appropriately. Include screenshots of the intermediate calculations you performed.
![[Pasted image 20210530232423.png]]
- First, I decided to see how many cluster groups I had in the data using the ward method. We only had two different clusters indicating that our data is cleaned and will provide insightful information. 
-  ![[Pasted image 20210530232642.png]]
-  ![[Pasted image 20210530232657.png]]
-  We can see from the visualization how the two groups differ. The yellow is the customers with churn, and the purple cluster is the group that has not churn. 
3.  Provide the code used to perform the clustering analysis technique from part 2.  
 ✅️

# **Part V: Data Summary and Implications**

### E.  Summarize your data analysis by doing the following:

1.  **Explain the accuracy** of your clustering technique.
- The cluster technique has a reasonable accuracy rate because the groups have a good separation when looking at the visualizations. We have two groups of clusters clearly separated. 
-![[Pasted image 20210602002211.png]]
- As for labeling the score we have is 60%
- The Rand index is proportional to the number of sample pairs whose labels are the same in both y_test and y_pred, or are different in both. Perfect labels will give a score of 1.0 (100%)
2.  Discuss the results and implications of your clustering analysis.
- ![[Pasted image 20210530234116.png]]
- The results are that if the customer has a tenure of 40, they are likely to stay with the company. If the customer has a bandwidth of above 3600, they are more likely not to churn 
3.  Discuss **one** limitation of your data analysis.

- One of the limitations of our data is that we do not have more numeric features. The lack of numeric features gives us more minor elements to visualize what customers to target as the company tries to increase its customer base. 

4.  Recommend a course of action for the real-world organizational situation from part A1 based on your results and implications discussed in part E2. 
	1.  My recommendation based on the data and visualization is the company target customers who have used 3600 GB of bandwidth and have a tenure of 40 months. We build a model of prediction Tenure is D208 task 1. This model could be used to predict the term of the company. The company can use a survey to indicate the tenure and go after these customers to expand its customer for the particular product. 
 

# **Part VI: Demonstration**

### .  Provide a Panopto video recording that includes a demonstration of the functionality of the code used for the analysis and a summary of the programming environment.  
 

_Note: The audiovisual recording should feature you visibly presenting the material (i.e., not in voiceover or embedded video) and should simultaneously capture both you and your multimedia presentation._  
 

 

#### G.  Record the web sources used to acquire data or segments of third-party code to support the analysis. Ensure the web sources are reliable.  
 N/A did not used any

#### H.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.  
  N/A did not used any