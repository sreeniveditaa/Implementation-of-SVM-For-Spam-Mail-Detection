# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries.
2.Read the data frame using pandas.
3.Get the information regarding the null values present in the dataframe.
4.Split the data into training and testing sets.
5.Convert the text data into a numerical representation using CountVectorizer.
6.Use a Support Vector Machine (SVM) to train a model on the training data and make predictions on the testing data.
7.Finally, evaluate the accuracy of the model.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: SREE NIVEDITAA SARAVANAN
RegisterNumber: 212223230213

import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import CountVectorizer
from sklearn import svm
from sklearn.metrics import classification_report, accuracy_score
df= pd.read_csv('/content/spam.csv', encoding='ISO-8859-1')
df.head()
vectorizer= CountVectorizer()
x= vectorizer.fit_transform(df['v2'])
y=df['v1']
x_train, x_test, y_train, y_test= train_test_split(x,y,test_size=0.25, random_state=42)
model= svm.SVC(kernel='linear')
model.fit(x_train, y_train)
predictions= model.predict(x_test)
print("Accuracy:", accuracy_score(y_test, predictions))
print("Classification Report:")
print(classification_report(y_test, predictions))  
*/
```

## Output:
![Screenshot 2024-05-07 161504](https://github.com/sreeniveditaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/147473268/970770f7-5517-4d1b-851a-898c29ef5f29)

![Screenshot 2024-05-07 161457](https://github.com/sreeniveditaa/Implementation-of-SVM-For-Spam-Mail-Detection/assets/147473268/b7698407-8e2a-49d4-8990-78cdcd93fd91)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
