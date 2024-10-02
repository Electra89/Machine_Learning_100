
# Regression Metrics

## Introduction

Regression metrics are crucial for evaluating the performance of regression models. They help measure the accuracy of predictions, identify errors, and ensure the model's robustness. 

## Regression Metrics

### 1. Mean Absolute Error (MAE)

MAE is the average of the absolute differences between the actual values and the model’s predicted values. It measures the magnitude of errors in a set of predictions, without considering their direction (i.e., it doesn't distinguish between under-predictions and over-predictions).

Formula:


$$
\text{MAE} = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|
$$


Where:

-   **n** = total number of data points
-   $y_i$ = actual value
-   $\hat{y}_i$ = predicted value

**Advantages**:

-   Error is in the same unit as the output column.
-   Robust to outliers.

**Disadvantages**:

-   The modulus graph is not differentiable at zero, which can pose challenges for optimization algorithms.

### 2. Mean Squared Error (MSE)

MSE is the average of the squared differences between the actual and predicted values. Squaring the errors ensures that large errors are penalized more than smaller ones.

Formula:


$$
\text{MSE} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
$$


Where:

- **n** = total number of data points  
-   $y_i$ = actual value
-   $\hat{y}_i$ = predicted value


**Advantages**:

-   Widely used as a loss function; differentiable at zero.
-   Provides a smoother gradient for optimization compared to MAE.

**Disadvantages**:

-   The unit of the error is not the same as the output variable.
-   MSE is more sensitive to outliers, as it squares the errors.

### 3. Root Mean Squared Error (RMSE)

RMSE is the square root of the average of the squared differences between the actual and predicted values. It provides an error metric in the same units as the original output.

Formula:

$$
\text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}
$$

Where:

- **n** = total number of data points  
- $y_i$ = actual value  
- $\hat{y}_i$ = predicted value  


**Advantages**:

-   Error is in the same unit as the output column.
-   Provides an overall estimate of error magnitude.

**Disadvantages**:

-   Not robust to outliers.

### 4. R-squared (R²) – Coefficient of Determination

R-squared measures the proportion of the variance in the dependent variable that is explained by the independent variable(s). It is a key metric in evaluating how well the model fits the data.

Formula:

$$
R^2 = 1 - \frac{\text{SSR}}{\text{SSM}}
$$

Where:
$$
\text{SSR} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
$$
- **SSR** = Sum of squared differences between actual and predicted values.  

$$
\text{SSM} = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
$$

- **SSM** = Total sum of squares (difference between actual values and their mean).  


**Advantages**:

-   Provides a clear metric to evaluate the goodness of fit.
-   Values range from 0 to 1, with values closer to 1 indicating a better fit.

**Disadvantages**:

-   R² always increases or remains constant when new features are added, even if they are irrelevant.

### 5. Adjusted R-squared

Adjusted R-squared is a modified version of R-squared that adjusts for the number of predictors in the model. Unlike R², it accounts for the impact of adding irrelevant variables and penalizes models for including unnecessary features.

Formula:

$$
\text{Adjusted } R^2 = 1 - \frac{(1 - R^2) \cdot (N - 1)}{N - k - 1}
$$

Where:

- **N** = Number of data points.  
- **k** = Number of independent variables in the model.  


**Advantages**:

-   Penalizes the addition of irrelevant predictors, making it a more reliable metric for model evaluation.
-   A better measure for comparing models with different numbers of predictors.

**Disadvantages**:

-   Always less than or equal to R-squared, but more useful in identifying model quality when comparing different models.