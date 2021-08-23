# Classification on restaurant reviews using NLP
Hello. In this kernel, I'll be performing sentiment analysis on restaurant reviews using the Natural Language process. 

The questions that arise for this analysis are:

1. What is Natural Language Processing?
-Natural Language Processing, shortened as NLP, is a branch of artificial intelligence that deals with the interaction between computers and humans using the natural language. The ultimate objective of NLP is to read, decipher, understand, and make sense of human languages in a practical manner.

2. What is sentiment analysis?
As the name implies, Sentiment Analysis is the process of determining a person's point of view or feeling in a given situation. It simply means analysing and determining the emotion or intent behind a text, voice, or another form of communication.

3. Why does a restaurant need a sentiment analysis on their customer reviews? what is the importance?
- A restaurant receives thousands of reviews every day. Reviews are the reflection of product and service satisfaction for the restaurants to notify. Reviews can be positive, negative and even neutral. By looking at the reviews, the restaurant management can conclude where they need to focus on improving and who they need to promote for continuously improved sales. Basically, this gives an overview of their existence. 

# Objective
-To perform sentiment analysis on the restaurant reviews and check the accuracy of the reviews predicted by the NB classifier.
-To provide directive answers for the given new reviews as positive or negative reviews by machine

# About the dataset
This dataset contains 1000 reviews with two columns, whereby the first column will be the reviews, and the second column would be the categorization of the review as 1=POSITIVE and 0=NEGATIVE.

![rr](https://user-images.githubusercontent.com/87844891/130389644-197ad36d-ea8e-4f7d-9210-bb4343c03b04.png)

# Data exploration and visulization
There are 500 positive and 500 negative reviews
![newplot](https://user-images.githubusercontent.com/87844891/130390024-21d817f3-95e7-43e4-a57a-55c7081df160.png)

Next,I created a Word Cloud. It is a data visualization technique used to depict text in such a way that, the more frequent words appear enlarged as compared to less frequent words. This gives us a little insight into, how the data looks after being processed through all the steps until now.

for POSITIVE REVIEWS
![image](https://user-images.githubusercontent.com/87844891/130390186-6e44b311-30c1-4b8e-ad8c-60da98b746ed.png)

for NEGATIVE REVIEWS
![image](https://user-images.githubusercontent.com/87844891/130390221-73a1cfc7-1901-4d2e-8d1c-b1986372b516.png)

# Data cleaning for Bag of Words
RE is imported to pre-process the strings as per the given regular expression
nltk is imported as it is a Natural Language Toolkit with collection of libraries for natural language processing
stopwords is called to eliminate a collection of words that don’t provide any meaning to a sentence

# Bag of Words
Now I'll utilise the Bag of Words Model (BOW), which is used to represent text in the form of a bag of words, i.e., syntax and the order of words in a phrase aren't as important as multiplicity, i.e. (the number of times a word appears in a document). It basically describes the total number of times a term appears in a document. 

# Data transformation for modelling 
Here, I used CountVectorizer from Scikit-Learn for a neat way of performing the bag of words technique. Now, I have converted the text data into vectors, by fitting and transforming the corpus that I have created. Followed by assingning the x and y variables for train(80%) and test(20%) splitting.

# Modelling
For the machine learning part of this project, I've used the NB classifier to train the dataset and then to predict with the test dataset. Once the model training on the train dataset is done, the predicting analysis using the test dataset is performed. 

# Model Evaluation
I've evaluated my model with metrics such as confusion matrix and accurcy score.

![image](https://user-images.githubusercontent.com/87844891/130455370-25ea5e1d-c5d8-4f7e-a16f-8789fb829553.png)
With the test dataset (20% of the test data), the NB classifier was able to detect 55 correct prediction (true negative) for the negative reviews and 42 wrong prediction (true positive), whereas for predicting the positive reviews there was 12 false negative and 91 true positives.

The model gave us 73% accuracy score for the model.

# Predict for custom output
Use our model to predict if the following review:

"I love this restaurant so much"

is positive or negative.

and 

"I hate this restaurant so much"

is positive or negative.

- I obtained 1(positive) for the first review and 0(negative) for the second review. The model have correctly classified the following reviews.

