# Sentiment Analysis for Amazon Fine Food Review
### Data Overview:

This dataset is in two kinds of format: csv and sqlite database. The Amazon Fine Food Reviews dataset consists of reviews of fine foods from Amazon. Number of reviews: 568,454 ; Number of users: 256,059 ; Number of products: 74,258 ; Timespan: Oct 1999 - Oct 2012 

Attribute Information:
     * Id ProductId - unique identifier for the product 
     * UserId - unqiue identifier for the user ProfileName 
     * HelpfulnessNumerator - number of users who found the review helpful 
     * HelpfulnessDenominator - number of users who indicated whether they found the review helpful or not 
     * Score - rating between 1 and 5 
     * Time - timestamp for the review 
     * Summary - brief summary of the review 
     * Text - text of the review

### Objective:

Given a review, determine whether the review is positive (Rating of 4 or 5) or negative (rating of 1 or 2).

### Methodology:

* Data Preprocessing: check missing values, remove duplicates, feature engineering(create a function to convert ratings of 4 or 5 to positive and ratings of 1 or 2 to negative. A review of 3 is nuetral and ignored)
* Visualization: use "wordcloud" to show both reviews with negative sentiment and reviews with postive sentiment
* Text Cleaning: convert to lowercase, remove HTML tags, retain only alphabets, remove punctuations and remove stopwords(Lemmatization)
* Word Embedding: use Word2Vec Embedding to check for similarities between two words, GloVe Embedding with CNN model, TF-IDF and N-grams for vectorization
* Topic Modeling: perform Latent Dirichlet Allocation (LDA) to classify text to a particular topic. 
* Data Modeling: Logistic Regression, SVM, Naive Bayes and Convolutional Neural Network (CNN) with Keras. Logistic Regression with N-grams and Convolutional Neural Network (CNN) with GloVe Embedding perform the best and they obtained 87.62% and 83.74% accuracy.
