# **Part I: Research Question**

### A.  Describe the purpose of this data mining report by doing the following:

1.  Propose **one** question relevant to a real-world organizational situation that you will answer by using principal component analysis (PCA).
- The organization wants to know if they can predict the churning feature only using numeric features.
2.  Define **one** goal of the data analysis. Ensure that your goal is reasonable within the scope of the scenario and is represented in the available data. 
-  The goal of the data analyst is to create visualizations and find out if we can create two cluster groups. One for customers who have churn and one for customer who have not churn. In addition, we want to find out what columns have correlation with each other.
 

# **Part II: Method Justification**

### B.  Explain the reasons for using PCA by doing the following:

1.  Explain how PCA analyzes the selected data set. Include expected outcomes.
- PCA works best with continuous features. We selected only continuous features and created a csv with only these features. The PCA analyzes the data and let's us know what features provide the most important information. Then the goal is to use only the important features to make the visualizations and see what features have a correlation. The expected outcome is that we can create a visualization to know what features have a correlation and cluster group to tell what customers have churn and those who have not churn. 
2.  Summarize **one** assumption of PCA.  
 - PCA makes the assumption that there are no unique variance. Variance tells you the degree of spread in the data we are using. The more spread the data, the larger the variance is to the relation of the mean.  The distribution of variance can be seen better when looking at a normal distribution graph (bell curve).

# **Part III: Data Preparation**

### C.  Perform data preparation for the chosen dataset by doing the following:

1.  Identify the continuous dataset variables that you will need in order to answer the PCA question proposed in part A1.
![[Pasted image 20210531004804.png]]
The Image above are all the continuous variables in our data set. 
2.  Standardize the continuous dataset variables identified in part C1. Include a copy of the cleaned dataset.  
 ✅️
 ![[Pasted image 20210531004907.png]]
  ![[Pasted image 20210531004920.png]]

# **Part IV: Analysis**

### D.  Perform PCA by doing the following:

1.  Determine the matrix of _all_ the principal components.
![[Pasted image 20210531005202.png]]
The above image has all the important components and the list below has components attached to each PCA based off the PCA components importance.
PC0 - Tenure
PC1 - Outage, Monthly Charge
PC2 - 
PC3 - Age
PC4 -  Income, Population
2.  Identify the _total_ number of principal components using the elbow rule or the Kaiser criterion. Include a screenshot of the scree plot.
- ![[Pasted image 20210531005637.png]]

3.  Identify the variance of _each_ of the principal components identified in part D2.

4.  Identify the _total_ variance captured by the principal components identified in part D2.

5.  Summarize the results of your data analysis.  
 

# **Part V: Attachments**

### E.  Record the web sources used to acquire data or segments of third-party code to support the analysis. Ensure the web sources are reliable.  
 

### F.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.  
  N/A did not used any
