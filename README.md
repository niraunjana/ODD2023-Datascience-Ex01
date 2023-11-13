# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE and OUTPUT
```
Developed By : Niraunjana Gayathri G R
Ref No.      : 212222230096
```
```
import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
df

df.head()

df.tail()

df.shape

df.describe()

df.info()

df.isnull().sum()

df.dropna(how="any").shape

df.dropna(how="any")

df.dropna(how="all").shape

x=df.dropna(how="all")
x

amt=df.dropna(subset=['LoanAmount'],how='any')
amt

M=df.dropna(subset=['LoanAmount','Loan_Amount_Term'],how='any')
M

df.fillna(0)

df

df.fillna(method='ffill')

df.fillna(method="bfill")

df.interpolate()

mn=df.LoanAmount.mean()
mn

l=df.LoanAmount.interpolate()
l

df.LoanAmount.fillna(mn,inplace=True)
df

df.isnull()

df.notnull()

df.dropna()

df.duplicated()

df.drop_duplicates(inplace=True)
df

md=df.LoanAmount.median()
md

mode=df.LoanAmount.mode()
mode

for x in df.index:
  if df.loc[x,'LoanAmount']>100:
    df.drop(x,inplace=True)
df
```
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/99761dfe-25ae-4aa5-8dbb-8ef4e069da1a)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/121b535a-92ae-4c74-91fa-86b35e12ef14)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/dc0559e2-709d-42cf-816b-a6f2f6822d93)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/149d840d-aada-4d7c-b427-45804e43548c)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/6b3db76f-3113-4d45-bbe8-7a06d783f423)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/6b4a1492-7d37-4cdb-a0db-83c682ac4e37)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/c7f1798b-f6b6-4a6a-9ad7-7655233d079a)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/ea8d68ea-ae48-41d1-b1c6-cd0ae6e35a94)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/81d9fef7-02d1-4942-824b-af746f2b49d0)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/a1264e8f-af7f-49d9-be32-05bab4be588f)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/5231c0bb-7c9e-4c58-9f20-2f0f2cb46ebf)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/fb8f9789-2768-4f22-9536-ceb9688f2e3b)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/626cdb50-1e26-4cee-b729-a7893377f808)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/c61d70c8-5f68-4eb8-afe5-54e7a54b78f7)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/8a51ac93-0287-4666-964a-c7c3e580d786)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/2d22f549-7965-4846-b316-1c1f9ae1dc65)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/3ee4fe33-9e75-4458-8d1b-58733c9213ef)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/a0c0bfe5-9e08-4c68-941c-e3aa16b9ca0a)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/1727400d-784c-4278-bd67-0fd73f6e127a)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/e63e1ca8-6e9c-44f4-9c48-09677f293c8e)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/34f01257-7b33-4df9-b30f-3302bc4b40b9)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/1a99ba82-6ad9-4b9b-a1b0-8b9ca4f87820)
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/bd1c5fe0-0e8d-46bb-9e7d-6f72e4c081df)










