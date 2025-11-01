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
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()

```

<img width="1069" height="185" alt="image" src="https://github.com/user-attachments/assets/f5fc15e7-fe30-4e74-9bb2-8f93b56396fb" />

# 1.Line Plot
```

x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')

```

<img width="507" height="410" alt="image" src="https://github.com/user-attachments/assets/75c008ce-8314-45ff-bce4-9994d13bcec3" />

# 2.Multi Line Plot
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

<img width="497" height="413" alt="image" src="https://github.com/user-attachments/assets/9214641f-69ba-487e-a9a3-c03db3e6db15" />

# TO VISUALIZE RELATIONSHIPS

# 1.Bar Chart
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")

```

<img width="637" height="435" alt="image" src="https://github.com/user-attachments/assets/8f3f929e-b136-4c9e-822d-80f827e00ada" />

# 2.Scatter Plot
```

sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()

```

<img width="535" height="419" alt="image" src="https://github.com/user-attachments/assets/ce2791d7-53a3-4a9b-851c-7645c6e16c86" />

# 3.Bubble Chart
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()

```

<img width="535" height="426" alt="image" src="https://github.com/user-attachments/assets/c9fa7974-460e-4703-af82-56c7d80b0bd2" />

# TO CAPTURE DISTRIBUTIONS

# 1.Histogram
```

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

```

<img width="537" height="405" alt="image" src="https://github.com/user-attachments/assets/130c618d-a880-4a8d-be6c-ca140de6565a" />

# 2.Box Plot
```

sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")

```
<img width="535" height="427" alt="image" src="https://github.com/user-attachments/assets/06ba1c72-f639-4ebb-9bd0-0ffc75e02ca7" />

# 3.Violin Plot
```

sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()

```

<img width="537" height="427" alt="image" src="https://github.com/user-attachments/assets/701a420d-68b5-4576-8d6f-88dca08783c4" />

# 4.Density Plot
```

sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()

```

<img width="551" height="425" alt="image" src="https://github.com/user-attachments/assets/b07f5248-79ef-4ec3-b8a1-9fdce5f8052b" />

# 5.Heatmap
```

numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()

```

<img width="552" height="474" alt="image" src="https://github.com/user-attachments/assets/60a0d96c-ef29-403b-b9a6-ab17637603a8" />


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
