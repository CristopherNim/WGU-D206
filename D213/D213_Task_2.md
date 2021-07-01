# **Part I:  Research Question** 

### A.  
1.  The company leaders want an accurate model to predict if the comments are negative or positive for a given product. This will allow the leaders to see how the products is doing based on user comments.
2.  The goals of the data analysis is to create a model with an accuracy of 70%.
3.  Keras is a tool for constructing neural networks framework based on TensorFlow. Keras can be used for text classification tasks and can be trained for valuable predictions on text sequences.
3a. Long Short-Term Memory (_LSTM_) is a specific neural network that can be trained for text sequential on our dataset. LSTM can be slow trained and can be trained on GPU hardware. 

# **Part II:  Data Preparation** 

### B. 

1.  
 presence of unusual characters (e.g., emojis, non-English characters, etc.)
![[Pasted image 20210609024800.png]]
vocabulary size
![[Pasted image 20210609033315.png]]
- The word embedding proposed is 5000.
 - statistical justification for the chosen maximum sequence length
  - ![[Pasted image 20210609183100.png]]
  - We will choose a sequence of four. 
2.  Describe the goals of the tokenization process, including any code generated and packages that are used to normalize text during the tokenization process.
![[Pasted image 20210609183514.png]]
![[Pasted image 20210609183445.png]]
- The first to work with text is to split it into words. Each word is considered a token, and the process of splitting text into tokens is called tokenization. 
- ![[Pasted image 20210609184853.png]]
- ![[Pasted image 20210609184905.png]]
- ![[Pasted image 20210609184918.png]]
3. The padding occurs after the sequence for better accuracy.
![[Pasted image 20210609211317.png]]

4.  Identify how many sentiment categories will be used and an activation function for the final dense layer of the network.
  1.  two categories will be used for the sentiment column—one is for a good comment and zeroes for critical comment. 
  2.  ![[Pasted image 20210609212921.png]]
5.  Explain the steps used to prepare the data for analysis, including the size of the training, validation, and test set split.
	1.  ![[Pasted image 20210609213457.png]]
	2.  ![[Pasted image 20210609213358.png]]
	3.  The first step is to combine all text files into one data frame.
	4.  The second step is to make three different series for each column.
	5.  The third step is to separate train and test sentences, then separate the sentiment labels into training and testing.
		1.  The train labels and train sentences are 561 rows 
		2.  The test labels and test sentences are 187 rows 
      6. The final step is to vectorize each word and transform the sentences.

6.  Provide a copy of the prepared dataset.  
   ✅️

# **Part III:  Network Architecture** 

### C.  Describe the type of network used by doing the following:

1.  Provide the output of the model summary of the function from TensorFlow.
![[Pasted image 20210609220023.png]]
2.  Discuss the number of layers, the type of layers, and the total number of parameters.
 1. the layer types for both is dense.
 2. The first layer shape is (None, 10) with a total of 1010 parameters. 
 3. the second layer shape is (None, 1) with a total of 11 parameters.
 4. In this parameter, all parameters are trainable and 0 nontrainable parameters.


3.  Justify the choice of Hyperparameters, including the following elements:
1. Hyperparameters: 
	 1. Filters used for output space.
	 2. maxlen of 100 to maximize the length of each sequence and reduced the model amount of memory
	 3. embedding_dim - helps represent each word by a unique integer. 
	 4. The amount nodes is between the size of input layer and the size of the output layer. 
	 5. Early stopping is used to prevent overfitting 

1. I will use the sigmoid function for the output layer since the column we are trying to predict is binary.
2. I have a binary classification, so I will only use one node. 
3. The loss function I will use is the binary cross-entropy since the classification is binary. 
4. The optimizer I will use is the "Adam," which has good performance. The adam optimizer is easy to implement and requires little memory.
5.  Early stopping is being used to prevent overfitting. Early stopping will occurred when validation loss occurs or it stops improving 
	1.  ![[Pasted image 20210630211923.png]]
6.  •   evaluation metric : The evaluation metric is accuracy
![[Pasted image 20210630212657.png]]
![[Pasted image 20210609225858.png]]
![[Pasted image 20210609225956.png]]
![[Pasted image 20210609230632.png]]
# **Part IV:  Model Evaluation** 

### D.  Evaluate the model training process and its relevant outcomes by doing the following:
   **Per the report:  Discuss the impact of using stopping criteria instead of defining the number of epochs**
1. Using too many epochs can lead to overfitting of the training dataset, but the downsized of too few epochs can underfit models. In our model, we used 20 epochs. Stopping criteria stops the training once the model performance stops improving. Here we used few epochs, because I do not have the computer to run anymore. **per the report:  including a screenshot showing the final training epoch.** 
	1. ![[Pasted image 20210609230639.png]]
	2.  ![[Pasted image 20210609225956.png]] 
	3.  ![[Pasted image 20210609225858.png]]
2. ![[Pasted image 20210609231158.png]]
3.  Assess the fitness of the model and any measures taken to address overfitting.
	1.  To prevent overfitting, we minimize the use of too many parameters. 
	2.  To prevent overfitting, we used more rows on the training dataset and changed the complexity of the networks. 
4.  Discuss the predictive accuracy of the trained network.  
	1.  ![[Pasted image 20210609225858.png]]
	2.  Amazon comments dataset has an accuracy of 83%. With different tuning, we might increase accuracy, but it will require more time and memory. In addition, obtaining more comments will help the accuracy.
	4.  ![[Pasted image 20210609225956.png]]
	5.  The accuracy for the IMDB dataset is 81%. With different tuning, we might increase accuracy, but it will require more time and memory. In addition, obtaining more comments will help the accuracy.
	6.  ![[Pasted image 20210609230639.png]]
	7.  The best accuracy for the yelp comments dataset is 81%. With different tuning, we might increase accuracy, but it will require more time and memory. In addition, obtaining more comments will help the accuracy.
  

# **Part V:  Summary and Recommendations** 


### F.  FUNCTIONALITY 



### G.  
Based on the model we have created, we can see if comments coming in are positive or negative. We can categorize future comments with a confidence of 80%. This will give the company leaders an idea on how each product is doing. My recommendation is that we can use this model to see if the comments are positive or negative for existing or new product lunches.
  

# **Part VI: Reporting** 
 
  

### I.  List the web sources used to acquire data or segments of third-party code to support the application.  
https://realpython.com/python-keras-text-classification/#hyperparameters-optimization  

### J.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.  
  N/A
