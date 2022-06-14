# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

### STEP 1:

Import the required libraries.

### STEP 2:

Upload the csv file and read the dataset.

### STEP 3:

Check for any null values using the isnull() function.

### STEP 4:

From sklearn.tree inport DecisionTreeRegressor.

### STEP 5:

Import metrics and calculate the Mean squared error.

### STEP 6:

Apply metrics to the dataset, and predict the output.

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Monisha T
RegisterNumber: 212221240029 

```

```python

import pandas as pd
data = pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()
x = data[["Position","Level"]]
y = data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
r2 = metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

```

# Output:

## DATA HEAD:

![output](./output1.png)

## DATA INFO:

![output](./output2.png)

## DATA ISNULL:

![output](./output3.png)

## DATA HEAD:

![output](./output4.png)

## dt.FIT:

![output](./output5.png)

## MSE:

![output](./output6.png)

## R2:

![output](./output7.png)

## PREDICT VALUE:

![output](./output8.png)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
