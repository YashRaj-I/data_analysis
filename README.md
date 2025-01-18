# data_analysis
do some basic operation on a dataset of 100 rows.
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
df =pd.read_csv(r"C:\Users\Asus\Downloads\sample_employee_data_large.csv")
print(df.head())

# print(df.isnull().sum())
# print(df.duplicated().sum())

# print(df.dtypes)
# print(df.describe())

# min_thresold, max_thresold = df.Salary.quantile([0.001,0.999])
# # print(max_thresold,min_thresold)
# no_outlier = df[(df.Salary>min_thresold)&(df.Salary<max_thresold)]
# print(no_outlier.describe())




# check number of male VS female employees

# gender_counts = df['Gender'].value_counts()
# gender_counts.plot(kind='bar',color=['blue','pink'])
# plt.title('Number of Male vs Female Employees')
# plt.xlabel('Gender')
# plt.ylabel('Count')
# plt.xticks(rotation=0)
# plt.show()

# check who earn more 

# avg_income_by_gender = df.groupby('Gender')['Salary'].mean()
# print(avg_income_by_gender)

# avg_income_by_gender.plot(kind='bar',color = ['blue','pink'])
# plt.xlabel('Gender')
# plt.ylabel(avg_income_by_gender)
# plt.xticks(rotation = 0)
# plt.show()


# check age b/w 20-30 earn , 30-40 eran ...
# print(df.Age.describe())
# bin1 = [20,30,40,50,60]
# label1 = ['20-30','31-40','41-50','51-60']
# df['Age_group']= pd.cut(df["Age"],bins=bin1, labels=label1, right=True)
# age_vs_income = df.groupby('Age_group')['Salary'].mean()
# print(age_vs_income)

# age_vs_income.plot(kind='bar',color = 'Green')
# plt.xlabel('Age_group')
# plt.ylabel('Salary')
# plt.xticks(rotation=0)
# plt.show()
