# Employee Attrition Predictor

The Employee Attrition Predictor is a Jupyter Notebook project that predicts employee attrition based on various factors and variables, it uses a technique called "Iterative Sampling".

## Data

The data used in this project is publicly available on Kaggle: https://www.kaggle.com/competitions/playground-series-s3e3/. Please note that you will need to create a Kaggle account and accept the competition rules to access the data.

## Iterative Sampling

This technique was used by the team "Carbon Cutters" in the 2023 ie Sustainability Datathon. Its name is iterative sampling.

The aim of the approach is to mitigate the impact of imbalanced classes by creating a training set that contains an equal number of samples from the majority class and the minority class. To achieve this, the approach randomly selects a subset of the majority class that is equivalent in size to the minority class. The following steps outline how the code executes this approach:

1. The size of the minority class is determined by calculating the length of the ones variable, which is used as a reference to set the desired size of each training set.
2. A copy of the training data that contains only samples from the minority class is created and stored in the model_zeros variable.
3. A dataframe is created to hold the predictions generated by the classifier both for kaggle and validation.
4. A loop is initialized to run until the zeros dataset has less elements than the ones dataset.
5. GridSearchCV + Training + Scoring + Predicting is performed
6. The loop starts again.
7. The final mean ROC AUC score is calculated by averaging the ROC AUC scores generated from all the iterations.

## Usage

The notebook contains detailed explanations and code to help you understand how to use the predictor to predict employee attrition based on the input data. Simply run the notebook and follow the instructions provided.
