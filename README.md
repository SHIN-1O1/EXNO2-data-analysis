# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
        import pandas as pd
      import numpy as np
      import matplotlib.pyplot as plt
      import seaborn as sns
      df=pd.read_csv("/content/titanic_dataset.csv")
      df
![image](https://github.com/user-attachments/assets/0a42d89f-fd3e-44e6-a3e0-05663ded9341)

      df.info()
![image](https://github.com/user-attachments/assets/a069b769-b200-42b0-bb10-76c56f701c19)
      
      df.shape
![image](https://github.com/user-attachments/assets/b1e4950c-272f-4a85-afde-57777dd8913c)

      import pandas as pd
      df=pd.read_csv("/content/titanic_dataset.csv")
      df.set_index("PassengerId",inplace=True)
      print(df.set_index)
![image](https://github.com/user-attachments/assets/f84b2b61-f32f-4cc8-9e55-a7cab89eed69)

      df.describe()
![image](https://github.com/user-attachments/assets/b720b795-abcb-49a5-bbdb-72fa13a6fdab)

       df.nunique()
![image](https://github.com/user-attachments/assets/c0be2135-8dec-4baf-8b64-b27187ca6297)

      df["Survived"].value_counts()
![image](https://github.com/user-attachments/assets/7b3d242a-d4fb-4f64-8197-1dbd247073d7)

      per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
      per
![image](https://github.com/user-attachments/assets/93eb2faa-5e15-4242-8815-d6f19077339e)

      sns.countplot(data=df,x="Survived")
![image](https://github.com/user-attachments/assets/b3c33c60-893a-442a-9ce1-81fc6af82422)

      df
![image](https://github.com/user-attachments/assets/f5f2051d-2fae-456d-b7bc-bc6fd8d01c09)
      
      df.Pclass.unique()
![image](https://github.com/user-attachments/assets/93a484ee-91b4-4565-b594-26895a3b1f14)

      df.rename(columns={'sex':'Gender'},inplace=True)
      df
![image](https://github.com/user-attachments/assets/ae91d6cf-a90b-42ba-b9e5-54b884be7a8a)

      import seaborn as sns
      df=pd.read_csv("/content/titanic_dataset.csv")
      sns.catplot(x="Sex",col='Survived',kind="count",data=df,height=5, aspect=.7)
![image](https://github.com/user-attachments/assets/322ef2af-5abb-4b9b-9090-431bf50390a9)

      sns.catplot(x='Survived',hue='Sex',data=df,kind='count')
![image](https://github.com/user-attachments/assets/7fae8e69-b29c-4d21-8bbc-98fb6fff0775)

      df.boxplot(column='Age',by="Survived")
![image](https://github.com/user-attachments/assets/750b686c-cfc1-4de2-b99b-d5fad980a7f8)

      sns.scatterplot(x=df['Age'],y=df["Fare"])
![image](https://github.com/user-attachments/assets/da8fe05c-91b8-4dc9-a5e9-1d0ef4bdd1af)
      
      import matplotlib.pyplot as plt
      fig,ax1=plt.subplots(figsize=(8,5))
      pt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Sex',data=df)
![image](https://github.com/user-attachments/assets/de7fc30d-899f-4b10-bd5d-f3b0237b255c)

      sns.catplot(data=df,col='Survived',x='Sex',hue='Pclass',kind='count')
![image](https://github.com/user-attachments/assets/6b4a938a-0d2c-4508-ad1f-dd4fbe7df56c)

      import seaborn as sns
      corr=df.corr()
      sns.heatmap(corr,annot=True)
![image](https://github.com/user-attachments/assets/f2c1bfbe-2997-4797-96ff-714951fb603f)
      
      sns.pairplot(df)
![image](https://github.com/user-attachments/assets/a7a13cd5-9b56-433d-a59d-fc046632cfd8)

      
# RESULT
##Code are sucessfully executed.
