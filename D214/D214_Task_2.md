- [ ] # **Research Question**

**Research Question:** Can a machine learning model be created statistically significantly to predict if a nursing home will be fined a ticket?
The feature we are trying to predict is the number of fines. The dataset contains other features that will aid in the prediction of number of fines. some of the columns that will aid in the predicted column are nursing home rating, the size of the nursing home, how many beds each nursing home has, and the amount of complains each nursing home has. I believe that there is enough valuable information with the features to try to answer the research question.

**Null Hypothesis**-: The independent variable cannot statistically significantly predict if a nursing home will be fined a ticket. The null hypothesis states that there is not enough valuable information in the features that will aid in the prediction of the number of fines. 

**Alternate Hypothesis**-: The independent variable can statistically significantly predict if a nursing home will be fined a ticket. The alternative hypothesis states there is enough information valuable information in the features to accurately predict the number of fines.

# **Data Collection**          

All data analyzed here comes from the Centers for Medicare and Medicaid Services. BuzzFeed News on GitHub put together the Dataset. The [Dataset](https://data.medicare.gov/data/nursing-home-compare) includes features like provider name, city, zip code, type of provider, business name, and hours of staff. total amount of fines in dollars, total number of penalties features will be remove, because if a fine occurs  money and a penalty will happen. 

Limitation: The dataset contains null values on the exact number of patients in care for each nursing home. Filling these missing values will prove to be challenging. Some of the rows with total staff hours also contain nulls. Delimitations: The Dataset has about ~14,000 rows, and some of the rows specified above will be removed with null values.



# **Data Extraction and Preparation**

###### C.  Describe your data-extraction and -preparation process and provide screenshots to illustrate _each_ step. Explain the tools and techniques you used for data extraction and data preparation, including how these tools and techniques were used on the data. Justify why you used these particular tools and techniques, including one advantage and one disadvantage when they are used with your data-extraction and -preparation methods. 

I am extracting data and preparing data to predict the number of fines feature. I looked at the spreadsheet and noticed that every time a fine occur the total amount of fines in dollars will increase. In addition, total number of penalties will essentially match the number of fines columns. If we left both features our model will produce a 95% accuracy rate. ![[Pasted image 20210920145154.png]]

Once we remove these two features we get a 79% accuracy rate to predicting whether or not the nursing home will be fine. ![[Pasted image 20210920191458.png]]

It is important to remove these two features, because in real life we won't know the amount of money in fines we will get until we get fined. The same goes for the number of penalties. The random forest model does not need the data to be normalized or for outliers to be removed. Random forest use trees, which split the data into multiple groups. For example the outliers don't have extra effect like in regression models, because they will only affect the leaf node they are in. The other leaf nodes are left unaffected. We can remove the outliers but it will essentially be a waste of time.
![[Pasted image 20210920150140.png]]

##### Now let's look at the null values
![[Pasted image 20210920150426.png]]
![[Pasted image 20210920150516.png]]
![[Pasted image 20210920150453.png]]

These are the features that have 75% or more null values. 
![[Pasted image 20210920150924.png]]

The requirement for the project is to have 10,000 or more rows. The data set has 15,446 total rows. If we removed all the rows that have null values we will still have 11,847 rows to work with. Furthermore, the difficult part of filling null values is that I do not have an expert consultant to help me understand the data. In addition, filling the null values will add noise to the dataset making it harder to use the model in real time use. The disadvantage of removing rows is removing data. The more rows the dataset has the more accurate the model is. 

##### Turning categorical values into integers
Random Forest model needs all features to be numerical, integers or float values. I used pandas library to turn categorical values into numerical for the model to work and produce no errors. The following python code turns all categorical values into integers.
![[Pasted image 20210920153300.png]] 

The model I will used to predict the fined feature is random forest. I will outline the assumptions, advantages, and disadvantages.
##### Random Forest Assumptions
The only assumption to random forest model is that it can handle outliers and multi-modal data. 
##### advantages to Random Forest 
- Robust to outliers. 
	- This will help us deal with outliers since I have no background in nursing home data and do not have an expert on the data. 
- Runs efficiently on large datasets
	- The data is relative large
- low risk to overfitting
##### Disadvantages to Random Forest 
- Slow training 
	- It will take time to train the data 
- Biased when dealing with categorical variables. 
	- The feature categorical columns will have some sort of biased attached to them

###### Preparing the data for the Random Forest Model
1) The y variable will represent whether the nursing home was fined or not. The X features are going to be use to predict the y feature. 
# **Analysis**

###### D.  Report on your data-analysis process by describing the analysis technique(s) you used to appropriately analyze the data. Include the calculations you performed and their outputs. Justify how you selected the analysis technique(s) you used, including one advantage and one disadvantage of these technique(s).

# **Data Summary and Implications**

###### E.  Summarize the implications of your data analysis by discussing the results of your data analysis in the context of the research question, including one limitation of your analysis. Within the context of your research question, recommend a course of action based on your results. Then propose **two** directions or approaches for future study of the data set.

###### F.  Acknowledge sources, using in-text citations and references, for content that is quoted.