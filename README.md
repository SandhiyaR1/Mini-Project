# Mini-Project: 
### DATASET: 
SUPER STORES 
### TOPIC:
DATA VISUALIZATION
# AIM:
To perform data visualization for the given dataset.

## PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv('/content/SuperStore.csv')
df.head()

df.info()

df.isnull()

df.isnull().sum()

df.describe()

df.dropna(subset=['Postal Code'], inplace=True)
print(df)

df.isnull().sum()

# Example: Create a bar plot of sales by category
category_sales = df.groupby('Category')['Sales'].sum()
category_sales.plot(kind='bar')
plt.xlabel('Category')
plt.ylabel('Sales')
plt.title('Sales by Category')
plt.show()

# Example: Create a bar plot of profits by sub-category
subcat_profits = df.groupby('Sub-Category')['Sales'].sum()
subcat_profits.plot(kind='bar')
plt.xlabel('Sub-Category')
plt.ylabel('Sales')
plt.title('Profit by Sub-Category')
plt.show()

# Example: Create a bar plot of sales by region
region_sales=df.groupby('Region')['Sales'].sum()
region_sales.plot(kind='bar')
plt.xlabel('Region')
plt.ylabel('Sales')
plt.title('Sales by Region')
plt.show()

# Example: Create a pie chart of sales by ship mode
shipmode_sales = df.groupby('Ship Mode')['Sales'].sum()
shipmode_sales.plot(kind='pie', autopct='%1.1f%%')
plt.title('Sales by Ship Mode')
plt.axis('equal')
plt.show()

# Example: Create a bar plot of sales by segment
segment_sales = df.groupby('Segment')['Sales'].sum()
segment_sales.plot(kind='bar')
plt.xlabel('Segment')
plt.ylabel('Sales')
plt.title('Sales by Segment')
plt.show()

# Example: Create a line plot of sales over time (order date)
df['Order Date'] = pd.to_datetime(df['Order Date'])
df['Year'] = df['Order Date'].dt.year
yearly_sales = df.groupby('Year')['Sales'].sum()
yearly_sales.plot(kind='line', marker='o')
plt.xlabel('Year')
plt.ylabel('Sales')
plt.title('Sales Over Time')
plt.show()
```
# OUTPUT:
### df.head():
![image](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/a02040d1-89cd-4fd7-8e8e-ebf1c9a02498)
## df.info():
![Screenshot 2023-06-13 092750](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/779eb65e-5cfd-4000-b800-de116a3a52ba)
## df.isnull():
![Screenshot 2023-06-13 093012](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/17c6eabf-bfa8-4452-af19-793c955d1513)
## df.isnull().sum():
![image](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/551e88d3-e2d2-46bc-b042-0659648cca95)
## df.describe():
![image](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/501c380c-0609-4082-b833-4e281e0be766)
### df.isnull().sum():
![image](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/2f2ee8ef-f7d8-45a9-8adc-1c5547e89a8c)
### Bar plot of sales by category:
![image](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/70f306e8-c86c-49da-bb24-81c0875060e7)
### bar plot of profits by sub-category:
![Screenshot 2023-06-13 093300](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/54cd3963-4af0-4454-8f8a-7001ea37e3e6)
## Create a bar plot of sales by region:
![Screenshot 2023-06-13 093340](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/63844594-1aaa-4866-81d7-aecfa095a701)
## Create a pie chart of sales by ship mode:
![Screenshot 2023-06-13 093413](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/f34ced3e-d7d2-44cf-a082-aa60786b14a2)
##  Create a bar plot of sales by segment:
![Screenshot 2023-06-13 093456](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/280c0caa-3e22-4fcc-b2a2-a0d56a9631f2)
## Create a line plot of sales over time (order date):
![Screenshot 2023-06-13 093528](https://github.com/SandhiyaR1/Mini-Project/assets/113497571/d2b7fbc0-2a2f-4bc1-878c-3700042b26af)

# RESULT:
Thus, we obtained the visualization of the data for the given dataset.

