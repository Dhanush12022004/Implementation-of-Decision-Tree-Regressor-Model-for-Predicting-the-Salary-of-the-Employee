# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import standard libraries in python for finding Decision tree regressor model for predicting the salary of the employee.
2. Initialize and print the Data.head(),data.info(),data.isnull().sum()

3. Visualize data value count.

4. Import sklearn from LabelEncoder.

5. Split data into training and testing.

6. Calculate the MSE Value,r2 Value and data prediction by importing the required modules from sklearn





## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: DHANUSH.G.R.
RegisterNumber:  212221040038
*/
```

import pandas as pd
data=pd.read_csv("/content/Salary.csv")

data.head()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder

le=LabelEncoder()

data["Position"]=le.fit_transform(data["Position"])

data.head()

x=data[["Position","Level"]]

y=data[["Salary"]]


from sklearn.model_selection import train_test_split

x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor

dt=DecisionTreeRegressor()

dt.fit(x_train,y_train)

y_pred=dt.predict(x_test)

from sklearn import metrics

mse=metrics.mean_squared_error(y_test,y_pred)

mse

r2=metrics.r2_score(y_test,y_pred)

r2

dt.predict([[5,6]])


## Output:


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
