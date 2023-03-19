# Ex-01_DS_Data_Cleansing
# AIM:
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation:
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM:

## STEP 1:
Read the given Data

## STEP 2:
Get the information about the data

## STEP 3:
Remove the null values from the data

## STEP 4:
Save the Clean data to the file

# CODE:
~~~py
import pandas as pd
df=pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
~~~

## OUPUT:
DATA:
![o1](https://user-images.githubusercontent.com/121418437/226157050-2bb0624b-b472-4bf7-9393-0263364cd8ae.JPG)
![o2](https://user-images.githubusercontent.com/121418437/226157064-7e4482d8-eb36-4657-b674-214d0039dad8.JPG)

NON NULL :
![o3](https://user-images.githubusercontent.com/121418437/226157090-7f5b42b7-3000-47b0-a108-e843a8d823fe.JPG)
![o4](https://user-images.githubusercontent.com/121418437/226157101-9e33bcd9-0f21-46b3-ace1-7b5041c0cc47.JPG)
![o5](https://user-images.githubusercontent.com/121418437/226157112-ff0746a3-09ea-4675-a6bc-90c0b2ada766.JPG)

MODE:
![o6](https://user-images.githubusercontent.com/121418437/226157131-2ecbfd12-19cc-428a-a02d-cb62c92866f4.JPG)

MEAN:
![o7](https://user-images.githubusercontent.com/121418437/226157146-1490e217-5471-4787-b2d0-ce7043584e17.JPG)

MEDIAN:
![o8](https://user-images.githubusercontent.com/121418437/226157161-ef6e5ace-17f5-4c9a-bd86-3a065ad9197c.JPG)

NON NULL AFTER:
![o9](https://user-images.githubusercontent.com/121418437/226157168-a621fa70-8e97-49ff-92c9-d47cfaed71b7.JPG)
![o10](https://user-images.githubusercontent.com/121418437/226157182-97c10750-a27c-46f7-a51d-bf9598debaec.JPG)

## RESULT:

Thus, the given data is read, cleansed and the cleansed data is saved into the file.



