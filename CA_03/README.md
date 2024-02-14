# CA03 – Decision Tree Algorithm

## 1. Data Source and Contents
The dataset is obtained from the Census Bureau and represents salaries of people along
with seven demographic variables. The following is a description of our dataset:
- Number of target classes: 2 ('>50K' and '<=50K') [ Labels: 1, 0 ]
- Number of attributes (Columns): 7
- Number of instances (Rows): 48,842
#### Data Source:
Use the following exact “path” in your code as the data source:
"https://github.com/ArinB/MSBA-CA-03-Decision-Trees/blob/master/census_data.csv?raw=true"

### Q.1 Why does it makes sense to discretize columns for this problem?
- Discretizing columns makes sense because the information is technically already "binned", it helps mitigate outliers, and categorical values help produce a more accuarate Decision Tree
### Q.2 What might be the issues (if any) if we DID NOT discretize the columns.
- If we do not clean and discretize our columns, our model will struggle to interpret the data and may create overly complex and inaccurate trees.

## 2. Data Quality Analysis (DQA)
- For this part we did the Data Quality report that identified Our dataset primarily consists of categorical variables, with no missing values.Regarding outliers, they were identified due to the nature of the columns, where values are either 0 or 1. Since the majority of values are 0, occurrences of 1 were flagged as outliers. However, this should not pose a problem for our model.
- Then we removed irrelevant characters in the data, like ("a.","b.") as it will affect our next step, and encoded our data, so it could fit into our model.

## 3. Build Decision Tree Classifier Models
For this step we splitted the our data into training and test, separeted labels and features and fitted the data into the our model.

## 4. Evaluate Decision Tree Performance
For this step we measured the performance of our model with the following:
- Confusion Matrix
- Accuracy
- Recall
- Precision
- Classification Report

## 5. Tune Decision Tree Performance
For this step we tried varying FOUR of the hyperparameters manually,train, and score the model for each set of these hyperparameters.The goal was to determine the hyper-parameter values for the “best-performing” tree with respect to “accuracy”

#### Hyperparameters to vary: 
- Split Criteria – ‘Entropy’ or ‘Gini Impurity’ 
- Maximum Features 
- Minimum Sample Leaf 
- Maximum Depth

## 6. Visualize Your Best Decision Tree using GraphViz
For this step we used the top performing Hyperparameters found in the last step, to create our Best performing tree. Following this we visualized the tree and measured its performance.

## 7. Conclusion
- Q.4 How long was your total run time to train the best model?
Best Model Run time: 0.03 seconds
- Q.5 Did you find the BEST TREE?
Yes, I did. Following the provided instructions, I tested all hyperparameters and identified the ones with the highest accuracy
- Q.6 Write your observations from the visualization of the best tree
The tree contains numerous internal nodes, making it challenging to visualize effectively.
- Q.7 Will this Tree “overfit”? (Hint: Is this tree “fully grown”)
Yes, this tree is fully grown and likely to overfit.

## 8. Prediction using your “trained” Decision Tree Model
This was the last step of our program. In this step we added a new row to the data with the goal of predicting which class this new row/person would fall into according to our model.
First I created an original copy of the dataset, than added the extra row, so whenever I encode the binninng on the new data would be identical as my trained data. After binning, I created a dataframe with this new row, and predicted which class the person would fall within, plus it probablity score.

## Acknowledgemnts
Dr. Brahma
