# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Harry, Cheung Ho Hoi

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
We need to use the format of the submission report provided, and pass the output data to a CSV, and upload to the kaggle.

### What was the top ranked model that performed?
The top ranked model is WeightedEnsemble_L3

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I add the extra features by extracting the hour, day & month from the datatime 

### How much better did your model preform after adding additional features and why do you think that is?
The model's kaggle score improve from 1.79 to 0.67
The main reason is that there exist strong correlation between the hour, day & month with the target (Count), for example, we can observe an significantly high count during jan and dec.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The model's kaggle score improve from 0.47 to 0.49

### If you were given more time with this dataset, where do you think you would spend more time?
Probably the data augmentation, we can simulate more data for a larger training data size, also more on the data cleaning, for example the removing the outlier. 

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1 learning rate|hpo2 activation|hpo3 dropout activation|score|
|--|--|--|--|--|
|initial|1e-4|relu|0.0|1.79|
|add_features|1e-2|softrelu|0.5|0.67|
|hpo|5e-4|tanh|0.1|0.49|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
From this project, we can understand that model training is a continuous trial and error process, we should try different approach to improve the performance on the validation dataset, and the EDA can bring insights on how to improve the model. For example, we perform the feature extraction and the hyperparameter tuning to improve the model performance. 