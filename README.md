# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1.'pandas': For handling and analyzing data.

2.'load_iris': Loads the Iris dataset, a built-in dataset in scikit-learn.

3.'SGDClassifier': Implements Stochastic Gradient Descent (SGD) for classification.

4.'train_test_split': Splits the dataset into training and testing sets.

5.'accuracy_score', 'confusion_matrix', 'classification_report': Evaluate model performance.

6.The Iris dataset is loaded.

7.The dataset is converted into a pandas DataFrame with feature names as column labels.

8.The target column (species labels: 0, 1, 2) is added.

9.The first few rows are printed to inspect the data.

10.'x' (features): All columns except target.

11.'y' (target variable): The 'target' column containing class labels.

12.80% of the data is used for training ('x_train', 'y_train').

13.20% of the data is used for testing ('x_test', 'y_test').

14.'random_state=42' ensures reproducibility (same split every time).

15.'SGDClassifier' is initialized with: 'max_iter=1000': Runs up to 1000 iterations to optimize weights. 'tol=1e-3': Stops early if the loss improvement is below '0.001'. 

16.The classifier is trained on the training dataset using 'fit()'. 

17.The trained model predicts labels ('y_pred') for 'x_test' using 'predict()'. 

18.'accuracy_score(y_test, y_pred)' compares predictions with actual values.

19.The accuracy (fraction of correct predictions) is printed. 

20.The Confusion Matrix is printed to analyze how many predictions were correct or misclassified. 

21.The Classification Report includes: Precision: How many positive predictions were actually correct? Recall: How many actual positives were correctly predicted? F1-score: Harmonic mean of precision and recall. Support: Number of actual occurrences of each class.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

import pandas as pd
from sklearn.datasets import load_iris
from sklearn.linear_model import SGDClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

iris  = load_iris()

df = pd.DataFrame(data=iris.data, columns=iris.feature_names)
df['target'] = iris.target
print("Name: DIVYASHREE B\nReg.no: 212224040081")
print(df.head())

x = df.drop('target', axis=1)
y = df['target']

x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=42)

sgd_clf = SGDClassifier(max_iter=1000, tol=1e-3)
sgd_clf.fit(x_train, y_train)

y_pred = sgd_clf.predict(x_test)

accuracy = accuracy_score(y_test, y_pred)
print(f"Accuracy: {accuracy:.3f}")

cm = confusion_matrix(y_test, y_pred)
print("Confusion Matrix:")
print(cm)

classification_report1 = classification_report(y_test, y_pred)
print(classification_report1)
Developed by: DIVYASHREE B
RegisterNumber: 212224040081
*/
```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
<img width="798" height="635" alt="image" src="https://github.com/user-attachments/assets/6a064de9-f529-44c9-99b6-031fd326883c" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
