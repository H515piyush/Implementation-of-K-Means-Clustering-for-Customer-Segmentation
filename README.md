# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages using import statement.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Import KMeans and use for loop to cluster the data.

4.Predict the cluster and plot data graphs.

5.Print the outputs and end the program
## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by:PIYUSH KUMAR 
RegisterNumber:212223220075  
*/
import pandas as pd
 import matplotlib.pyplot as plt
 data = pd.read_csv("C:/Users/admin/Downloads/Mall_Customers.csv")
 data.head()
data.info()

 data.isnull().sum()

 from sklearn.cluster import KMeans
 wcss=[]
for i in range(1,11):
 Kmeans = KMeans(n_clusters = i , init = "K-means++")
 Kmeans.fit(data.iloc[:,3:])
 wcss.append(kmeans.inertia_)


 plt.plot(range(1,11),wcss)
 plt.xlabel("No. of clustres ")
 plt.ylabel("wcss")
 plt.title("Elbow Method")

km=KMeans(n_clusters=5)
 km.fit(data.iloc[:,3:])

 y_pred=km.predict(data.iloc[:,3:])
 y_pred

data['cluster']=y_pred
 df0=data[data["cluster"]==0]
 df1=data[data["cluster"]==1]
 df2=data[data["cluster"]==2]
 df3=data[data["cluster"]==3]
 df4=data[data["cluster"]==4]
 plt.scatter(df0['Annual Income (k$)'],df0['Spending Score (1-100)'],c="red" 
plt.scatter(df1['Annual Income (k$)'],df1['Spending Score (1-100)'],c="black
 plt.scatter(df2['Annual Income (k$)'],df2['Spending Score (1-100)'],c="blue
 plt.scatter(df3['Annual Income (k$)'],df3['Spending Score (1-100)'],c="green
 plt.scatter(df4['Annual Income (k$)'],df4['Spending Score (1-100)'],c="magen
 plt.legend()
 plt.title("customer segments")




```

## Output:


![Screenshot 2024-04-23 104433](https://github.com/H515piyush/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147472999/33387a14-4951-4d65-acff-a94fc176b945)
![Screenshot 2024-04-23 104442](https://github.com/H515piyush/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147472999/2c2441be-50a6-45ba-bac3-bcdbc23a1ae6)
![Screenshot 2024-04-23 104450](https://github.com/H515piyush/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147472999/c837b9e8-0e21-4de6-8f26-f96af7a6fcfb)
![Screenshot 2024-04-23 104503](https://github.com/H515piyush/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147472999/cf7fc59b-3c41-4ce1-ac20-cdbc47aa78fa)
![Screenshot 2024-04-23 104510](https://github.com/H515piyush/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147472999/90bc39a3-9149-48d6-9b6d-7ea665151ae9)
![Screenshot 2024-04-23 104522](https://github.com/H515piyush/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147472999/2a5acb58-024f-4e27-8081-18026dd0338e)

![Screenshot 2024-04-23 104530](https://github.com/H515piyush/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/147472999/17e29cd3-a855-488c-b068-f30a50dbd072)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
