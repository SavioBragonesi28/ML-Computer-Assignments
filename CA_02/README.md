# CA02: This is a eMail Spam Classifers that uses Naive Bayes supervised machine learning algorithm. 

In this assignment you will ...
1. Complete the code such a way that it works correctly with this given parts of the program.
2. Explain as clearly as possible what each part of the code is doing. Use "Markdown" texts and code commenting to explain the code

## Part 1: Importing
The initial section involves importing necessary packages and libraries:
- `os` for file operations and OS interaction
- `numpy` as `np` for numerical operations
- `Counter` from `collections` for counting class instances
- `GaussianNB` from `sklearn.naive_bayes` for Gaussian Naive Bayes
- `accuracy_score` from `sklearn.metrics` for accuracy calculation
- `confusion_matrix` from `sklearn.metrics` (though not used)
- `train_test_split` from `sklearn.model_selection` for splitting data into training and testing sets

## Part 2: Pre-Processing and Creating a Dictionary
This section introduces a function that reads email files, tokenizes words, removes non-alphabetic and single-character words, and returns a list of the 3000 most common words and their frequencies. The process involves iterating through emails, creating a dictionary based on word frequency, and applying boolean conditions to filter unwanted words.

## Part 3: Processing, Feature Extraction and Building a Matrix
Here, another function uses the previously created dictionary. It iterates through email content, counting occurrences of words from the dictionary, and populating a matrix. Rows correspond to emails, and columns represent words. Spam emails (those containing "spmsg") are labeled as 1. This matrix serves as a numerical representation of email content for machine learning purposes.

## Part 4 Importing files and applying the fucntions to it
This segment involves importing training and test data, processing it through the created functions, and generating variables for model usage: `test_features_matrix`, `test_labels`, `features_matrix`, and `labels`. 
### For this part pay attention to the file path depending on your OS and if you are on Coolab or Jupyter 
- Linux('/') 
- Windows ('\\)


## Part 5 Model Training, Prediction, and Accuracy
The model is fitted using the `features_matrix` and `labels`. Subsequently, the trained model predicts labels for the `test_features_matrix`. The accuracy of the model is assessed by comparing predictions with actual labels in the `test_labels` dataset, employing the `accuracy_score` function.

