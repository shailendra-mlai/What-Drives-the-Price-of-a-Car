# What-Drives-the-Price-of-a-Car
Professional Certificate in Machine Learning and Artificial Intelligence. Practical Application Assignment 11.1: What Drives the Price of a Car?

**Overview**

Goal of the project is to understand what factors make used car more or less expensive. Based on the analyais provide recommendations to a used car dealership on what consumers value in a car.

**Data**

The original dataset from kaggle contained information on 3 million used cars. A smaller dataset is provided which contains information on 426K cars to ensure speed of processing.

**The Jupyter Notebook covers the following:**

**Business Understanding**

Task here is to identify the key features from the dataset to predict price of the used cars.
The objective is to develop a predictive model that accurately estimates the prices of used cars. The task involves data preprocessing, feature engineering, and machine learning model development to create a robust predictive algorithm capable of accurately forecasting used car prices based on the provided dataset.

**Data Understanding**

Examine the dataset, unique values for each column. Visualizate data for better understanding. 

**Data Preparation**

1. Converting the datatype to best possilble datatypes
2. Drop Columns with large unique entries.
3. Dropping rows where the title_status is not clean, since 405k entry has "clean" value.
4. Dropping the rows with missing values means losing lot of data. Using Simple Imputer for completing missing values with simple strategies.
5. Tried Label Encoder and One hot encoding.

**Modeling**

1. Function to determine best model complexity using One hot encoding
2. For best model complexity use PolynomialFeatures (degree=4)
3. Function to determine best model complexity using Label Encoder
4. For best model complexity use PolynomialFeatures using Label encoder (degree=3)
5. Grid Search CV using One hot encoding to search for Number of features
6. Grid Search CV using Label Encoder and found n_features_to_select=4
7. Ridge Regression with GridSearch CV to find the optimal alpha for one hot encoding
9. Ridge Regression with GridSearch CV to find the optimal alpha for label encoder
10. Using Ridge(alpha=449.84) with Label encoder to calculate MSE
11. Using RandomForestRegressor to calculate MSE
12. Using RandomForestRegressor with Label encoder to calculate MSE

**Conclusion:**

From give data set and choosing the optimal modeling we came to conclusion on what drives the price of the used car:

The coefficients in a linear regression model represent the weights assigned to each feature in the model. These coefficients indicate the strength and direction of the relationship between each feature and the target variable.

1.	Car title must be clean status.
2.	Year: For each year increase in the vehicle's age, the price decreases by approximately $38.19.
3.	Manufacturer: The price decreases by about $1.67 for each unit increase in the manufacturer index based on Categorical encoder. 
4.	Condition: Each unit increase in the condition index results in a decrease in price of about $11.68.
5.	Cylinders: Price increases by approximately $1.05 for each additional cylinder.
6.	Fuel type also dictate the price of the car. Most of the data we had was gas. 
7.	Odometer: For every mile increase in odometer reading, the price decreases by about $0.02.
8.	Transmission: Most of the data had automatic transmission, which will also influence the price of the car. 
9.	Drive type of rwd leads to a decrease in price of around $16.47.


PS: The HTML representation is unable to render in the github, please try this link to view the Jupyter notebook.
https://nbviewer.org/github/shailendra-mlai/What-Drives-the-Price-of-a-Car/blob/main/Shailendra-Practical-App-2.ipynb
