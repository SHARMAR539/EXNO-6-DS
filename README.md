# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 Include the necessary coding and corresponding screenshots


```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```


<img width="1131" height="201" alt="image" src="https://github.com/user-attachments/assets/469e9097-b038-4b39-a98e-6a3488024084" />



1.Line Plot

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="568" height="483" alt="image" src="https://github.com/user-attachments/assets/0d1bf80e-2748-4a1e-8cd0-6093d7c784d8" />


2.Multi Line Plot

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```


<img width="551" height="471" alt="image" src="https://github.com/user-attachments/assets/f99e1dfd-ccad-4e59-9579-46193b5a2ea9" />




TO VISUALIZE RELATIONSHIPS

1.Bar Chart


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="1316" height="583" alt="image" src="https://github.com/user-attachments/assets/fe55777c-b4ac-4567-85ee-97656ba08b85" />


2.Scatter Plot

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="575" height="456" alt="image" src="https://github.com/user-attachments/assets/a5e6a47c-d8de-4c62-9320-de90e7a4db9d" />


3.Bubble Chart

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="575" height="457" alt="image" src="https://github.com/user-attachments/assets/c0d7f6d7-a022-46b7-a24a-a9b737c7a3d8" />


TO CAPTURE DISTRIBUTIONS

1.Histogram

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="582" height="471" alt="image" src="https://github.com/user-attachments/assets/5e81e0c8-4844-46e0-a527-f0fdfa9ff2b5" />


2.Box Plot

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="1335" height="566" alt="image" src="https://github.com/user-attachments/assets/c6dd9867-cb68-4b90-a026-78b926ee85bf" />


3.Violin Plot

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="569" height="462" alt="image" src="https://github.com/user-attachments/assets/6b314805-dcf9-4650-92c2-c70e01e39cbe" />



4.Density Plot

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="590" height="579" alt="image" src="https://github.com/user-attachments/assets/b71b295f-b3b3-4d1f-af9a-09159b94813d" />



5.Heatmap


```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="594" height="495" alt="image" src="https://github.com/user-attachments/assets/f2b94a7d-6204-430f-afe2-c3cfe365efa9" />




 

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
