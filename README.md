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


We can then transform each of the reviews into a feature vector of length d by setting the i-th coordinate of the feature vector to 1 if the i-th  word in the dictionary appears in the review, or 0 otherwise. For instance, consider two simple documents “Mary loves apples" and “Red apples". In this case, the dictionary is the set {Mary; loves;apples;red}, and the documents are represented as (1;1;1;0) and {0;0;1;1}.

A bag of words model can be easily expanded to include phrases of length m. A unigram model is the case for which m=1. In the example, the unigram dictionary would be {Mary;loves;apples;red}. In the bigram case, m=2, the dictionary is {Mary loves; loves apples; Red apples}, and representations for each sample are {1;1;0, {0;0;1}}. In this section, you will only use the unigram word features. These functions are already implemented for you in the bag of words function.

# Python preliminaries
In ```util.py```:
- ```load data ``` function which can be used to read the .tsv files and returns the labels and texts
- ```bag_of_words``` function is supplied in project1.py, which takes the raw data and returns dictionary of unigram words
- ```extract_bow_feature_vectors ```  computes a feature matrix of ones and zeros that can be used as the input for the classification algorithms