Customer Churn Analysis and Prediction
  
DATA USED:-
- Source -->  https://www.kaggle.com/datasets/ankitverma2010/ecommerce-customer-churn-analysis-and-prediction/data
- The dataset used in this project is based on an e-commerce company who wants to know number of customers who are going to churn 
  
  
EXPLORATORY DATA ANALYSIS:-
- With the help of Seaborn and Matplotlib, many charts and graphs were plotted
- This step is crucial as it helps in visualizing differnet relationships between each feature present in the dataset

Observations:-

1. Male customers are more in number - 3384 and among them 17% are churned
2. Among females- 2246, around 16% are churned
3. Most of the customers prefer mobile phones as login device, and only around 13% churn is seen
4. Maximum, 4 hrs is spent on the app, but majority of customers use for around 3 hrs
5. More complains are raised by customers from City Tier 1
6. Debit card is the most preferred payment mode and least preferred is Cash on Delivery
7. Churn count is high among customers who prefer e-wallet for payment 


DATA PREPROCESSING:-
- The dataset is read using the Pandas library from a csv file and then looked for its dimensions, each columns' data types.
- Also, checked for the presence of any null values or duplicates
- Since the dataset is large, null values are removed from the dataset
  
FEATURE ENGINEERING:-

One hot encoding:

- As, there are multi columns with categorical variables, label encoding was used, through which the data was ready for undergoing model buliding process

FEATURE SELECTION:-
- As there are many features, top 10 features which affect the churn are selected using correlation coefficient method one among the filter methods under feature selection
- 'Tenure', 'Complain', 'NumberOfDeviceRegistered', 'DaySinceLastOrder','MaritalStatus', 'PreferedOrderCat', 'SatisfactionScore','WarehouseToHome', 'NumberOfAddress', 'CityTier' are
- the 10 features selected for model training

DATA STANDARDISATION:-
- Since the dataset has values which are of different formats like float, whole number are standardised

MODEL BUILDING:-
- The data was separated into features and target followed by train test split
- As the target value is price, which is a continous variable, algorithms like Linear Regression, KNeighborsRegression and Random Forest Regression were used
- Grid Search CV method was employed followed by cross validation method in order to find the best model parameters
- From the above method, Random Forest Classifier was found out to be the best algorithm with best fit for this prediction with around 97% accurate
- This can be saved as model using pickle and use later for predicting customers churn

REFERENCES:-
- https://365datascience.com/tutorials/python-tutorials/how-to-build-a-customer-churn-prediction-model-in-python/#2
- https://www.analyticsvidhya.com/blog/2022/06/e-commerce-customer-churn-prediction/
