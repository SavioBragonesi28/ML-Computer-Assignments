# CA04 – Ensemble Models

## 1. Data Source and Contents

The dataset is obtained from the Census Bureau and represents salaries of people along with seven demographic variables. The following is a description of our dataset:

- Number of target classes: 2 ('>50K' and '<=50K') [Labels: 1, 0]
- Number of attributes (Columns): 7
- Number of instances (Rows): 48,842

Use the following exact “path” in your code as the data source: [Census Data](https://github.com/ArinB/MSBA-CA-03-Decision-Trees/blob/master/census_data.csv?raw=true)

Training and Test Data: There is a column indicating the rows to be used as “Training Data” and “Testing Data”. You can programmatically create your Training and Testing datasets as separate dataframes in your code based on this column value. In this part, we utilized all the cleaning and transformation from CA03, since we are using the same dataset.

## 2. Finding Optimal Value of a key Ensemble Method Hyper-parameter

For this part, we only used max depth from Decision Tree classifier to exemplify how we would find the optimal number of estimators later on our project. The code used here was adapted and re-utilized for the rest of the activity.

## 3. Building a Random Forest Model

Using an adapted version of the code from the previous step we build a random forest model and calculated its accuracy and AUC based on a range of estimators, to define what would be the optimal estimator.

## 4. Building AdaBoost, Gradient Boost, and XGB.

We repeated the last step, but for different classifiers this time.

## 5. Compare Performance

On the last step, we created a table to compare the performance of each classifier based on their best performance based on the number of estimators.

## 6. Findings 

### Random Forest:
1. **Observations about the Classifier’s behavior with respect to the number of estimators:** Both metrics reach their peak performance significantly early, followed by a sharp drop in performance with the next increase in estimators. However, performance remains unchanged as we further increase the number of estimators, indicating that we have found an optimal estimator.
2. **Optimal value of the estimator within the given range:** Yes, with 200 estimators, we achieve the best trade-off between AUC and accuracy.

### Gradient Boost:
1. **Observations about the Classifier’s behavior with respect to the number of estimators:** Both metrics start off with poor performance at 50 estimators but show significant improvement after reaching 100. However, accuracy experiences a sharp decline after 150, while AUC remains relatively stable with minor fluctuations.
2. **Optimal value of the estimator within the given range:** Yes, 150. After 150 estimators, we observe a significant decrease in accuracy, while AUC remains stable.

### AdaBoost:
1. **Observations about the Classifier’s behavior with respect to the number of estimators:** Both metrics reach their peak performance significantly early, followed by a sharp drop in performance with the next increase in estimators. However, performance remains unchanged as we further increase the number of estimators, indicating that we have found an optimal estimator.
2. **Optimal value of the estimator within the given range:** Yes, with 200 estimators, we achieve the best trade-off between AUC and accuracy.

### XGB:
1. **Observations about the Classifier’s behavior with respect to the number of estimators:** Both metrics exhibit almost identical plots, with performance peaking initially with fewer estimators and then gradually declining.
2. **Optimal value of the estimator within the given range:** Yes, at 50 estimators, both AUC and accuracy reach their peak.

## Acknowledgments:
- Professor Brahma
- Team 07

