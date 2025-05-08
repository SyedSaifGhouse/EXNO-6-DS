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
# Name : SYED SAIF SYED GHOUSE
# Reg no : 212224230286
```
  import pandas as pd
  import seaborn as sns
  import matplotlib.pyplot as plt
  df=pd.read_csv("titanic_dataset.csv")
  df.head()
```
![441173008-ff246e8a-2d10-44b7-bcee-20210556cfa5](https://github.com/user-attachments/assets/a354cd49-2400-40a5-a686-be42c91aa0e6)

# 1.LINE PLOT
```
  x=[1,2,3,4,5]
  y=[3,6,2,7,1]
  sns.lineplot(x=x,y=y)
  plt.title('Line Plot')
```
![441173111-039930a2-701d-4eb0-88bb-d0953bfa4634](https://github.com/user-attachments/assets/aa98c787-633e-4e87-bf71-4c1cd573f76f)

# MULTI LINE PLOT
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


![441173502-394e0b91-1091-40ab-82d7-6712f6c0ed6b](https://github.com/user-attachments/assets/309d4302-1b5c-4a66-a20e-1250eed8c74d)
# TO VISUALIZE RELATIONSHIPS
# BAR CHART
```
  plt.figure(figsize=(8,5))
  sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
  plt.title("Fare Of Passenger By Embarked Town")
```
![441173718-b72d36e2-754d-49f2-91ca-24c77332f24d](https://github.com/user-attachments/assets/4cc5126c-0a48-46c4-81a4-5e18e40acea1)

# SCATTER PLOT
```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

![441173861-8c787ffb-5b18-4b4f-8e9d-9c222e424f69](https://github.com/user-attachments/assets/094d0b87-6c23-4c09-80b9-7c8175fb0854)

# BUBBLE CHART
```
  sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
  plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
  plt.show()
```

![441174177-e294cc77-d04b-485b-9467-028347388d5e](https://github.com/user-attachments/assets/4e369d0a-51ae-4ccb-89ff-cdf4f2612191)

# TO CAPTURE DISTRIBUTIONS
# HISTOGRAM

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![441174435-efce6920-569d-46b0-8005-9ef2d758f93c](https://github.com/user-attachments/assets/9c3c3de9-a096-4b9f-840a-33f5bd70b77d)

# BOX PLOT
```
  sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
  plt.title("Age By Passenger Class")

```
![441174595-92f9db8b-ae76-447e-8bca-e0579ab4dd87](https://github.com/user-attachments/assets/5ec74644-1c97-4099-ba38-b52371293a04)

# VIOLIN PLOT
```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![441174898-5d31b843-c672-475c-b8a4-584c39fc0d6a](https://github.com/user-attachments/assets/c425c29a-26a5-4384-90b3-44408f331f4b)

# DENSITY PLOT
```

  sns.kdeplot(data=df['Age'], shade=True)
  plt.title('Density Plot of Passenger Ages')
  plt.show()

```
![441175064-365eafce-5fbc-43df-9fa7-5d9c5ff81c1b](https://github.com/user-attachments/assets/8a48adc3-02f5-44fd-be4b-b931c1b7b7bc)

# HEAT MAP
```

  numeric_df = df.select_dtypes(include=['float64', 'int64'])
  corr_matrix = numeric_df.corr()
  sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
  plt.title('Heatmap of Titanic Dataset')
  plt.show()
```

![441175228-e224bd4e-5995-410a-b85b-314caf78f141](https://github.com/user-attachments/assets/16d5aab0-8f10-4c45-b74d-8c521550b1be)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
