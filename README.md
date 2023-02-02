
# Title of Project

## Bank Marketing Campaign


# Introduction
This project is aimed at analyzing a bank's marketing campaign data to determine the factors that influence customers to subscribe to a term deposit. The goal is to build a model that can accurately predict whether a customer will subscribe to a term deposit based on their characteristics and past marketing campaign interactions.



## Data 
The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed.

There are 45211 rows and 17 columns in data set

#### Columns description
- age - Age of the customer
- job - Profession of the customer
- marital - Marital status of the customer
- education - Educational qualification of the customer
- default - Does the customer have credit in default?
- balance - Average yearly balance
- housing - Does the customer have a housing loan?
- loan - Does the customer have a personal loan?
- contact - Contact communication type of the customer
- day - Last contact day of the month
- month - Last contact month of the year
- duration - Last contact duration in seconds
- campaign - Number of contacts during campaign
- pdays - Number of days since last contact
- previous - Number of contacts before campaign
- poutcome - Outcome of previous campaign
- y - Has the customer subscribed for a deposit?

The data set is downloaded from kaggle.


To downlad the data set you can refer to this link:-

https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset/code

## Prerequisites
The following packages and libraries are required to run this project:

- Python 3.x
- Pandas
- NumPy
- Sklearn
- Matplotlib
- Seaborn
- imbalanced-learn
## Task Done

- Problem Undertsatnding and Data Collection part are already Done 

### 1) EDA
- After reading the data set we have done Exploratory Data Analysis
- No null value is there in data set
- Done the statistical Analysis for numeical columns and categorical columns.
- Done some visulization by using different- different graphs like as bar plot,pie plot, boxplot, histogram, dist plot, heatmap etc. 

- After doing visualization we found that outliers are present in data set and Data set is highly unbalanced
- Checked the correlation also



 ### 2) Fetaure Engineering 
#### a) outliers
 - Remove the outliers using quantile method

#### b) One-Hot-Encoding
- Some columns are categorical in nature so we have done one hot encoding of these categorical features

#### c) Handle unbalance data
- To handle unbalance data we have two technique
-  1.--Undrsampling
-  2.--Over sampling
- But here we have used Over sampling techniques

#### c) Feature Scaling 

- Done feture scaling to scale the each feature inot same range.
- There are lot of outliers in data set so we have used Robust scaler for scaling the data

#### d) Feature selection
- Done feature selection to select the most important feaures that are taking participation in prediction
- We have used Recurssive Feature Elimination technique for numerical features to select important features
- For categorical features we have used filter method that is chi2 score 

### 3) Model Building 
-  We have already split the data into train and test data set
- Trained multiple models on training data set like logistic regresion, Decision Tree classifer, svc , Random forest classifier, XGBClassfier

### 4) Model Evaluation
- To evaluate the models multiple metrices are used like accuracy_score, cross validation score, classification report, recall, precission,f1_score, ROC-AUC curve
- Compared the performance of models on the basis of multiple metrices like recall, precision ,f1_score
- After evaluation we got XGBClassifier is giving the best best result.
 - So we finalize XGBClassifier as best performing model among other used models.

- Afte that we have done some hyperparameter tuning using random search cv.
- And we find significant incereasement in performance of model



## Conclusion

The bank marketing campaign project provides valuable insights into the factors that influence customer behavior and can be used to improve future marketing campaigns. The model developed in this project can be used to predict which customers are more likely to subscribe to a term deposit, allowing the bank to target its marketing efforts more effectively.
## Future work


- We can also apply deep learning algorithm.
- After testing we will deploy the model