# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
We got good performance on Weighted Ensemble with the score of -52.69, but we could improve it by tunning hyperparameters and creating new features.
### What was the top ranked model that performed?
Weighted Ensemble
## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
That we had categorical data on the features season and weather. Another improvement was adding the year, month and day from the datetime column
### How much better did your model preform after adding additional features and why do you think that is?
Our best model got an score_val of -52.66, I think it was by transforming the features season and weather to categorical.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The LightGBM model got an score_val of -133.575981.
### If you were given more time with this dataset, where do you think you would spend more time?
I would run a cluster model and after creating a regression model to each cluster to evaluate the performance. 

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|default|default|default|52.720195|
|add_features|default|default|default|52.72060|
|hpo|CAT_iterations|'CAT_learning_rate'| 'GBM_num_boost_round'|130.310568|

### Create a line plot showing the top model score for the three (or more) training runs during the project.


![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score.png](img/model_test_score.png)

## Summary
Bike-sharing demand is highly relevant to related problems companies encounter, such as Uber, Lyft, and DoorDash. Predicting demand not only helps businesses prepare for spikes in their services but also improves customer experience by limiting delays.

In this project, we'll use the AutoGluon library to train several models for the Bike Sharing Demand competition in Kaggle. You will be using Tabular Prediction to fit data from CSV files provided by the competition.

