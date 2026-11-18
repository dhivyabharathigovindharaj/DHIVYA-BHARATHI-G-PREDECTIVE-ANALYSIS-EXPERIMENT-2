## Experiment 2: Data Visualization Using Matplotlib and Seaborn

## Aim

To visualize data using Matplotlib and Seaborn libraries.

## Algorithm
Start.
Import the Matplotlib and Seaborn libraries.
Load data into a Pandas DataFrame.
Plot a histogram for age distribution using plt.hist().
Plot a scatter plot for Age vs. Salary using sns.scatterplot().
Plot salary distribution using sns.boxplot().
Show the plots sequentially.
Stop.

## Program
```
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
# Create Dataset
data = {
    'Age': [22, 25, 30, 27, 32, 38, 26, 29, 35, 40],
    'Salary': [30000,35000,40000,45000,50000,38000,42000,48000,34000,37000],
    'Salary_color': ['red','blue','orange','purple','green','yellow','lightblue','pink','brown','magenta']
}
df = pd.DataFrame(data)
print("\nDataset:")
print(df)
# Histogram
plt.figure(figsize=(6,4))
plt.hist(df['Age'], bins=6, color='orange', edgecolor='black')
plt.title('Age Distribution')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()
# Scatter Plot
plt.figure(figsize=(6,4))
sns.scatterplot(x='Age', y='Salary', data=df, color='purple')
plt.title('Age vs Salary')
plt.xlabel('Age')
plt.ylabel('Salary')
plt.show()
# Pie Chart
plt.figure(figsize=(6,6))
plt.pie(
    df['Salary'],
    labels=df['Age'],
    colors=df['Salary_color'],
    autopct='%1.1f%%'
)
plt.title('Salary Distribution by Age')
plt.show()
# Box Plot
plt.figure(figsize=(6,4))
sns.boxplot(x=df['Salary'], color='gold')
plt.title('Salary Distribution')
plt.xlabel('Salary')
plt.show()
```

## Output

Dataset:
   Age  Salary Salary_color
0   22   30000          red
1   25   35000         blue
2   30   40000       orange
3   27   45000       purple
4   32   50000        green
5   38   38000       yellow
6   26   42000    lightblue
7   29   48000         pink
8   35   34000        brown
9   40   37000      magenta

<img width="536" height="393" alt="image" src="https://github.com/user-attachments/assets/7ba99dc0-cd6c-404c-90e5-319ca7b69b09" />


<img width="558" height="393" alt="image" src="https://github.com/user-attachments/assets/b44080e6-5d42-4601-9097-d954a100e07b" />


<img width="558" height="393" alt="image" src="https://github.com/user-attachments/assets/d94b8a00-5a43-4d30-9d18-88ee6e3d0fe2" />






## Result
