import pandas as pd
df= pd.read_csv("D:\\Programming Fundamentals (LAB)\\dataaaaaaaa.csv")
df.shape
df.info()
# cleaning data
df.dropna()
# replace empty values
df.fillna(44)
# replacing the specific column
df['Sleep Hours'].fillna(999)
df['Grades'].mean() # take out average

df['Grades'].mode()# most common

df['Grades'].median()# middle value
# fixing wrong data
df['Grades']
df.loc[2,'Grades']=56777
# data duplications
df.duplicated()
pd.set_option("display.max_rows",None)
pd.set_option("display.max_columns",None)
#df.drop_duplicates()
df.describe()
# adding a new column in data frame
df['col']=7
df
# Remove a column
df.drop(columns=['col'],inplace=True)
df
# adding a row
a=pd.DataFrame({'study hours':3.4,
                '	Sleep Hours':'Attendance (%)',
                  'Grades':'col'},
                  index=[0])
a
df=pd.concat([a,df])
df
# Remove a row
df.drop(0,inplace=True)
df
# Slicing in code
df[4:7]
df[4:7:2]
df[['study hours']][54:65]
# Flow chart
df['Grades'].value_counts().plot(kind="bar")
df['Grades'].value_counts().plot(kind="barh")
df['Grades'].value_counts().plot(kind="box")
df['Grades'].value_counts().plot(kind="density")
df['Grades'].value_counts().plot(kind="pie")
df['Grades'].value_counts().plot(kind="line")
df['Grades'].value_counts().plot(kind="kde")
df['Grades'].value_counts().plot(kind="hist")
# Data aggregation
df.aggregate(['sum', 'min'])
df['Grades'].sum()
# Standard derivation
df['Study Hours'].std()
# varience calculations
df['Study Hours'].var()
# Data reprocessing
df.isnull().sum()
# Data saving
pip install openpyxl
df = pd.read_csv("D:\\Programming Fundamentals (LAB)\\dataaaaaaaa.csv")
df
df.to_excel("newdata.xlsx", sheet_name="newsheet")
