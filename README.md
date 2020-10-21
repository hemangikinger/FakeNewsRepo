### What is Fake News?

A type of yellow journalism, fake news encapsulates pieces of news that may be hoaxes and is generally spread through social media and other online media. This is often done to further or impose certain ideas and is often achieved with political agendas. Such news items may contain false and/or exaggerated claims, and may end up being viralized by algorithms, and users may end up in a filter bubble.

### What is a TfidfVectorizer?

**TF (Term Frequency):** The number of times a word appears in a document is its Term Frequency. A higher value means a term appears more often than others, and so, the document is a good match when the term is part of the search terms.

**IDF (Inverse Document Frequency):** Words that occur many times a document, but also occur many times in many others, may be irrelevant. IDF is a measure of how significant a term is in the entire corpus.

The TfidfVectorizer converts a collection of raw documents into a matrix of TF-IDF features.

### What is a PassiveAggressiveClassifier?

Passive Aggressive algorithms are online learning algorithms. Such an algorithm remains passive for a correct classification outcome, and turns aggressive in the event of a miscalculation, updating and adjusting. Unlike most other algorithms, it does not converge. Its purpose is to make updates that correct the loss, causing very little change in the norm of the weight vector.

### Detecting Fake News with Python – Objective

To build a model to accurately classify a piece of news as REAL or FAKE.

### Detecting Fake News with Python – About the Python Project

This advanced python project of detecting fake news deals with fake and real news. Using sklearn, we build a TfidfVectorizer on our dataset. Then, we initialize a PassiveAggressive Classifier and fit the model. In the end, the accuracy score and the confusion matrix tell us how well our model fares.

### The Dataset

The dataset we’ll use for this python project- we’ll call it news.csv. This dataset has a shape of 7796×4. The first column identifies the news, the second and third are the title and text, and the fourth column has labels denoting whether the news is REAL or FAKE.

### Advanced Python Project – Prerequisites

You’ll need to install the following libraries with pip:

You’ll need to install Jupyter Lab to run your code. Get to your command prompt and run the following command:

You’ll see a new browser window open up; create a new console and use it to run your code. To run multiple lines of code at once, press Shift+Enter.

### Steps for detecting fake news with Python

Follow the below steps for detecting fake news and complete your first advanced Python Project –

1. Make necessary imports:

![Imports Screenshot](https://github.com/hemangikinger/FakeNewsRepo/blob/master/python-projects-imports-data_LI.jpg?raw=true)

2. Now, let’s read the data into a DataFrame, and get the shape of the data and the first 5 records.

![Read Data Screenshot](https://github.com/hemangikinger/FakeNewsRepo/blob/master/python-projects-read-data_LI.jpg?raw=true)

3. And get the labels from the DataFrame.

![Get Labels Screenshot](https://github.com/hemangikinger/FakeNewsRepo/blob/master/python-projects-get-labels-_LI.jpg)

4. Split the dataset into training and testing sets

![Split dataset Screenshot](https://github.com/hemangikinger/FakeNewsRepo/blob/master/split-dataset-in-python-projects_LI.jpg)

5. Let’s initialize a TfidfVectorizer with stop words from the English language and a maximum document frequency of 0.7 (terms with a higher document frequency will be discarded). Stop words are the most common words in a language that are to be filtered out before processing the natural language data. And a TfidfVectorizer turns a collection of raw documents into a matrix of TF-IDF features.

Now, fit and transform the vectorizer on the train set, and transform the vectorizer on the test set.

![TfidfVectorizer Screenshot](https://github.com/hemangikinger/FakeNewsRepo/blob/master/python-projects-tfidf_LI.jpg)

6. Next, we’ll initialize a PassiveAggressiveClassifier. This is. We’ll fit this on tfidf_train and y_train.

Then, we’ll predict on the test set from the TfidfVectorizer and calculate the accuracy with accuracy_score() from sklearn.metrics.

![PassiveAggressiveClassifier Screenshot](https://github.com/hemangikinger/FakeNewsRepo/blob/master/passive-aggressive-calssifier-in-python-projects_LI.jpg)

7. We got an accuracy of 92.82% with this model. Finally, let’s print out a confusion matrix to gain insight into the number of false and true negatives and positives.

![confusion matrix Screenshot](https://github.com/hemangikinger/FakeNewsRepo/blob/master/confusion-matrix-python-projects_LI.jpg)

So with this model, we have 589 true positives, 587 true negatives, 42 false positives, and 49 false negatives.

## Summary

Today, we learned to detect fake news with Python. We took a political dataset, implemented a TfidfVectorizer, initialized a PassiveAggressiveClassifier, and fit our model. We ended up obtaining an accuracy of 92.82% in magnitude.







