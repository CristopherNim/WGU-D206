# **Part I:  Research Question**

### A.  Describe the purpose of this data analysis by doing the following:

1.  Summarize **one** research question that is relevant to a real-world organizational situation captured in the selected data set and that you will answer using time series modeling techniques.
 - The company wants to understand the financial impact churning is having in the current times and in the future.
2.  Define the objectives or goals of the data analysis. Ensure that your objectives or goals are reasonable within the scope of the scenario and are represented in the available data.  
- The goal of the data analysis  is to ensure the leaders of the company understand the financial impact that churning is having and how it affects the company moving forward. The objective is to create visualization and machine learning model to predict the churning financial impact. 
  

# **Part II:  Method Justification**

### B.  Summarize the assumptions of a time series model including stationarity and autocorrelated data.  
- Assumptions for time series model:
	- Stationary assumptions:
		- that the mean and the variance does not change over time.
		- The structure does not change over time. 
		- helps understand trend without having variance and variables change over time
	-  Autocorrelation: 
		-  The lag between the data and now. Defining it by time units. 
		-  autocorrelation has residual errors.
		-  To create the best time series model is to use stationary data, but it should not be the expected outcome.  

# **Part III:  Data Preparation**

### C.  Summarize the data cleaning process by doing the following:

1.  Provide a line graph visualizing the realization of the time series.
![[Pasted image 20210605155341.png]]
2.  Describe the time step formatting of the realization, including any gaps in measurement and the length of the sequence.
- The revenue feature is used millions.
	- For example, 2.5 is 2.5 millions
	- For example, 5 is 5 millions
- Between day 0 and 90:
	- The company saw an increase of 0 to 7.5. During that time the company had a lost revenue of 3 to 1.5 millions. During that time we can assume that the company lost some revenue due to churning.
	- between day 90 to 180 the company experience a lost in revenue of 2.5 millions. 
		- During that time the company experience inclines follow by declines.
		- We can theorize that the company experience churning
	- Between day 180 to 270:
		- Profit increase to 11 millions
		- we can assume that the company experience a surge of new customers.]
	- Between day 270 - 360:
		- profit increased by one million.
		- In addition, we can theorize the company experience churning, with new customers joining towards the latter part.
	- Between day 360 to 610:
		- The company experience a similar trend between day 270 to 360
	- Between day 610 to 630:
		- a profit loss of 4.5 millions. 
		- We can theorize based on the data that the company experience a lot of customer churning.
	- Between day 630 to 730:
		- experience a profit of 8 Million.
			- Just by looking at this trend and data we can theorize that the company experience minimal churning with a surgent of new customers.
4.  Evaluate the stationarity of the time series.
 
4.  Explain the steps used to prepare the data for analysis, including the training and test set split.

5.  Provide a copy of the cleaned dataset.  
  

# **Part IV:  Model Identification and Analysis**

### D.  Analyze the time series dataset by doing the following:

1.  Report the annotated findings with visualizations of your data analysis, including the following elements:

•   the presence or lack of a seasonal component

•   trends

•   auto correlation function

•   spectral density

•   the decomposed time series

•   confirmation of the lack of trends in the residuals of the decomposed series

2.  Identify an autoregressive integrated moving average (ARIMA) model that takes into account the observed trend and seasonality of the time series data.

3.  Perform a forecast using the derived ARIMA model.

4.  Provide the output and calculations of the analysis you performed.

5.  Provide the code used to support the implementation of the time series model.  
  

# **Part V:  Data Summary and Implications**

### E.  Summarize your findings and assumptions, including the following points:

1.  Discuss the results of your data analysis, including the following:

•   the selection of an ARIMA model

•   the prediction interval of the forecast

•   a justification of the forecast length

•   the model evaluation procedure and error metric

2.  Provide an annotated visualization of the forecast of the final model compared to the test set.

3.  Recommend a course of action based on your results.  
  

# **Part VI:  Reporting**

### F.  Create your report from part E using an industry-relevant interactive development environment (e.g., an R Markdown document, a Jupyter Notebook, etc.). Include a PDF or HTML document of your executed notebook presentation.  
  

### G.  List the web sources used to acquire data or segments of third-party code to support the application.  
  

### H.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.  
  

### I.  Demonstrate professional communication in the content and presentation of your submission.