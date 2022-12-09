# PandasAssignment

Q1. How do you load a CSV file into a Pandas DataFrame?

df=pd.read_csv("file path/link")

Q2. How do you check the data type of a column in a Pandas DataFrame?

df.dtypes

Q3. How do you select rows from a Pandas DataFrame based on a condition?

df.loc[(df['TotalMarks'] >= 50) & (df['TotalMarks'] <= 79)]

Q4. How do you rename columns in a Pandas DataFrame?

df["new_column"]=df["old_column_name"]

Q5. How do you drop columns in a Pandas DataFrame?

df.drop("column_name",axis=1)

Q6. How do you find the unique values in a column of a Pandas DataFrame?

df["column_name"].unique()

Q7. How do you find the number of missing values in each column of a Pandas DataFrame?

df.isna().sum()

Q8. How do you fill missing values in a Pandas DataFrame with a specific value?

data["Gender"].fillna("No Gender", inplace = True)

Q9. How do you concatenate two Pandas DataFrames?

We can concatenate two dataframes using .concate() function 
eg:
data1={'Name':['Vijaya','Harish'],'Age':[23,18],'Address':['Pune','Washim']
      }
data2={'Name':'Radha','Age':25,'Address':'Wardha'}
# Convert the dictionary into DataFrame  
df = pd.DataFrame(data1,index=[0,2])
 
# Convert the dictionary into DataFrame  
df1 = pd.DataFrame(data2, index=[1])
#res=[df,df1]
result_df=pd.concat([df,df1])
result_df     

Q10. How do you merge two Pandas DataFrames on a specific column?


Q11. How do you group data in a Pandas DataFrame by a specific column and apply an aggregation function?


Q12. How do you pivot a Pandas DataFrame?



Q13. How do you change the data type of a column in a Pandas DataFrame?

df = df.astype(required_datatype)

Q14. How do you sort a Pandas DataFrame by a specific column?

df.sort()

Q15. How do you create a copy of a Pandas DataFrame?

df.copy(deep)

Q16. How do you filter rows of a Pandas DataFrame by multiple conditions?

dataFrame.loc[(dataFrame['Salary']>=100000) & (dataFrame['Age']< 40) & (dataFrame['JOB'].str.startswith('D')),['Name','JOB']]

Q17. How do you calculate the mean of a column in a Pandas DataFrame?

# Using multiple columns mean using DataFrame.mean()
df2 = df[["Fee","Discount"]].mean()
print(df2)

# Average of each column using DataFrame.mean()
df2 = df.mean(axis=0)
print(df2)


Q18. How do you calculate the standard deviation of a column in a Pandas DataFrame?

df.std()

Q19. How do you calculate the correlation between two columns in a Pandas DataFrame?

dataframe[‘first_column’].corr(dataframe[‘second_column’])

Q20. How do you select specific columns in a DataFrame using their labels?

df['hue']

Q21. How do you select specific rows in a DataFrame using their indexes?

df.iloc[[2, 3, 4]]
or 
df.loc[[2, 3, 4]]

Q22. How do you sort a DataFrame by a specific column?

df.sort_values()

Q23. How do you create a new column in a DataFrame based on the values of another column?

df['colG'] = df.apply(lambda row: row.colC + row.colE, axis=1)

Q24. How do you remove duplicates from a DataFrame?

df.drop_duplicates(subset="First Name", keep=False, inplace=True)

Q25. What is the difference between .loc and .iloc in Pandas?

The loc() function is label based data selecting method which means that we have to pass the name of the row or column which we want to select. This method includes the last element of the range passed in it, unlike iloc(). loc() can accept the boolean data unlike iloc().

The iloc() function is an indexed-based selecting method which means that we have to pass an integer index in the method to select a specific row/column. This method does not include the last element of the range passed in it unlike loc(). iloc() does not accept the boolean data unlike loc(). 
