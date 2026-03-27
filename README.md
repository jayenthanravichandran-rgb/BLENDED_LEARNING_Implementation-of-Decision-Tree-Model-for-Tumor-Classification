# BLENDED_LEARNING
# Implementation of Decision Tree Model for Tumor Classification

## AIM:
To implement and evaluate a Decision Tree model to classify tumors as benign or malignant using a dataset of lab test results.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and load the tumor dataset using pandas.

2.Separate the dataset into input features (X) and target class (y).

3.Split the dataset into training and testing sets using train_test_split.

4.Train the Decision Tree Classifier using the training data.

5.Predict the test results and evaluate the model using accuracy score, classification report, and confusion matrix.


## Program:
```
/*
Program to  implement a Decision Tree model for tumor classification.
Developed by: R JAYENTHAN
RegisterNumber:  212225240057


import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score,classification_report,confusion_matrix
import seaborn as sns
import matplotlib.pyplot as plt

data = pd.read_csv("tumor.csv")

print(data.head())
print(data.columns)

X=data.drop("Class",axis=1)
y=data["Class"]

X_train,X_test,y_train,y_test = train_test_split(X,y,test_size=0.3,random_state=42)

model = DecisionTreeClassifier(random_state=42)
model.fit(X_train,y_train)

y_pred=model.predict(X_test)

accuracy=accuracy_score(y_test,y_pred)
print("\nName: R VENKATRAMANI")
print("\nReg No: 212225240182")
print("\nAccuracy",accuracy)

print("Classification Report:\n", classification_report(y_test, y_pred))

c_matrix=confusion_matrix(y_test,y_pred)
sns.heatmap(c_matrix)
plt.xlabel("Predicted")
plt.ylabel("Actual")
plt.title("Confusion Matrix")
plt.show()
*/
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)
<img width="1012" height="533" alt="image" src="https://github.com/user-attachments/assets/ef48039c-ed6f-4279-aad7-7eefac5f531f" />
<img width="706" height="473" alt="image" src="https://github.com/user-attachments/assets/4dec23b0-cf48-406e-897d-0b70d49621de" />


## Result:
Thus, the Decision Tree model was successfully implemented to classify tumors as benign or malignant, and the model’s performance was evaluated.
