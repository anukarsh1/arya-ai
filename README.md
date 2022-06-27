# Aim: Binary Classification of the given sample data
## Files Submitted
* EDA + Preprocessing + Performance on Training and Test Data
* Predictions of the model on Test Data
* Requirements.txt

## General Approach To the Assignment

Training Data --> (3910,57)

Test Data --> (691,57)

Task: Perform Data Preprocessing, Exploratory Data Analysit, rain a  ML model on the training dataset, and perform predictions on the test dataset.

### Exploratory Data Analysis(EDA)+Preprocessing

* Data has 57 features
* Y label is binary in nature, hence binary classification needs to be performed.
* There is no major class imbalance issue here, as the labels are almost equally distributed in the two classes. So we need not need to use metrics like F1 score here.
* We have no missing values anywhere in the dataset. Hence no need to do anything extra here.
* The distribution of all the features are highly skewed.
* Data is highly sparse, as most of the values are 0
* All the features in our dataset are continuous
* Here I have used mutual information as the measure of feature importance. I calculated the mutual information of each feature and ranked them w.r.t. the target variable. 26 features were finally shortlisted as the important features.

### Training our model + Performance on the test data

* Since we have binary values in our class labels, so we can choose Binary Cross Entropy here.
* Models tried: Random Binomial Model, Logistic Regression, Decision Tree, Random Forest, XgBoost
* The Xgboost have the least gap between the train and test logloss.
* And Xgboost has least logloss for test data. So we choose XgBoost as our classifier here.(AUC Score = 0.982 on the validation set)
* Logistic Regression and Random Model acts as good baseline models to start with.


