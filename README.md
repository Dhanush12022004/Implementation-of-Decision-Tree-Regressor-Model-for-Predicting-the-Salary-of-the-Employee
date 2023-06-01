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
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: DHANUSH.G.R.
RegisterNumber:  212221040038

import pandas as pd
data=pd.read_csv("/content/Salary.csv")

print("Data.head():")

data.head()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder

le=LabelEncoder()
print("data.head() for Salary:")
data["Position"]=le.fit_transform(data["Position"])

print("data.head() for Salary:")

data.head()

print("Data.info():")
data.info()
print("Data.isnull() and Sum():")

data.isnull().sum()

x=data[["Position","Level"]]

y=data[["Salary"]]


from sklearn.model_selection import train_test_split

x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor

dt=DecisionTreeRegressor()

dt.fit(x_train,y_train)

y_pred=dt.predict(x_test)

print("MSE Value:")


from sklearn import metrics

mse=metrics.mean_squared_error(y_test,y_pred)

mse

r2=metrics.r2_score(y_test,y_pred)
print("r2 Value:")

r2

print("data prediction:")

dt.predict([[5,6]])

```
## Output:

![image](https://github.com/Dhanush12022004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135558/b96f341c-c759-439a-8441-3b45439bd5f5)

![image](https://github.com/Dhanush12022004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135558/7affba19-f2b8-400e-b083-dd7d116acefa)

![image](https://github.com/Dhanush12022004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135558/9f80a8af-a688-44be-9a6c-66aecf7339b1)

![image](https://github.com/Dhanush12022004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135558/55c033cf-bf45-43d8-b916-b0fd3598ac23)

![image](https://github.com/Dhanush12022004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135558/e007e660-b5f5-4a79-9097-5cc1ab3fe0b3)

![image](https://github.com/Dhanush12022004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135558/a5856c3f-dd78-42b3-9f74-b8d4c546330e)

![image](https://github.com/Dhanush12022004/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/128135558/7be85307-f7d5-43c1-9c75-d0b8fd248c77)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
