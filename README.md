# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. Calculate Mean square error,data prediction and r2.


## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: SUNIL KUMAR P.B.
RegisterNumber:  212223040213
*/
```
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>




```PY

import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()

data.info

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
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
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


## Output:

### DATA HEAD:

![image](https://github.com/user-attachments/assets/ec083b7b-ab45-43c0-80d4-ba05ec1645ef)

### DATA INFO:
![image](https://github.com/user-attachments/assets/7342f8c0-ec14-40f8-b26e-5df1d793c135)

### ISNULL() AND SUM():

![image](https://github.com/user-attachments/assets/f13737c6-61fd-4c28-a5e8-cb0c000128a8)

### DATA HEAD FOR SALARY:

![image](https://github.com/user-attachments/assets/97504577-6eee-460a-abe1-09acf8cb7194)

### MEAN SQUARED ERROR:

![image](https://github.com/user-attachments/assets/ea3259ec-a248-4601-b605-b67262751272)

### R2 VALUE:

![image](https://github.com/user-attachments/assets/89bccffb-a7e6-4395-9ae7-e37bcfe7586a)

### DATA PREDICTION:

![image](https://github.com/user-attachments/assets/1a692c24-a11f-4b30-9d54-16fb3dc9b326)

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>





## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
