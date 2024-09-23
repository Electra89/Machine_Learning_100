
#   Outliers in Machine Learning

<br>

## What Are Outliers?

Outliers are data points that differ significantly from other observations in a dataset. They can skew and mislead the interpretation of results in machine learning algorithms, particularly in models sensitive to outliers, This is particularly true for algorithms that **rely on weighted data points**, such as linear regression, logistic regression, and ensemble methods like AdaBoost.

## How to Treat Outliers

1.  **Trimming**: This involves removing outliers from the dataset. While this can lead to a cleaner dataset, it may also reduce the overall data volume.
    
2.  **Capping**: this method sets boundaries on both ends of the data, replacing outliers with values at the specified percentiles.
    
3.  **Missing Value Treatment**: Outliers can be treated as missing values, allowing for imputation techniques to fill them in based on the rest of the data.
    
4.  **Discretization**: Transforming continuous variables into categorical ones can mitigate the influence of outliers by grouping values.
    

## How to Detect Outliers

1.  **Normal Distribution**: In a normally distributed dataset, points that lie outside the range of μ±3σ\mu \pm 3\sigmaμ±3σ are typically considered outliers.
    
2.  **Skewed Distribution**: For skewed data, the Interquartile Range (IQR) method is often employed. Here, outliers are defined as points that fall **below Q1−1.5×IQR** or **above Q3+1.5×IQR**
    
3.  **Other Distributions**: For non-normal distributions, the percentile approach can be used, identifying outliers based on specific percentile thresholds.
    

## Techniques for Outlier Detection and Removal

1.  **Z-Score Treatment**: This method requires the data to be normally distributed. The Z-score indicates how many standard deviations an element is from the mean:
    
   $${μ ± σ=68.2\%}\\
   {μ±2σ=95.4\%}\\
   {μ±3σ=99.7\% }$$

   - Points outside these boundaries are considered outliers and can be removed.
2.  **IQR-Based Filtering**:
    
    -   Calculate **Q1 (25th percentile)** and **Q3 (75th percentile)**.
    -   Compute IQR: **IQR = Q3 − Q1**
    -   Identify outliers: Values **below Q1−1.5×IQR** or **above Q3+1.5×IQR** are considered outliers.
    
3.  **Percentile-Based Capping (Winsorization)**: In this approach, outliers are capped at specified percentile values, preventing extreme values from skewing the analysis.

