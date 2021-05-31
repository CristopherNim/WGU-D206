# **Part I: Research Question**

### A.  Describe the purpose of this data mining report by doing the following:

1.  Propose **one** question relevant to a real-world organizational situation that you will answer by using principal component analysis (PCA).
- The organization wants to know if they can predict the churning feature only using numeric features.
2.  Define **one** goal of the data analysis. Ensure that your goal is reasonable within the scope of the scenario and is represented in the available data. 
The data analyst aims to create visualizations and determine if we can create two cluster groups—one for customers who have churn and one for the customer who has not churned. In addition, we want to find out what columns correlate with each other.

 

# **Part II: Method Justification**

### B.  Explain the reasons for using PCA by doing the following:

1.  Explain how PCA analyzes the selected data set. Include expected outcomes.
- PCA works best with continuous features. We selected only continuous features and created a CSV with only these features. The PCA analyzes the data and lets us know what features provide the essential information. Then the goal is to use only the critical features to make the visualizations and see what features correlate. The expected outcome is that we can create a visualization to know what features have a correlation and cluster group to tell what customers have churn and those who have not to churn. 
2.  Summarize **one** assumption of PCA.  
 - PCA assumes that there is no unique variance. Variance tells you the degree of spread in the data we are using. The more spread the data, the larger the variance is to the relation of the mean.  The variance distribution can be seen better when looking at a normal distribution graph (bell curve).

# **Part III: Data Preparation**

### C.  Perform data preparation for the chosen dataset by doing the following:

1.  Identify the continuous dataset variables that you will need to answer the PCA question proposed in part A1.
![[Pasted image 20210531004804.png]]
The Image above is all the continuous variables in our data set. 
2.  Standardize the continuous dataset variables identified in part C1. Include a copy of the cleaned dataset.  
 ✅️
 ![[Pasted image 20210531004907.png]]
  ![[Pasted image 20210531004920.png]]

# **Part IV: Analysis**

### D.  Perform PCA by doing the following:

1.  Determine the matrix of _all_ the principal components.
![[Pasted image 20210531005202.png]]
The above image has all the essential components, and the list below has components attached to each PCA based on the PCA components importance.
PC0 - Tenure
PC1 - Outage, Monthly Charge
PC2 - 
PC3 - Age
PC4 -  Income, Population
2.  Identify the _total_ number of principal components using the elbow rule or the Kaiser criterion. Include a screenshot of the scree plot.
- ![[Pasted image 20210531005637.png]]
- The total number of components is from 0 to 4 based on the kaiser criterion. Component 0 to 4 has an eigenvalue above one.

3.  Identify the variance of _each_ of the principal components identified in part D2.
![[Pasted image 20210531005929.png]]
- PC0 has 27% variance.
- PC1 has a 15% variance
- PC2, PC3, and PC4 all have 14%
4.  Identify the _total_ variance captured by the principal components identified in part D2.
- The total variance capture from the PC0 to PC4 is 84%.
5.  Summarize the results of your data analysis.  
 ![[Pasted image 20210531010219.png]]
 From the visualization, we can the numeric values to create a visualization in 3d to identify what customers are with the company and those who have churn.
 ![[Pasted image 20210531010332.png]]
 The visualization above let us know what columns correlate:
  - PC0 tells us that Tenure and bandwidth GB per year has a positive correlation.
  - PC1 tells us that Outage per week and monthly charges have a positive correlation.
  - PC2 tells us that age, income, and population have a correlation
  - PC3 tells us that age and population have an inverse correlation 
  - PC4  tell us that Income and population have a positive correlation



# **Part V: Attachments**

### E.  Record the web sources used to acquire data or segments of third-party code to support the analysis. Ensure the web sources are reliable.  
N/A did not used any 

### F.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.  
  N/A did not used any
