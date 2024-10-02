
# Simple Linear Regression

## Introduction

Linear Regression is a widely used supervised machine learning algorithm designed to solve regression problems, where the goal is to predict a numerical output based on one or more input variables. It is a fundamental tool in statistics and machine learning, useful in situations where the relationship between the variables can be approximated as linear.

## What is Linear Regression?

Linear Regression aims to model the relationship between the dependent variable (output) and one or more independent variables (input) by fitting a linear equation to the observed data. The simplest form of this relationship can be written as:



Copy code

`y = b0 + b1 * x` 

Where:

-   `y`: The dependent variable (the output we are trying to predict).
-   `x`: The independent variable (the input or predictor).
-   `b0`: The intercept term (the value of `y` when `x` is zero).
-   `b1`: The slope (the change in `y` for a unit change in `x`).

The goal of linear regression is to determine the best values for `b0` and `b1` such that the model accurately predicts the output `y` based on input `x`, while minimizing the error or difference between the predicted and actual values.

![Linear Regression Graph](https://miro.medium.com/v2/resize:fit:506/1*Y34IA0vHuu2SWBWPW7Vb6Q.png)

## Types of Linear Regression

1.  **Simple Linear Regression**:
    
    -   This involves only one independent variable and one dependent variable.
    -   It predicts the dependent variable using a single feature or predictor by fitting a straight line through the data points.
2.  **Multiple Linear Regression**:
    
    -   This involves more than one independent variable, and one dependent variable.
    -   The model predicts the output by considering the combined effect of several predictors. The equation extends to include additional coefficients for each input variable.
3.  **Polynomial Linear Regression**:
    
    -   A form of regression where the relationship between the independent and dependent variables is modeled as an nth-degree polynomial.
    -   Though it uses linear techniques, the equation is no longer a straight line but a curve, allowing it to handle more complex relationships.

<br>

##  Mathematical Formulation

![](https://miro.medium.com/v2/resize:fit:640/1*iXW_mkBpC1S9tbon543GxQ.jpeg)

$$Error = d_1 + d_2 + d_3  ...+ d_n$$ 
$$Error = d^2_1 + d^2_2 + d^2_3  ...+ d^2_n$$

#### why squared error ?

 1. Penalized outlier 
 2. Differentiation

$$\text{Error} =  \sum_{i=1}^{n} ( d^2_i )$$ 

- Error is also called as loss / error function.

$$\text{Error} =  \sum_{i=1}^{n} ( y_i - \hat{y}_i)^2 $$ 


$$\therefore     y = mx + b$$

$$\text{Error} =  \sum_{i=1}^{n} ( y_i - (mx_i + b))^2$$ 

$$\text{E(m,b)} = \sum_{i=1}^{n} ( y_i - (mx_i + b))^2$$ 

$$\text{E(m,b)} =  \sum_{i=1}^{n} ( y_i - mx_i - b))^2$$ 

$$\therefore  Let \hspace{3pt}m = 0$$

$$\text{E(b)} =  \sum_{i=1}^{n} ( y_i -x_i - b))^2$$ 

--



### 1. Partial Derivative with respect to $b$ and equate with 0 :

$$
\frac{\partial E}{\partial b} = \frac{\partial}{\partial b} \sum_{i=1}^{n} (y_i - mx_i - b)^2 = 0
$$

Using the chain rule:

$$
  \frac{\partial}{\partial b} \sum_{i=1}^{n} (y_i - mx_i - b)^2 = 0
$$

$$
 \sum_{i=1}^{n} -2 (y_i - mx_i - b) \frac{\partial}{\partial b} (y_i - mx_i - b) = 0
$$
 
 $$
\sum_{i=1}^{n} -2 (y_i - mx_i - b)  (-1) = 0
$$

Dividing both side  by **-2** for simplification

$$
\sum_{i=1}^{n} (y_i - mx_i - b) = 0
$$

$$
\sum_{i=1}^{n} y_i  -m \sum_{i=1}^{n} x_i -  \sum_{i=1}^{n}b = 0
$$

Dividing by **n** for simplification

$$
 \sum_{i=1}^{n}\frac{y_i}{n}  - m  \sum_{i=1}^{n}\frac{x_i}{n} -  \sum_{i=1}^{n} \frac{b}{n} = \frac{0}{n}
$$

$$ \bar{Y} - m \bar{X} - b = 0 $$

$$ \boxed{b = \bar{Y} - m \bar{X}} $$


### 2. Partial Derivative with respect to $m$ and equate with 0 :

$$
\frac{\partial E}{\partial m} = \frac{\partial}{\partial m} \sum_{i=1}^{n} (y_i - mx_i - b)^2 = 0
$$

$$
  \frac{\partial}{\partial m} \sum_{i=1}^{n} (y_i - mx_i - b)^2 = 0
$$

$$\therefore   b = \bar{Y} - m \bar{X} $$

$$
  \frac{\partial}{\partial m} \sum_{i=1}^{n} (y_i - mx_i - (\bar{Y} - m \bar{X}))^2 = 0
$$

Using the chain rule:

$$
  \frac{\partial}{\partial m}  \sum_{i=1}^{n} (y_i - mx_i - \bar{Y} - m \bar{X})^2 = 0
$$

$$
 \sum_{i=1}^{n} 2 (y_i - mx_i - \bar{Y} - m \bar{X}) \frac{\partial}{\partial m} (y_i - \bar{Y} - mx_i  +m \bar{X}) = 0
$$

$$
 \sum_{i=1}^{n}  2 (y_i - mx_i - \bar{Y} - m \bar{X})  ( - x_i  + \bar{X}) = 0
$$

$$
 \sum_{i=1}^{n} -2 (y_i - mx_i - \bar{Y} - m \bar{X})(x_i   -  \bar{X}) = 0
$$

Dividing both side  by **-2** for simplification

$$
 \sum_{i=1}^{n}  [(y_i - \bar{Y}) - m(x_i  +\bar{X})] (x_i   -  \bar{X}) = 0
$$

$$
 \sum_{i=1}^{n}  (y_i - \bar{Y})(x_i   -  \bar{X}) - m(x_i  +\bar{X})^2 = 0
$$

This simplifies to:

$$
 \sum_{i=1}^{n}  (y_i - \bar{Y})(x_i   -  \bar{X}) - m\sum_{i=1}^{n} (x_i  +\bar{X})^2 = 0
$$

$$
 \sum_{i=1}^{n}  (y_i - \bar{Y})(x_i   -  \bar{X}) = m\sum_{i=1}^{n} (x_i  +\bar{X})^2 
$$

Rearranging gives: 

$$
\boxed{ m = \frac{\sum_{i=1}^{n} (y_i - \bar{Y})(x_i - \bar{X})}{\sum_{i=1}^{n} (x_i - \bar{X})^2}}.
$$
