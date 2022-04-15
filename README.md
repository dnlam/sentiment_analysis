# sentiment_analysis
 Linear Classifer with Perceptron/Perseus and Automative Review Analyzer 

 # Objective
 The goal of this project is to design a classifier to use for sentiment analysis of product reviews. Our training set consists of reviews written by Amazon customers for various food products. The reviews, originally given on a 5 point scale, have been adjusted to a +1 or -1 scale, representing a positive or negative review, respectively.

 In order to automatically analyze reviews, we will need to get through the following task:

 - Implement and compare three types of linear classifiers: the perceptron algorithm, the average perceptron algorithm, and the Pegasos algorithm.

 - Use your classifiers on the food review dataset, using some simple text features.

 - Experiment with additional features and explore their impact on classifier performance.


# Review Analyzer
## The Data

The data consists of several reviews, each of which has been labeled with -1 or +1 , corresponding to a negative or positive review, respectively. The original data has been split into several files:

- reviews_train.tsv (4000 examples)
- reviews_validation.tsv (500 examples)
- reviews_test.tsv (500 examples)

## Translating reviews to feature vectors

We will convert review texts into feature vectors using a bag of words approach. We start by compiling all the words that appear in a training set of reviews into a dictionary , thereby producing a list of <b>d</b> unique words.