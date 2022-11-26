# Spam-or-Ham-Classification
Spam or Ham Classification using Navie Bayes Algorithm 

A little introduction
-------------------------
These Informations are Gathered from Different Sources:- Spam Email , become a big trouble over the internet. Spam is waste of time, storage space and communication bandwidth. The problem of spam e-mail has been increasing for years. In recent statistics, 40% of all emails are spam which about 15.4 billion email per day and that cost internet users about $355 million per year Knowledge engineering and machine learning are the two general approaches used in e-mail filtering In knowledge engineering approach a set of rules has to be specified according to which emails are categorized as spam or ham. Machine learning approach is more efficient than knowledge engineering approach; it does not require specifying any rules . Instead, a set of training samples, these samples is a set of pre classified e-mail messages. A specific algorithm is then used to learn the classification rules from these e-mail messages. Machine learning approach has been widely studied and there are lots of algorithms can be used in e-mail filtering. They include Naive Bayes, support vector machines, Neural Networks, K-nearest neighbour, Rough sets and the artificial immune system. 

# What is Naive Bayes algorithm?
----------------------------------
It is a classification technique based on Bayes’ Theorem with an assumption of independence among predictors. In simple terms, a Naive Bayes classifier assumes that the presence of a particular feature in a class is unrelated to the presence of any other feature.
For example, a fruit may be considered to be an apple if it is red, round, and about 3 inches in diameter. Even if these features depend on each other or upon the existence of the other features, all of these properties independently contribute to the probability that this fruit is an apple and that is why it is known as ‘Naive’.

How it is Work ?

Naive Bayes model is easy to build and particularly useful for very large data sets. Along with simplicity, Naive Bayes is known to outperform even highly sophisticated classification methods. Bayes theorem provides a way of calculating posterior probability P(c|x) from P(c), P(x) and P(x|c). Look at the equation below: Above,

P(c|x) is the posterior probability of class (c, target) given predictor (x, attributes).
P(c) is the prior probability of class.
P(x|c) is the likelihood which is the probability of predictor given class.
P(x) is the prior probability of predictor.

P(c|x)=(P(x|c)P(c))|P(x)

![1_2Ixe8hsTASXjMXt9TySHGA](https://user-images.githubusercontent.com/67859800/204078247-e62f4754-68cd-48b8-90b6-c30e870676ab.png)

Bag of Words Approach
------------------------
What we have here in our data set is a large collection of text data (5,572 rows of data). Most ML algorithms rely on numerical data to be fed into them as input, and email/sms messages are usually text heavy. We need a way to represent text data for machine learning algorithm and the bag-of-words model helps us to achieve that task. It is a way of extracting features from the text for use in machine learning algorithms. In this approach, we use the tokenized words for each observation and find out the frequency of each token. Using a process which we will go through now, we can convert a collection of documents to a matrix, with each document being a row and each word(token) being the column, and the corresponding (row,column) values being the frequency of occurrence of each word or token in that document.

For example:
Lets say we have 4 documents as follows:
['Hello, how are you!', 'Win money, win from home.', 'Call me now', 'Hello, Call you tomorrow?']
Our objective here is to convert this set of text to a frequency distribution matrix, as follows:

<img width="528" alt="countvectorizer" src="https://user-images.githubusercontent.com/67859800/204078226-7b0dad90-93ce-4b89-9a0b-554cd54f7651.png">

Here as we can see, the documents are numbered in the rows, and each word is a column name, with the corresponding value being the frequency of that word in the document.

Lets break this down and see how we can do this conversion using a small set of documents.

To handle this, we will be using sklearns count vectorizer method which does the following:

It tokenizes the string(separates the string into individual words) and gives an integer ID to each token. It counts the occurrence of each of those tokens.
