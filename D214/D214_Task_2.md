- [ ] # **Research Question**

**Research Question:** Can a machine learning model be created statistically significantly to predict if a nursing home will be fined a ticket?
The feature we are trying to predict whether the nursing home is in danger of getting fined. The dataset contains other features that will aid in the prediction of predictable variable. some of the columns that will aid in the predicted column are nursing home rating, the size of the nursing home, how many beds each nursing home has, and the amount of complains each nursing home has. I believe that there is enough valuable information with the features to try to answer the research question.

**Null Hypothesis**-: The independent variable cannot statistically significantly predict if a nursing home will be fined a ticket. The null hypothesis states that there is not enough valuable information in the features that will aid in the prediction of the number of fines. 

**Alternate Hypothesis**-: The independent variable can statistically significantly predict if a nursing home will be fined a ticket. The alternative hypothesis states there is enough information valuable information in the features to accurately predict the number of fines.

# **Data Collection (Library)**       
![[Pasted image 20210920195330.png]]
![[Pasted image 20210920195348.png]]
![[Pasted image 20210920195424.png]]
![[Pasted image 20210920195441.png]]
![[Pasted image 20210920195505.png]]
![[Pasted image 20210920195540.png]]
![[Pasted image 20210920195559.png]]

All data analyzed here comes from the Centers for Medicare and Medicaid Services. BuzzFeed News on GitHub put together the Dataset. The [Dataset](https://data.medicare.gov/data/nursing-home-compare) includes features like provider name, city, zip code, type of provider, business name, and hours of staff. total amount of fines in dollars, total number of penalties features will be remove, because if a fine occurs  money and a penalty will happen. 

Limitation: The dataset contains null values on the exact number of patients in care for each nursing home. Filling these missing values will prove to be challenging. Some of the rows with total staff hours also contain nulls. Delimitations: The Dataset has about ~14,000 rows, and some of the rows specified above will be removed with null values.



# **Data Extraction, Preparation Analysis**

###### C.  
 libraries for Python to prepare the data and preparation 
 - Numpy - Numpy contains statistical functions.
- pandas - create the data frame and allow data manipulation.
 - sklearn -  Contains the Naive Bayes algorithm function.
 - seaborn and matplotlib libraries will allow us to make visualizations. 


The first step is to turn the feature of number of fines into a binary column. The goal of the model is to predict whether the nursing home is in danger to getting fine not how many times. I used the following code in python to turn the numerical feature to a binary column. If the nursing home has been fined at least once then the row will have a 1 for yes. If the nursing home has not been fined then the row will have a 0 for no
![[Pasted image 20210920192021.png]]. 

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
2) I then split X feature into training and testing set. I do the same for the y feature. Furthermore, the test sizes will be 20% and 80% of the data will be used for the training sets.  ![[Pasted image 20210920193147.png]]
3) We train the data to create a forest. ![[Pasted image 20210920193244.png]]
4) Finally, We test the data. ![[Pasted image 20210920193627.png]]
	1) The model score is 79% 

##### Feature importance
![[Pasted image 20210922140149.png]]
The graph above let's me see what features are important.

##### chi-square 
1) The first to testing dataset using the chi-square is to grab all the categorical columns. The code below grabs only the categorical features.                                         ![[Pasted image 20210922140514.png]]
2) The code below tests if there is a relationship between number of fines and all the other categorical features.
	1) ![[Pasted image 20210922140712.png]]
3) The accepted list has the feature that do have a relationship with the number of fines feature. The rejected list has the feature that do not have a relationship with number of fines feature. ![[Pasted image 20210922141129.png]]

##### Now let's the dataset with only the accepted categorical columns 
![[Pasted image 20210922141343.png]]
The model score is 78% after removing the features that do no aid in the prediction of number of fine feature. 
![[Pasted image 20210922141512.png]]
The importance feature graph looks similar with the only difference being with the removal of the rejected columns. 
#### we now only have 58 features after starting with 87 features 

#### Confusion matrix
![[Pasted image 20210922141802.png]]

##### Area Under the Curve 
The model Area under the curve is 71%. Meaning that is labeling the correct label 71% of the time. ![[Pasted image 20210922142503.png]]
# **Data Summary and Implications**
#### Analysis summary 
The top five columns that aid in the predictt

 - The Main limitation for random forest classifier that if it has a large number of trees, the algorithm is slow and ineffective for right away use. Waiting to get the results might cost the