# CA02: This is a eMail Spam Classifers that uses Naive Bayes supervised machine learning algorithm. 

In this assignment you will ...
1. Complete the code such a way that it works correctly with this given parts of the program.
2. Explain as clearly as possible what each part of the code is doing. Use "Markdown" texts and code commenting to explain the code

# Part 1: Importing
In the fisrt part of the code we import the packages and libraries we will
import os for file operations and OS interaction
import numpy as np for numerical operations
from collections import Counter  for counting the number of instances of each class
from sklearn.naive_bayes import GaussianNB for Gaussian Naive Bayes
from sklearn.metrics import accuracy_score for accuracy calculation
from sklearn.metrics import confusion_matrix did not use it
from sklearn.model_selection import train_test_split for splitting the data into training and testing sets

# Part 2: Pre-Processing and Creating a Dictionary
In this part we created a function that reads all the email files tokenizes the words,removes non-alphabetic and single-character words, 
and returns a list of the most common 3000 words, and their frequencies. The process is done by looping through all emails, spliting the words,
creating a dictionary based on the frequency of each word. Then using boolean coditioning we created a list to remove non-alphabetical words, and  wrods containing 
len equal 1. To finalize the function returns a dictionary with the 3000 most common words.

# Part 3: Processing, Feature Extraction and Building a Matrix
In this function we will use the dictionary created previoulsy. We are gonna use a for loop to iterate over the content of each email, counting the occurrences 
of words from the dictionary. The counts will then populate the 3000 columns of a matrix, where the rows correspond to the emails and the columns each word of our 
dictionary. Then we will check the emails that are spam ( contains "spsmg") and label it as 1. In the end this matrix will be able to provide numerical
representation to the emails based on its content, and will also allow us to use it for ML purposes. 

# Part 4 Importing files and applying the fucntions to it
This part is very simple we pretty much import our training and test data, proccess it through the functions we created, and create the variables we will be using
for our model. Functions created : test_features_matrix, test_labels, features_matrix, labels.

# Part 5 
Fisrt we fit our model into the features_matrix and lables. We then use this trained model to predcit the lables for the dataset test_features_matrix.
To finalized we use the accuracy function to compare the predictions with the actual labels in the test dataset test_labels, and get the accuracy of our model.

