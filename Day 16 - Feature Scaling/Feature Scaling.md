# Feature Scaling

<br>

**Feature Scaling** is a technique to standardize the independent features present in the data in a fixed range

## Types of Feature Scaling 

### > Standardization - 
**Standardization** (also known as **Z-score normalization**) is a preprocessing step in data analysis and machine learning that involves transforming data to have a **mean of 0** and a **standard deviation of 1**. This process ensures that the data is on the same scale, which can improve the performance of many machine learning algorithms.
### Why is it Called Z-score?

The term **Z-score** comes from statistics and refers to the number of standard deviations a data point is from the mean of the distribution. The formula for calculating a Z-score is:

$$ z = {x -  \mu  \over  \sigma} $$

Where:
-   Z is the Z-score.
-   X is the original data point.
-   μ is the mean of the data.
-   σ is the standard deviation of the data.

#### When to use Standardization ?
![](https://miro.medium.com/v2/resize:fit:700/0*pF6aefM2Xy7r-3cH.png)

- **Distance-Based Algorithms**: Algorithms like k-nearest neighbors (KNN) and support vector machines (SVM) rely on distance measurements. Standardization ensures that features contribute equally to the distance computation.
- **Gradient Descent-Based Algorithms**: Algorithms such as linear regression, logistic regression, and neural networks benefit from standardization because it helps with faster convergence during optimization.
<br>
#### When Not to Use Standardization ?
-   **Tree-Based Models**: Algorithms like decision trees, random forests, and gradient boosting trees do not require standardization because they are not based on distance measurements.
-   **Interpreting Raw Values**: If the interpretation of raw values is crucial, standardization may obscure the original scale and make interpretation difficult.
### > Normalization  - 
**Normalization** is a technique often applied as part of data preparation for machine learning. The goal of normalization is to change the values of numeric columns in the dataset to use a common scale, without distorting differences in the ranges of values or losing information
- ### Common Normalization Techniques
	-   ### Min-Max Normalization

	**Formula**:
	 $$X' = \frac{X_i - X_{\text{min}}}{X_{\text{max}} - X_{\text{min}}}$$

	**Description**: Scales the data to a fixed range, usually [0, 1].

	**Use Case**: When you need a bounded range for all features, especially useful when the algorithm does not assume any distribution of the data (e.g., neural networks).

	- ### Max-Abs Scaling

	**Formula**:
	$$X'_i = \frac{X_i}{|X_{\text{max}}|}$$

	**Description**: Scales each feature by its maximum absolute value, resulting in values in the range [-1, 1].

	**Use Case**: Useful for data that is already **centered at zero and sparse data**, since it does not shift/center the data.

	- ### Robust Scaling

	**Formula**: 
	$$X'_i = \frac{X_i - \text{median}(X)}{\text{IQR}(X)} $$
	- where IQR is the interquartile range (75th percentile - 25th percentile).

	**Description**: Scales the data according to the median and IQR, which makes it robust to outliers.

	**Use Case**: When your **data contains outliers** and you want to reduce their influence.

	- ### Mean Normalization

	**Formula**:
	$$ X'_i = \frac{X_i - \mu}{X_{\text{max}} - X_{\text{min}}}$$

	**Description**: Centers the data around the mean, with values scaled between -1 and 1.

	**Use Case**: When you need to center the data while also scaling it, commonly used in scenarios where **zero-centered data is required.**
	
<br>

#### When to Use Normalization?

Normalization is particularly useful in the following scenarios:

1.  **Machine Learning Algorithms**: Distance-based algorithms (e.g., KNN, SVM) and gradient-based algorithms (e.g., logistic regression, neural networks) benefit from normalized data.
2.  **Feature Scaling**: When different features have different units or scales, normalization ensures they contribute equally to the model.
3.  **Convergence**: For gradient descent-based optimization, normalized data can lead to faster convergence and better performance.

#### When Not to Use Normalization?

-   **Tree-Based Models**: Decision trees, random forests, and gradient boosting machines do not require normalization since they are not based on distance or gradient descent.
-   **Data with Inherent Scales**: If the data has meaningful inherent scales (e.g., counts, binary variables), normalization may not be appropriate.

>## Normalization VS Standardization 
-   **Range**:
    
    -   Normalization scales data to a fixed range (e.g., [0, 1]).
    -   Standardization scales data to a mean of 0 and a standard deviation of 1.
-   **Outliers**:
    
    -   Normalization can be influenced by outliers since it uses the minimum and maximum values.
    -   Standardization is less sensitive to outliers because it centers the data around the mean and scales based on standard deviation.
-   **Application Examples**:
    
    -   **Normalization**: k-NN, neural networks.
    -   **Standardization**: PCA (Principal Component Analysis), SVM, linear regression.