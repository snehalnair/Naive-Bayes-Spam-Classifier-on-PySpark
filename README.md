# Naive-Bayes-Spam-Classifier-on-PySpark
Spam detection is one of the major applications of Machine Learning in the interwebs today. Most of the email service providers have spam detection built in to automatically classify such mails as ‘Junk Mail’.


We will be working on dataset provided on UCI Machine Learning Respository. This dataset is a collection of 425 SMS spam messages manually extracted from the Grumbletext Web site. This is a UK forum in which cell phone users make public claims about SMS spam messages, most of them without reporting the very spam message received.

We will implement Naive Bayes classifier using pySpark ML packages. It is a classification technique based on Bayes’ theorm. Its called Naive since it assumes independence between predictors. There are a few advantages of using Naive Bayes for NLP over other classification algorithms:
- It can handle an extremely large number of features. NLP works with lots of features which are nothing but the unique words in our dataset.
- The other advantage is that relatively simple to implement and tune the model. We will look at the impact of hyperparameter tunning in the end of the project.
- Faster training time, since it assumes conditional independence, it helps to reduce complexity by 2n

1. Load data
We will first instantiate a spark session and load the data as spark dataframe. The data doesnt have header. Lets name the columns as label_string and sms.

2. Build pipeline stages
The data is in textual format we will want to do data preprocessing to prepare data for the model. The preprocessing will include stages:
- Strip strings of punctuations, normalise case, break the sentences into list words often referred to as tokens in NLP. All these steps can be done using RegexTokenizer
- Next we will use CountVectoriser to convert the collection of text documents to a vector of term/token counts
- Convert the string type label to numeric labels
- In the end we will assemble all the features into a vector using VectorAssembler. This step is required for any pySpark model.

3. Fit the pipeline to transform the data

4. Split dataset into train and test

5. Naive Bayes Implementation

6. Evaluate the model

In the end we will run hupertuning for smoothing parameter.
