# Quantum-task-3: Regression on the tabular data

## Task description
You have a dataset (internship_train.csv) that contains 53 anonymized features and a target column. Your task is to build model that predicts a target based on the proposed features. Please provide predictions for internship_hidden_test.csv file. Target metric is RMSE. The main goal is to provide github repository that contains:
- jupyter notebook with analysis; 
-	code for modeling (Python 3); 
-	file with model predictions; 
-	readme file;
-	requirements.txt file.


## File overview
Both analysys and modelling is done in quantum_task_3.ipynb notebook file.
Because I was working in Google Colab the requirements.txt file might contain some addittional packages, however I tried to get it as smal as I can.
_hidden_test_with_predictions.csv_ is a copy of _internship_hidden_test.csv_ with the additional column with predictions (at the very end).

## Solution
I decided to use random forest regressor, because it's often a good starting point for many tabular data problems.
Because there was no missing data and only numerical values were present I decided to train a simple model right away.
I used a random forest with 100 estimators and 80/20% train/test split.

This led to RMSE error of: _7.226429057194979e-06_.

Because the results seem quite good I didn't do any further finetuning.
To finetune the model we could for example use [GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html) or RandomSearchCV to seach through different model paramenters and pick RMSE as a target score.

![image](https://user-images.githubusercontent.com/13591149/189418584-d93c04c3-5ae1-4f9d-86f5-c3ec38067057.png)
