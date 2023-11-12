# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload the csv file and read the dataset. 3.check for any null values using the isnull() function.
3. From sklearn.tree inport DecisionTreeRegressor.
4. Import metrics and calculate the Mean squared error.
5. Apply metrics to the dataset, and predict the output. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by:GREFFINA SANCHEZ P 
RegisterNumber:  212222040048
*/

import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data[["Salary"]]
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

```

## Output:

1. data.head()

   ![image](https://github.com/greffinaprem/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475603/979f7ed1-1868-4015-9160-5fdcb73e8995)

2. data.info()

   ![image](https://github.com/greffinaprem/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475603/2a6d4ef4-19cc-4f7d-9617-f6233a52b14c)

3. isnull() & sum() function

    ![image](https://github.com/greffinaprem/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475603/f5dce8ce-05ba-4eb4-8946-8002c9bebcc5)

4. data.head() for position

   ![image](https://github.com/greffinaprem/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475603/541400f0-197a-4fb4-873e-b9be7cc6f84e)

5. MSE value

    ![image](https://github.com/greffinaprem/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475603/5a631dc3-0864-4c28-b405-9932921175fd)

6. R2 value

    ![image](https://github.com/greffinaprem/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475603/5ac4f4f7-8a37-42ea-9008-59def303c4ce)

7. Prediction value

    ![image](https://github.com/greffinaprem/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119475603/ab016de4-2e56-45c6-a8a0-0aaae1ae5d9a)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
