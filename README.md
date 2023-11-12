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
![image](https://github.com/niraunjana/ODD2023-Datascience-Ex01/assets/119395610/294a2aa2-653d-49a0-b340-8bbb68ec1000)



