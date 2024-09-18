#  Handling Missing Data

<br>

## Complete case analysis (CCA)
Complete-case analysis (CCA), also called "list-wise deletion" of cases, consists in discarding **observations**(Rows) where values in any of the **variables**(Columns) are missing. 
Complete Case Analysis means literally analyzing only those observations for which there is information in all of the variables in the dataset.
This method involves excluding rows with missing values from the dataset. It is simple and straightforward but can lead to significant data loss, especially if missing values are frequent.

- Assumption for CCA :- 
	- Missing completely as random (**MCAR**)

- Advantages :-
	1. Easy to implement as no data manipulation required
	2. Preserves variable distribution (if data is MCAR, then the distribution of the variables of the reduced dataset should match the distribution in the original dataset.

- Disadvantage :- 
	1.	It can exclude a large fraction of the original dataset (if missing data is abundant)
	2.	Excluded observations could be informative for the analysis (if data is not missing at random)
	3.	When using our models in production, the model will not know how to handle missing data
- When to use CCA :
	- MCAR
	- Data > 5% missing




## Imputation

### Univariate

-   **Numerical Data:**
    
    -   **Mean/Median:** Replace missing values with the mean or median of the column. This method is easy to implement and works well when data is symmetrically distributed.
    - **Arbitrary Value Imputation:** This method involves replacing missing values with a constant or arbitrary value that is not present in the original data (e.g., -1, 99, 0 or a specific number). Arbitrary value imputation is useful when you want to clearly distinguish imputed values from actual data. This technique will perform when data is not randomly missing.
    **End of Distribution Imputation:** Impute missing values using extreme values in the distribution. For a normally distributed data, use mean ± 3σ (three standard deviations from the mean). If the data is skewed, apply the IQR proximity rule, using Q1 - 1.5 IQR for lower extremes and Q3 + 1.5 IQR for upper extremes. This method is effective for flagging missing data with values that are significantly different from the rest of the dataset.
   
    
-   **Categorical Data:**
    
    -   **Mode:** Replace missing values with the most frequent value in the column. This method preserves the common category but may skew the distribution if the mode is overly frequent.
    -   **Missing Value Indicator:** Create a new category labeled 'Missing' to explicitly mark the absence of data. This can be useful for algorithms that can handle categorical features well.
 
- **Random Value Imputation:** Fill missing values with random values from the same column, which helps maintain the original distribution but introduces some randomness to the data. This method can be used for both **numerical and categorical** data but is best suited for linear algorithms. However, be cautious, as this approach can change the covariance structure of the data.

### Multivariate

-   **KNN Imputer:** Uses the k-nearest neighbors algorithm to impute missing values by averaging the values of the nearest data points. This method considers the relationships between features but can be computationally intensive.
-   **Iterative Imputer (MISE) :** Uses an iterative approach to predict and replace missing values based on a multivariate model (Multivariate Imputation by Chained Equations). It can capture complex relationships between features but may require more computational resources and fine-tuning.