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
- Our Data Quality Analysis (DQA) report identified that our dataset primarily consists of categorical variables with no missing values. Outliers were identified due to the binary nature of the columns, where values are either 0 or 1. Since the majority of values are 0, occurrences of 1 were flagged as outliers. However, this should not pose a problem for our model.
- Additionally, we removed irrelevant characters from the data, such as "a." and "b.", as they could affect our subsequent steps. We also encoded our data to ensure it could fit into our model.

## 3. Build Decision Tree Classifier Models
In this step, we split our data into training and test sets, separated labels and features, and fitted the data into our model.

## 4. Evaluate Decision Tree Performance
We measured the performance of our model using various metrics, including:
- Confusion Matrix
- Accuracy
- Recall
- Precision
- Classification Report

## 5. Tune Decision Tree Performance
We manually varied FOUR hyperparameters to find the best-performing tree with respect to accuracy. These hyperparameters include:
- Split Criteria: 'Entropy' or 'Gini Impurity'
- Maximum Features
- Minimum Sample Leaf
- Maximum Depth

## 6. Visualize Your Best Decision Tree using GraphViz
Using the top-performing hyperparameters identified in the previous step, we created our best performing tree. We then visualized the tree and evaluated its performance.

## 7. Conclusion
- **Q.4:** How long was your total run time to train the best model?  
  **A:** The run time for training the best model was 0.03 seconds.
- **Q.5:** Did you find the BEST TREE?  
  **A:** Yes, I did. By testing all hyperparameters, I identified the ones with the highest accuracy.
- **Q.6:** Write your observations from the visualization of the best tree  
  **A:** The tree contains numerous internal nodes, making it challenging to visualize effectively.
- **Q.7:** Will this Tree “overfit”? (Hint: Is this tree “fully grown”)  
  **A:** Yes, this tree is fully grown and likely to overfit.

## 8. Prediction using your “trained” Decision Tree Model
In this final step, we added a new row to the data to predict which class this new row/person would fall into according to our model. We created an original copy of the dataset, added the extra row, and ensured that the encoding and binning on the new data were identical to our trained data. After binning, we created a dataframe with this new row and predicted which class the person would fall into, along with its probability score.

## Acknowledgements
Dr. Brahma
