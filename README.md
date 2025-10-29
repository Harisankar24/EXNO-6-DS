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
 import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("/content/titanic_dataset (1).csv")
 df.head()

 <img width="1445" height="370" alt="image" src="https://github.com/user-attachments/assets/f1b3761d-faff-484b-827e-4fe7b12806e8" />

## Line plot

 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')

 <img width="1176" height="649" alt="image" src="https://github.com/user-attachments/assets/4b7b450b-d704-4c36-a2ea-3e153612056a" />

 ## Mulit Line plot

  x=[1,2,3,4,5]
 y1=[3,5,2,6,1]
 y2=[1,6,4,3,8]
 y3=[5,2,7,1,4]
 sns.lineplot(x=x,y=y1)
 sns.lineplot(x=x,y=y2)
 sns.lineplot(x=x,y=y3)
 plt.title('Multi Line Plot')

 <img width="929" height="706" alt="image" src="https://github.com/user-attachments/assets/527e0472-6b42-4181-879a-dc7f7628c810" />

 ## Bar chart

  plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")

 <img width="1051" height="528" alt="image" src="https://github.com/user-attachments/assets/c0cb794c-dd80-4f02-947e-403e1d3b52e0" />

## scatter plot

 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()

 
 <img width="995" height="584" alt="image" src="https://github.com/user-attachments/assets/a0488c00-035b-4ded-a3b2-6d34be8e1d0c" />


## Bubble plot

 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()

 <img width="982" height="594" alt="image" src="https://github.com/user-attachments/assets/a2419d4f-a865-4d11-b10b-c4318d84bdd7" />

## Histogram

 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)


 <img width="1002" height="568" alt="image" src="https://github.com/user-attachments/assets/4aaf1c71-a5d7-4c4d-8312-1956bc7852ef" />

## Box plot

sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")

 <img width="805" height="505" alt="image" src="https://github.com/user-attachments/assets/aae64be9-ee5c-47e4-a1c3-dc4681f3cbe9" />

## Violin plot


  sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()

 <img width="1005" height="610" alt="image" src="https://github.com/user-attachments/assets/945c6ba9-20f3-4c0b-9f8c-715a79597d31" />

## Density plot


  sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()

 <img width="977" height="492" alt="image" src="https://github.com/user-attachments/assets/d1a9989a-298a-4d1b-8095-a5f9b86c16d7" />

## Heatmap


  numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()

 <img width="1113" height="684" alt="image" src="https://github.com/user-attachments/assets/47006113-14f4-485f-8ea7-6226cde29388" />




# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
