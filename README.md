# DS_exp5
# Ex:05 Feature Generation
# AIM
To read the given data and perform Feature Generation process and save the data to a file.

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

# ALGORITHM
STEP 1 Read the given Data

STEP 2 Clean the Data Set using Data Cleaning Process

STEP 3 Apply Feature Generation techniques to all the feature of the data set

STEP 4 Save the data to the file

# PROGRAM
```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
Data.csv
import pandas as pd
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
BMI.csv file
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2
```
# OUTPUT
For encoding.csv file Initial data:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/e40ad5a2-402b-45c0-9675-3bcf375ade08)


Unique value:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/2d26695c-b378-4d49-9bec-9e765c0adbe6)


Ordinal Encoder:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/da85d391-d57d-4faf-972c-c8ce98bab0bc)


Label Encoder:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/bcc64b5e-6f8b-4c38-9ecc-0df88391a2a7)


Binary Encoder:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/109cf5a7-4774-4d9a-840b-c4bf1625a6f5)


![image](https://github.com/Leela1822/DS_exp5/assets/106167639/0720e423-4083-4eed-a3ee-5fc11f94aaed)


For Data.csv file Initial data:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/ecd63497-de33-4652-b8d3-3ed6979a63e7)


Unique data:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/0d027532-9cff-4a96-a2a8-2c6c8483b88f)


Ordinal Encoder:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/687f9803-2963-49fb-8399-4923da59ca6d)


![image](https://github.com/Leela1822/DS_exp5/assets/106167639/a3f7903e-fe18-4fb7-bb9d-f25ffa96300d)


Label Encoder:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/8bfec247-9c4d-4fe1-91d3-fad1dd510bbe)


Binary Encoder:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/f7c64e10-e5bc-49d2-b4f3-4916bac6baab)


![image](https://github.com/Leela1822/DS_exp5/assets/106167639/8fef5ac7-52e6-4539-99cb-7c5068cf4bd6)


For bmi.csv file Initial data:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/f1ed8146-f152-40ac-b6f2-4b5a8055bd95)


Binary Encoders:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/ba8e3b20-b03b-430f-87b5-3a88f7c0dd39)


Dummies:

![image](https://github.com/Leela1822/DS_exp5/assets/106167639/237c2ffc-850a-40e9-bb7f-5341bebdb2a5)


# RESULT:
The Feature Generation process was performed and saved the data to a file.
