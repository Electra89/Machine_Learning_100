
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