# **Part I:  Research Question**

### A. Purpose of the analysis 

 - The company wants to understand the financial impact churning is having in the current times and the future.

- The goal of the data analysis is to ensure the company's leaders understand the financial impact that churning is having and how it affects the company moving forward. The objective is to create a visualization and machine learning model to predict the churning financial impact. 
  

# **Part II:  Method Justification**

### B.  
- Assumptions for time series model:
	- Stationary assumptions:
		- that the mean and the variance does not change over time.
		- The structure does not change over time. 
		- helps understand trend without having variance and variables change over time
	-  Autocorrelation: 
		-  The lag between the data and now. Defining it by time units. 
		-  autocorrelation has residual errors.
		To create the best time series model, use static data, but it should not be the expected outcome.  

# **Part III:  Data Preparation**

### C.

1.  Provide a line graph visualizing the realization of the time series.
![[Pasted image 20210605155341.png]]
2.  Describe the time step formatting of the realization, including any gaps in measurement and the length of the sequence.
- To create the visualization, I used a line plot using the matplotlib library. The y-axis was used for the revenue, and the x-axis is the days. The Xticks are separated by 90 days. 
3.  Evaluate the stationarity of the time series.
 The revenue feature is used millions.
- For example, 2.5 is 2.5 million
	- For example, five is five million
- Between day 0 and 90:
	- The company saw an increase of 0 to 7.5. During that time, the company had lost revenue of 3 to 1.5 million. During that time, we can assume that the company lost some income due to churning.
	- between days 90 to 180, the company experienced a loss in revenue of 2.5 million.
		-  During that time, the company experience inclines to follow by declines.
			- We can theorize that the company experience churning
	- Between day 180 to 270:
		- Profit increase to 11 million
			- we can assume that the company experience a surge of new customers.]
	- Between day 270 - 360
		- profit increased by one million.
		- We can theorize the company experience is churning, with new customers joining towards the latter part.
	- Between day 360 to 610
		- The company experienced a similar trend between day 270 to 360
	- Between day 610 to 630
		- a profit loss of 4.5 million. 
		- We can theorize based on the data that the company experienced a lot of customer churning.
	- Between day 630 to 730:
		- experience a profit of 8 Million
		- Just by looking at this trend and data, we can theorize that the company experiences minimal churning with a surge of new customers


3a. Testing for stationary or non stationarity
 ###### Augmented Dickey-Fuller Test
 ![[Pasted image 20210629223655.png]] 
 - The null hypothesis is that the data is non-stationarity, and alternative hypothesis is that the data is stationarity. 
 - The p-value is greater than the significant level of 0.05 we accept the null hypothesis. So, according the ADF test the data is non-stationarity.
 
4.  Explain the steps used to prepare the data for analysis, including the training and test set split.
![[Pasted image 20210608213656.png]]
- To create the model, I removed the column "day."
- The data was split into 80% percent training and 20% percent test data



# **Part IV:  Model Identification and Analysis**

### D.  

1.  Report the annotated findings with visualizations of your data analysis, including the following elements:

•   the presence or lack of a seasonal component
- Lacking seasonal components of data makes it challenging to understand trends. We can assume that the company has increased during seasonal months during that time, and after seasonal ends, the company has increased churning. 
•   trends
- Every 90 days, the company has increased in revenue. 
- After ten days of the 90th-day increase, the company has a loss in revenue.
•   autocorrelation function
- ![[Pasted image 20210608220228.png]] 
- Inside, the light blue cone is set to 95th confidence interval. Values inside the blue cone are likely a correlation and not a statistical fluke. 
•   spectral density 
![[Pasted image 20210608223213.png]]
![[Pasted image 20210608223222.png]]
We can see that the frequency does not change over time. In addition, it does not show seasonal trends.
•   the decomposed time series
![[Pasted image 20210608225953.png]]
There are no seasonal or residual trends in the dataset.
2.  Identify an autoregressive integrated moving average (ARIMA) 
![[Pasted image 20210608231341.png]]
![[Pasted image 20210610233538.png]]
**The image above shows a model that takes into account trends and seasonality trends. In addition, we tested for seasonality and observed no seasonality. The data does not show noticeable trends.**
![[Pasted image 20210629231236.png]]
![[Pasted image 20210629231320.png]]
3.  ARIMA model forecast:
The following graph is a trend for the next year. According to the movement, the company will see an increase in revenue from 16 million to 24 million. 
![[Pasted image 20210608231132.png]]
4.  
The images above show the outputs and calculations. Code will be provided with the submission. 

 

# **Part V:  Data Summary and Implications**

### E.  
1.  Discuss the results:
•   the selection of an ARIMA model
![[Pasted image 20210609003401.png]]
- The ARIMA model shows an increase of 8 million in revenue each year.
 - a justification of the forecast length
	 -  the forecast length is based on one year. Trying to predict even longer will be an inaccurate result to the real world as things always change outside just the data. For example, another company is becoming more popular and growing in user base.
•   the model evaluation procedure and error metric
![[Pasted image 20210609001125.png]]
The model accuracy is 95% based on the R^2 score. 
2.  Provide an annotated visualization of the forecast of the final model compared to the test set.
![[Pasted image 20210610234859.png]]
![[Pasted image 20210629231724.png]]
4.  Recommend a course of action:
  Every time the company has an increase in revenue, the company loses revenue due to churning. Based on the analysis, I would suggest that the Teleco company leaders invest research on customer churning to prevent the customer from churning to keep the trend upward. 

### G.
  N/A

### H. 
  N/A


