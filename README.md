# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the Employee dataset and separate the features and target variable.
2. Convert categorical variables into numerical values.
3. Split the dataset into training and testing data.
4. Train a Decision Tree Classifier using the training data.
5. Predict employee status and evaluate the model using accuracy and confusion matrix.


## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import confusion_matrix, accuracy_score, classification_report
from sklearn import tree
import matplotlib.pyplot as plt

df = pd.read_csv("Employee.csv")

df = pd.get_dummies(df, columns=['Departments ', 'salary'], drop_first=True)

X = df.drop('left', axis=1)
y = df['left']

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.25, random_state=42
)

dt_model = DecisionTreeClassifier(
    criterion='entropy',
    max_depth=4,
    random_state=42
)

dt_model.fit(X_train, y_train)

y_pred = dt_model.predict(X_test)

print("Confusion Matrix:\n", confusion_matrix(y_test, y_pred))
print("\nAccuracy Score:", accuracy_score(y_test, y_pred))
print("\nClassification Report:\n", classification_report(y_test, y_pred))

plt.figure(figsize=(30, 15), dpi=150)

tree.plot_tree(
    dt_model,
    feature_names=X.columns,
    class_names=['Stayed', 'Churn'],
    filled=True,
    fontsize=10
)

plt.show()
Developed by: DARSHIKA M
RegisterNumber: 212225220020
*/
```

## Output:
<img width="1920" height="1080" alt="Screenshot (527)" src="https://github.com/user-attachments/assets/e6aee736-ae24-4226-936f-50e62a7cb87c" />
<img width="1920" height="1080" alt="Screenshot (528)" src="https://github.com/user-attachments/assets/dd575a62-82cd-4835-b7e1-12b4a8d36e36" />



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.

