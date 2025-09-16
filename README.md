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
```
import pandas as pd 
import numpy as np
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
df

```
<img width="1398" height="621" alt="Screenshot 2025-09-15 113946" src="https://github.com/user-attachments/assets/c31fbffa-b075-4596-b236-b694f3818e2b" />

```
df.info()

```
<img width="607" height="509" alt="Screenshot 2025-09-15 114128" src="https://github.com/user-attachments/assets/6ebba507-dc4f-4626-bc37-ad6c34f9d963" />

```
df.describe()

```
<img width="1018" height="444" alt="image" src="https://github.com/user-attachments/assets/202354df-fb0f-4c6a-8d63-f8bcc7fca890" />

```

df.dtypes

```
<img width="367" height="595" alt="Screenshot 2025-09-15 114313" src="https://github.com/user-attachments/assets/7680b94f-d247-4a21-9977-37a5310aec81" />

```

df.shape

```

<img width="220" height="98" alt="Screenshot 2025-09-15 114404" src="https://github.com/user-attachments/assets/c2ff33ad-d8fc-4f65-bc75-06059dbe489c" />

```

df.value_counts()

```

<img width="1674" height="666" alt="Screenshot 2025-09-15 114512" src="https://github.com/user-attachments/assets/1d8fc77a-3526-4d11-8980-2c4be0ecfac4" />

```

df['Age'].value_counts()

```

<img width="526" height="656" alt="Screenshot 2025-09-15 114557" src="https://github.com/user-attachments/assets/501c92c4-e539-45f4-bdb9-90c81418c3c4" />

```
df.set_index("PassengerId",inplace=True)
df

```

<img width="1706" height="642" alt="Screenshot 2025-09-15 114655" src="https://github.com/user-attachments/assets/a7e9e5cb-9512-4d37-addf-378820eaf9cd" />

```

  df.nunique()

```

<img width="480" height="571" alt="Screenshot 2025-09-15 114752" src="https://github.com/user-attachments/assets/8dbbcd82-fbcf-4a09-a0f6-0a6ff508cde4" />

```

sns.countplot(data=df,x='Age')

```

<img width="1403" height="649" alt="Screenshot 2025-09-15 114844" src="https://github.com/user-attachments/assets/70d8c3a9-3cc8-40cc-8f57-b088597963c7" />

```
df.rename(columns={'Sex':'Gender'},inplace=True)
df

```


<img width="1642" height="653" alt="Screenshot 2025-09-15 114933" src="https://github.com/user-attachments/assets/15d8f0ad-6e27-419a-b358-cf97399c45f1" />

```

sns.catplot(x='Gender',col='Survived',kind="count",data=df,height=5,aspect=1)

```

<img width="1491" height="719" alt="Screenshot 2025-09-15 115037" src="https://github.com/user-attachments/assets/94cadd27-cf7b-4b45-9586-a86ded0a9a40" />


```

df.boxplot(column='Age',by='Survived')
df

```


<img width="1477" height="599" alt="Screenshot 2025-09-15 115130" src="https://github.com/user-attachments/assets/4b368cd2-5a6b-482d-83e8-341f32f675f8" />


```

sns.scatterplot(x=df['Age'],y=df['Fare'])

```

<img width="957" height="611" alt="Screenshot 2025-09-15 115225" src="https://github.com/user-attachments/assets/16106fe1-9ad1-4cf1-b5ec-686acb88906f" />

```

plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)

```

<img width="917" height="605" alt="Screenshot 2025-09-15 115310" src="https://github.com/user-attachments/assets/2e74789b-47ca-459d-80b0-3d4e080ef43c" />

```

sns.catplot(x='Pclass',y='Age',hue='Gender',col='Survived',kind='box',data=df)

```

<img width="1647" height="733" alt="Screenshot 2025-09-15 115357" src="https://github.com/user-attachments/assets/458ab0f3-1cfe-41fb-abbd-ab067acd16e2" />

```
corr=df.corr(numeric_only=True)
sns.heatmap(corr,annot=True)

```

<img width="1039" height="691" alt="Screenshot 2025-09-15 115500" src="https://github.com/user-attachments/assets/06660061-bb7a-4d16-9099-9bca2e781b0f" />

# RESULT
Exploratory Data Analysis on the given data set is successful
        
