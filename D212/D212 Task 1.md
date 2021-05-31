# **Part I: Research Question**

### A.  Describe the purpose of this data mining report by doing the following:
1.  Propose **one** question relevant to a real-world organizational situation that you will answer using **one** of the following clustering techniques:
The telecommunication is looking to target customers who will not churn the company. With hierarchical clustering we will be able to identify what customers to pursue. The question is what customers should we target for our current product?


2.  Define **one** goal of the data analysis. Ensure that your goal is reasonable within the scope of the scenario and is represented in the available data.  
 - The goal of the Data analysis is to identify what customers the company should target using hierarchical clustering. 
https://www.analyticsvidhya.com/blog/2019/05/beginners-guide-hierarchical-clustering/
# **Part II: Technique Justification**

### B.  Explain the reasons for your chosen clustering technique from part A1 by doing the following:

1.  Explain how the clustering technique you chose analyzes the selected dataset. Include expected outcomes.
- clustering technique uses unsupervised learning. Clustering will divide the data into 2 or more clusters. 
- The expected outcome is two have two different groups (clusters). One group will be the group that will churn the company. The other group is the customers that will stay with the company long term.
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
- We will turn our categorical columns into 1's and 0's. The pandas function get_dummies will turn the columns into binary. The 1's are for yes = True and the 0's stand for no = False.

2.  Identify the initial dataset variables that you will use to perform the analysis for the clustering question from part A1, and label _each_ as continuous or categorical.
- ![[Pasted image 20210527182853.png]]
- ![[Pasted image 20210527183020.png]]

3.  Explain _each_ of the steps used to prepare the data for the analysis. Identify the code segment for _each_ step.
![[Pasted image 20210530210617.png]]
- First we created a loop to grab the numeric features for the dataframe. Then we grab those numeric features and put them into a list. We follow that up and create a new dataframe with only numeric features. Finally we normalize the numeric features and make a new dataframe with the normalize numeric features. 
- ![[Pasted image 20210530210956.png]]
- We do the same for the categorical features, but instead we turn the categorical features into binary columns using the get_dummies function. 
- ![[Pasted image 20210530211057.png]]
- Lastly we merge the two dataframes back into one using the pandas concat function.
4.  Provide a copy of the cleaned dataset.  
 ✅️

# **Part IV: Analysis**

### D.  Perform the data analysis and report on the results by doing the following:

1.  Split the data into training and test data sets and provide the file(s).
✅️
2.  Describe the analysis technique you used to appropriately analyze the data. Include screenshots of the intermediate calculations you performed.

3.  Provide the code used to perform the clustering analysis technique from part 2.  
 

# **Part V: Data Summary and Implications**

### E.  Summarize your data analysis by doing the following:

1.  Explain the accuracy of your clustering technique.

2.  Discuss the results and implications of your clustering analysis.

3.  Discuss **one** limitation of your data analysis.

4.  Recommend a course of action for the real-world organizational situation from part A1 based on your results and implications discussed in part E2.  
 

# **Part VI: Demonstration**

### .  Provide a Panopto video recording that includes a demonstration of the functionality of the code used for the analysis and a summary of the programming environment.  
 

_Note: The audiovisual recording should feature you visibly presenting the material (i.e., not in voiceover or embedded video) and should simultaneously capture both you and your multimedia presentation._  
 

 

#### G.  Record the web sources used to acquire data or segments of third-party code to support the analysis. Ensure the web sources are reliable.  
 N/A did not used any

#### H.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.  
  N/A did not used any