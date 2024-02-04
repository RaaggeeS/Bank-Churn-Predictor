# Bank-Churn-Dataset
Task: Predict whether a customer continues with their account or closes it (eg.churns).
Notebook Link: https://www.kaggle.com/code/raaggeesingh/playground-series-s4-ep1

## 1. What is nature of the dataset?
The dataset consisted of features which intrpret whether a customer exited or continue with their account.

## 2. What do the column describe?
-CustomerID - ID of customer
-Surname - Surname of the customer
-CreditScore - Represents the credit score
-Geography - Country where the customer resides
-Gender - Male or Female
-Age - Age of the customer
-Tenure - Customer's tenure with the bank
-Balance - Customer's balance
-NumOfProducts - Number of products opted by customer for the bank
-HasCrCard - Whether a customer has a credit card
-IsActiveMember - Whether a customer is active user of bank
-EstimatedSalary - Estimated Salary of the Customer
-Exited - Depicts if the person still with bank or not.

## 3. What approach we followed here?
a. Data Preprocessing:
- Checked the null values in dataset
- Checked the dtypes
- Described the whole dataset
- Checked the number of unique values

 b. Feature Engineering: Introduced three new variables
 - Bal_to_Sal_Ratio - Balance to Salary Ratio.
 - Age_balance - Age and Balance interation terms
 - Balance_and_Product - Combined effect of Balance and Number of Product

c. EDA:
- Plotting the relevant columns to get sour of countries, credit score and EstimatedSalary.
- Also checked the bivariate feature relevance using heatmap.

d. Machine Learning: 
- Before running any ML model, first converted all the categorical to numerical.
- Performed StandardScaler to bring down all the important numerical values near to mean. This helps in removing outliers, and centralizing our data.
- Now splitted the data into training and testing.
- Here I used VoteClassifier with ensembling LightGradientBoostClassifier, CatBoostClassifier, XGBoostClassifier and GradientBoostClassifier. Found parameters of these models using Optuna.
- The applied Repeated Stratified KFold so that we can find out best accuracy our model can give.
- Predicted the model on test.csv.

As this was a Kaggle Competition, my rank was in top 35%. 
- 



 
