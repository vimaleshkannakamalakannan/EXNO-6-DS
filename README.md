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
 ~~~
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
~~~
<img width="1327" height="213" alt="Screenshot 2026-08-25 104543" src="https://github.com/user-attachments/assets/85f07cac-437c-469a-bd88-a9036b1f5664" />

~~~
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
~~~
<img width="534" height="433" alt="download" src="https://github.com/user-attachments/assets/5d07dcb5-5932-400a-91d4-e903b21cf0b5" />

~~~
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
~~~
<img width="534" height="433" alt="download" src="https://github.com/user-attachments/assets/d26337cb-f85c-4dcf-9ad5-88bbeb12d3b4" />

~~~
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
~~~
<img width="687" height="468" alt="download" src="https://github.com/user-attachments/assets/078e9427-1708-473f-b612-5e3fb9146f4f" />

~~~
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
~~~
<img width="571" height="453" alt="download" src="https://github.com/user-attachments/assets/1acf133f-fcaa-4ff5-aa63-debb084ca504" />

~~~
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
~~~
<img width="571" height="453" alt="download" src="https://github.com/user-attachments/assets/37a5adae-56ed-4898-8ce7-85a847198811" />

~~~
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
~~~
<img width="571" height="432" alt="download" src="https://github.com/user-attachments/assets/3caf83d6-efb2-4502-a86e-30df35b62690" />

~~~
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
~~~
<img width="563" height="453" alt="download" src="https://github.com/user-attachments/assets/b652e75a-9e47-4b77-aaf3-71fc3a6a17cc" />

~~~
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
~~~
<img width="571" height="453" alt="download" src="https://github.com/user-attachments/assets/029d92ba-d388-488c-8480-592db206e627" />

~~~
sns.kdeplot(data=df['Age'], fill=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
~~~
<img width="585" height="453" alt="download" src="https://github.com/user-attachments/assets/bcf03ce8-853d-4db4-ac75-42c9f8794738" />

~~~
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
~~~
<img width="597" height="503" alt="download" src="https://github.com/user-attachments/assets/47d0f62f-eb91-4e29-81d9-0fa4f26fd47c" />

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully



