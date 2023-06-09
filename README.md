# **Ex-02-OUTLIER**

# AIM

To read the given data and remove the outliers present in it using IQR.

# ALGORITHM

(1) Remove outliers using IQR

(2) After removing outliers in step 1, you get a new dataframe.

(3) use zscore of 3 to remove outliers. This is quite similar to IQR and you will get exact same result

(4) for the data set height_weight.csv find the following

(i) Using IQR detect weight outliers and print them

(ii) Using IQR, detect height outliers and print them
# CODE
#get the data
data = pd.read_csv('/content/gdrive/MyDrive/Bengaluru_House_Data.csv')
data.head(10)

df=pd.DataFrame(data)
median=df.quantile(0.5)
Q1 = df.quantile(0.25)
Q3 = df.quantile(0.75)
IQR = Q3-Q1
print(IQR)

low=Q1-1.5*IQR
high=Q3+1.5*IQR
df1=df[((df>=Q1-1.5*IQR)&(df<=Q3+1.5*IQR))]
print(df1)

#get the data
data = pd.read_csv('/content/gdrive/MyDrive/height_weight.csv')
data.head(10)

df=pd.DataFrame(data)
median=df.quantile(0.5)
Q1 = df.quantile(0.25)
Q3 = df.quantile(0.75)
IQR = Q3-Q1
print(IQR)

low=Q1-1.5*IQR
high=Q3+1.5*IQR
df1=df[((df>=Q1-1.5*IQR)&(df<=Q3+1.5*IQR))]
print(df1)


#get the data
data = pd.read_csv('/content/gdrive/MyDrive/heights.csv')
data.head(10)

df=pd.DataFrame(data)
median=df.quantile(0.5)
Q1 = df.quantile(0.25)
Q3 = df.quantile(0.75)
IQR = Q3-Q1
print(IQR)

low=Q1-1.5*IQR
high=Q3+1.5*IQR
df1=df[((df>=Q1-1.5*IQR)&(df<=Q3+1.5*IQR))]
print(df1)

# output
![h1](https://user-images.githubusercontent.com/107982953/227729520-c488f781-570f-4bbe-945e-08d72c81fd3e.png)
![h2](https://user-images.githubusercontent.com/107982953/227729584-bce75112-c643-43fa-b871-7280b351f648.png)
![h3](https://user-images.githubusercontent.com/107982953/227729635-12fefbf9-a608-4596-92f2-c0e5049587a9.png)

![h4](https://user-images.githubusercontent.com/107982953/227729725-bf56add5-d3a0-4cdf-8303-69fa53e81c0e.png)
![h5](https://user-images.githubusercontent.com/107982953/227729768-5f6407ec-7ec5-49a6-80ba-6e8a7b565648.png)
![h6](https://user-images.githubusercontent.com/107982953/227729823-05cb2c90-ed55-4afb-9fc3-9f1fd6e31dd1.png)

# RESULT
Thus, we have successfully removed the outliers using IQR method.
