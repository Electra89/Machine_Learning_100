# Understanding Dataset
<br>

 ## 1.  How big is the data ?
 **To check the size of the dataset:**
 
    df.shape
> This returns the number of rows and columns in the dataset.

 ## 2.   How does the data look like?
 **To get a quick look at a random sample of the data:**
 
    df.sample(5) 
   > This displays 5 random rows from the dataset.
    
 ## 3.  What is the data type of cols? 
 **To see the data types of each column:**

    df.info()
  > This provides information about the data types and non-null counts for each column.

 ## 4.  Are there any missing values?
 **To identify missing values in the dataset:**
 
    df.isnull().sum()
   > This shows the count of missing values in each column.
	
 ## 5.  How does the data look mathematically?
 **To get descriptive statistics of the dataset:**
 
    df.describe()
  > This provides a summary of the central tendency, dispersion, and shape of the dataset’s distribution.

 ## 6.   Are there duplicate values?
 **To find duplicate rows in the dataset:**
 
    df.duplicated().sum()
  > This returns the number of duplicate rows.
    
 ## 7.  How is the correlation between cols?
 **To check the correlation between columns:**
 
    df.corr()
  > This produces a correlation matrix showing the pairwise correlations between columns in the dataset.

   
