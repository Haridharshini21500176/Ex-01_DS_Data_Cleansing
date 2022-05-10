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


# CODE
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
df.head(10)
df.tail()
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['show_name'].mode()[0])
df['rating']=df['rating'].fillna(df['rating'].mean())
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].median())
df.info()
```
# OUPUT
### BEFORE THE CLEANING OF DATA:
![out1](https://user-images.githubusercontent.com/94168395/167537075-33005277-c196-408b-9e69-cfa30b29b1b4.png)
![out2](https://user-images.githubusercontent.com/94168395/167537430-c57532aa-b19b-4356-849f-60f3350fdc89.png)


### AFTER CLEANING THE DATA:
![out3](https://user-images.githubusercontent.com/94168395/167537475-46118be5-0ddb-426b-80e8-41a507994109.png)

![out4](https://user-images.githubusercontent.com/94168395/167537183-7b07fb34-6e79-465f-9bbe-5ae089ddcec6.png)

# RESULT:
Hence the data is read and cleaned






