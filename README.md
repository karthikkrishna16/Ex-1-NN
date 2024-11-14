<H3>ENTER YOUR NAME</H3> TH KARTHIK KRISHNA
<H3>ENTER YOUR REGISTER NO.</H3> 212223240067
<H3>EX. NO.1</H3>
<H3>DATE</H3> 22/08/2024
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
# Data set
```import pandas as pd                                                
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
df=pd.read_csv("/content/Churn_Modelling (2).csv")         
df.head()
```
# Null Values:
```
df.isnull().sum()
df.duplicated().sum()
```
# Normalized Data:
```
df=df.drop(['Surname', 'Geography','Gender'], axis=1)
scaler=StandardScaler()                                             
df=pd.DataFrame(scaler.fit_transform(df))
df.head()
```
# Data Splitting:
```
X,Y=df.iloc[:,:-1].values ,df.iloc[:,-1].values                     
print('Input:\n',X,'\nOutput:\n',Y)
```
# Train and Test Data
```
Xtrain,Xtest,Ytrain,Ytest = train_test_split(X, Y, test_size=0.2)
print("Xtrain:\n" ,Xtrain, "\nXtest:\n", Xtest)                     
print("\nYtrain:\n" ,Ytrain, "\nYtest:\n", Ytest)
```
# OUTPUT:
# Dataset:

![Screenshot 2024-08-23 095158](https://github.com/user-attachments/assets/1c52d3fc-3aa1-4e66-b727-22f28d53af37)

# Null Values:

![Screenshot 2024-08-23 095241](https://github.com/user-attachments/assets/e7378916-e60d-46eb-bea8-b0980cbf194f)

# Normalized Data:

![Screenshot 2024-08-23 110145](https://github.com/user-attachments/assets/3cb3e699-7aea-4cef-990e-da9b07d43505)

# Data Splitting:

![Screenshot 2024-08-23 110226](https://github.com/user-attachments/assets/a6b02b84-0a61-4fd9-9df2-307362cd7e98)

# Train and Test Data:

![Screenshot 2024-08-23 110257](https://github.com/user-attachments/assets/f4e7ebda-33a5-45b1-9abf-7e439262d509)






# RESULT:
Thus, Implementation of Data Preprocessing is done in python using a data set downloaded from Kaggle.


