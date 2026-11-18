## Experiment 2: Data Visualization Using Matplotlib and Seaborn

## Aim

To visualize data using Matplotlib and Seaborn libraries.

## Algorithm

1. Start.
2. Import the Matplotlib and Seaborn libraries.
3. Load data into a Pandas DataFrame.
4. Plot a histogram for age distribution using plt.hist().
5. Plot a scatter plot for Age vs. Salary using sns.scatterplot().
6. Plot salary distribution using sns.boxplot().
7. Show the plots sequentially.
8. Stop.

## Program
## Input 1
```
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

#Create Dataset
data = {
    'Age': [22, 25, 30, 27, 32, 38, 26, 29, 35, 40],
    'Salary': [30000,35000,40000,45000,50000,38000,42000,48000,34000,37000],
    'Salary_color': ['red','blue','orange','purple','green','yellow','lightblue','pink','brown','magenta']
}
df = pd.DataFrame(data)
print("\nDataset:")
print(df)
```

## Output 1
```

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
```



## Input 2
# Histogram
```
plt.figure(figsize=(6,4))
plt.hist(df['Age'], bins=6, color='orange', edgecolor='black')
plt.title('Age Distribution')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()
```
## Output 2

<img width="536" height="393" alt="image" src="https://github.com/user-attachments/assets/7ba99dc0-cd6c-404c-90e5-319ca7b69b09" />


## Input 3

# Scatter Plot
```
plt.figure(figsize=(6,4))
sns.scatterplot(x='Age', y='Salary', data=df, color='purple')
plt.title('Age vs Salary')
plt.xlabel('Age')
plt.ylabel('Salary')
plt.show()
```
## Output 3
<img width="558" height="393" alt="image" src="https://github.com/user-attachments/assets/6ebc6a35-fa9a-49c4-8d83-518d931b3342" />


## Input 4

# Pie Chart
```
plt.figure(figsize=(6,6))
plt.pie(
    df['Salary'],
    labels=df['Age'],
    colors=df['Salary_color'],
    autopct='%1.1f%%'
)
plt.title('Salary Distribution by Age')
plt.show
```
## Output 4
<img width="481" height="504" alt="image" src="https://github.com/user-attachments/assets/24d34541-1903-4660-b80f-3ea14418f7d7" />

## Input 5
# Box Plot
```
plt.figure(figsize=(6,4))
sns.boxplot(x=df['Salary'], color='gold')
plt.title('Salary Distribution')
plt.xlabel('Salary')
plt.show()
```
## Output 5
<img width="490" height="393" alt="image" src="https://github.com/user-attachments/assets/5b43356c-aba8-4088-a0a0-90d5e310786c" />









## Result
Thus, the experiment was successfully executed using Matplotlib and Seaborn to create different data visualizations. The histogram, scatter plot, pie chart, and box plot helped analyze and understand the dataset effectively.

