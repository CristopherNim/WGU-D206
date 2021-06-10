# **Part I:  Research Question** ✅️

### A.  Describe the purpose of this data analysis by doing the following:

1.  Summarize **one** research question that you will answer using neural network models and NLP techniques. Be sure the research question is relevant to a real-world organizational situation and sentiment analysis captured in your chosen dataset.
	1.  The leaders of the company want to know how comments affect the sales of the products.
2.  Define the objectives or goals of the data analysis. Be sure the objectives or goals are reasonable within the scope of the research question and are represented in the available data.
	1. The goals of the data analysis is to create model with an accuracy of 70%
3.  Identify a type of neural network capable of performing a text classification task that can be trained to produce useful predictions on text sequences on the selected data set.  
	1. Keras is a tool for constructing neural networks framework based on tensorflow. Keras an be used for text classification tasks and can be trained for useful predictions on text sequences.
  

# **Part II:  Data Preparation** ✅️

### B.  Summarize the data cleaning process by doing the following:

1.  Perform exploratory data analysis on the chosen dataset, and include an explanation of each of the following elements:

•   presence of unusual characters (e.g., emojis, non-English characters, etc.)
![[Pasted image 20210609024800.png]]
•   vocabulary size
![[Pasted image 20210609033315.png]]
•   proposed word embedding length
  - The word embedding proposed is 5000.
•   statistical justification for the chosen maximum sequence length
  - ![[Pasted image 20210609183100.png]]
  - We will choose a sequence of four. 
2.  Describe the goals of the tokenization process, including any code generated and packages that are used to normalize text during the tokenization process.
![[Pasted image 20210609183514.png]]
![[Pasted image 20210609183445.png]]
- The first to working with text is to split into words. each word is consider a token and the process of splitting text into tokens is called tokenization. 
- ![[Pasted image 20210609184853.png]]
- ![[Pasted image 20210609184905.png]]
- ![[Pasted image 20210609184918.png]]
3.  Explain the padding process used to standardize the length of sequences, including the following in your explanation:
  - The padding occurs after the sequence for better accuracy
![[Pasted image 20210609211317.png]]


4.  Identify how many categories of sentiment will be used and an activation function for the final dense layer of the network.
  1.  two categories will be used for the sentiment column. One being for a good comment and zero for a bad comment. 
  2.  ![[Pasted image 20210609212921.png]]
5.  Explain the steps used to prepare the data for analysis, including the size of the training, validation, and test set split.
	1.  ![[Pasted image 20210609213457.png]]
	2.  ![[Pasted image 20210609213358.png]]
	3.  The first step is to combined all txt files into one dataframe.
	4.  The second step is to make three difference series for each column.
	5.  The third step is to separate train and test sentence, then separate the sentiment labels into training and testing.
		1.  The train labels and train sentences are 561 rows 
		2.  The test labels and test sentences are 187 rows 
      6. The final step is to vectorize each word and transform the sentences.

6.  Provide a copy of the prepared dataset.  
   ✅️

# **Part III:  Network Architecture**

### C.  Describe the type of network used by doing the following:

1.  Provide the output of the model summary of the function from TensorFlow.
![[Pasted image 20210609220023.png]]
2.  Discuss the number of layers, the type of layers, and total number of parameters.
 1. the layer types for both is dense.
 2. The first layer shape is (None, 10) with a total of 1010 parameters. 
 3. the second layer  shape is (None, 1) with a total of 11 parameters.
 4. In this parameter all parameters are trainable and 0 non trainable parameters.


3.  Justify the choice of Hyperparameters, including the following elements:
1. Hyperparameters: 
	 1. Filters used for output space.
	 2. maxlen of 100 to maximize the length of each sequence and reduced the model amount of memory
	 3. embedding_dim - helps represent each word by a unique integer. 

1. I will use the sigmoid function for the output layer since the column we are trying to predict is binary.
2. I have a binary classification so I will only used one node. 
3. The loss function I will use is the binary cross entropy since the classification is binary. 
4. The optimizer I will use is the "Adam" that has good performance. The adam optimizer is easy to implement and requires little memory.
5.  We are not using a stopping criteria. 
•   evaluation metric :
![[Pasted image 20210609225858.png]]
![[Pasted image 20210609225956.png]]
![[Pasted image 20210609230632.png]]
# **Part IV:  Model Evaluation**

### D.  Evaluate the model training process and its relevant outcomes by doing the following:

1. Using too many epochs can lead to overfitting of the training dataset, but the downsized of too few epochs can underfit models. In our model we used 20 epochs. stopping criteria stops the training once the model performance stops improving. 
2.  Provide visualizations of the model’s training process, including a line graph of the loss and chosen evaluation metric.

3.  Assess the fitness of the model and any measures taken to address overfitting.
	1.  To prevent overfitting we minimize the use of too many parameters. 
	2.  To prevent overfitting we used more rows on the training dataset and change the complexity of the networks. 
4.  Discuss the predictive accuracy of the trained network.  
	1.  ![[Pasted image 20210609225858.png]]
	2.  Amazon comments dataset has an accuracy of 83%. With different tuining we might be able to increase to accuracy, but it will require more time and memory. In addition, obtaining more comments will help the accuracy.
	4.  ![[Pasted image 20210609225956.png]]
	5.  The accuracy for IMDB dataset is 81%. With different tuining we might be able to increase to accuracy, but it will require more time and memory. In addition, obtaining more comments will help the accuracy.
	6.  ![[Pasted image 20210609230639.png]]
	7.  The best accuracy for yelp comments dataset is 81%. With different tuining we might be able to increase to accuracy, but it will require more time and memory. In addition, obtaining more comments will help the accuracy.
  

# **Part V:  Summary and Recommendations**

### E.  Provide the code used to save the trained network within the neural network.  

### F.  Discuss the functionality of your neural network, including the impact of the network architecture.  

### G.  Recommend a course of action based on your results.

  

# **Part VI: Reporting**

### H.  Create your neural network using an industry-relevant interactive development environment (e.g., an R Markdown document, a Jupyter Notebook, etc.). Include a PDF or HTML document of your executed notebook presentation.  
  

### I.  List the web sources used to acquire data or segments of third-party code to support the application.  
  

### J.  Acknowledge sources, using in-text citations and references, for content that is quoted, paraphrased, or summarized.  
  

### K.  Demonstrate professional communication in the content and presentation of your submission.