# Multiple Linear Regression Mathematical Formulation

 

<br>

![MLR](https://miro.medium.com/v2/resize:fit:1076/1*STo4xuaX_Sr4LliKLYx6Uw.gif)
 
<br>

& \cdots
$$
\hat{y}= \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \beta_3 X_3  \cdots + \beta_n X_n
$$

Y = Dependent variable / Target variable

β0 = Intercept of the regression line

β1, β2, β3, .... βn = Slope of the regression line which tells whether the line is increasing or decreasing

X1, X2, X3, .... Xn = Independent variable / Predictor variable

<br>

$$
\hat{y}= \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \beta_3 X_3
$$


```math
\begin{bmatrix}
\hat{y}_1 \\
\hat{y}_2 \\
\vdots \\
\hat{y}_{100}
\end{bmatrix} =
\begin{bmatrix}
\beta_0  & \beta_1 X_{11} & \beta_2 X_{12} & \beta_3 X_{13} \\
\beta_0 & \beta_1 X_{21} & \beta_2 X_{22} & \beta_3 X_{23} \\
\vdots & \vdots & \vdots & \vdots \\
\beta_0 & \beta_1 X_{100 \times1} & \beta_2 X_{100 \times2} & \beta_3 X_{100 \times3}
\end{bmatrix}
```



 

<br>

 

####  For n rows and m cols

 

```math
\begin{bmatrix}

\hat{y}_1 \\

\hat{y}_2 \\

\vdots \\

\hat{y}_{n}

\end{bmatrix} =

\begin{bmatrix}

\beta_0 & \beta_1 X_{11} & \beta_2 X_{12} & \beta_2 X_{13}& \cdots & \beta_m X_{1m} \\

\beta_0 & \beta_1 X_{21} & \beta_2 X_{22} & \beta_2 X_{23}& \cdots & \beta_m X_{2m} \\

\vdots & \vdots &\vdots &\vdots & \ddots & \vdots \\

\beta_0 & \beta_1 X_{n1} & \beta_2 X_{n2} & \beta_2 X_{n3}& \cdots & \beta_m X_{nm}

\end{bmatrix}
```

 

```math
= \begin{bmatrix}

1& X_{11} & X_{12} & X_{13}& \cdots & X_{1m} \\

1& X_{21} & X_{22} & X_{23} & \cdots & X_{2m} \\

\vdots & \vdots & \vdots & \vdots & \ddots & \vdots \\

1& X_{n1} & X_{n2} & X_{n3}& \cdots & X_{nm}

\end{bmatrix}

\begin{bmatrix}

\beta_0 \\

\beta_1 \\

\beta_2 \\

\vdots \\

\beta_m

\end{bmatrix}
```

 

$$
\boxed{\hat{Y} = X \beta}
$$




$$
e = y - \hat{y}
$$

 

```math
e = \begin{bmatrix}

y_1 \\

y_2 \\

\vdots \\

y_n

\end{bmatrix} -

\begin{bmatrix}

\hat{y}_1 \\

\hat{y}_2 \\

\vdots \\

\hat{y}_n

\end{bmatrix}
```

 

```math
e = \begin{bmatrix}

(y_1 - \hat{y}_1 )\\

(y_2 - \hat{y}_2 )\\

\vdots \\

(y_n - \hat{y}_n)

\end{bmatrix}
```

 

<br>

 

##

 

> In simple linear regression loss / error function.

 

$$\boxed{\text{E} =  \sum_{i=1}^{n} ( y_i - \hat{y}_i)^2} $$

 

$$\therefore  E = e ^T e $$

 

```math
E = \begin{bmatrix}

(y_1 - \hat{y}_1) & (y_2 - \hat{y}_2) & \cdots &( y_n - \hat{y}_n)

\end{bmatrix}_{(1 \times n)}

\begin{bmatrix}

(y_1 - \hat{y}_1 )\\

(y_2 - \hat{y}_2) \\

\vdots \\

(y_n - \hat{y}_n)

\end{bmatrix}_{(n \times 1)}
```

 

>If we perform metrics multiplication

 

$$
E = \begin{bmatrix}
(y_1 - \hat{y}_1)^2 & (y_2 - \hat{y}_2)^2  & \cdots &( y_n - \hat{y}_n)^2
\end{bmatrix}
$$

 

> In summation form we'll be getting

 

$$\text{E} =  \sum_{i=1}^{n} ( y_i - \hat{y}_i)^2 $$

 

##

 

$$ E = e ^T e $$

 

$$ E = ( y- \hat{y}) ^T \cdot ( y_ - \hat{y}) $$

 

$$ E = ( y^T- \hat{y}^T) \cdot ( y_  -  \hat{y}) $$

 

$$ E = [( y^T- ( X \beta)^T)] \cdot( y_  -  ( X \beta)) $$

 

$$
E =  y^T y - \underline{y^T (X \beta)} - \underline{(X \beta)^T y} + (X \beta)^T (X \beta)
$$

 

## Detour

 

$$ y^T (X \beta) = (X \beta)^T y $$

 

$$\therefore y = A \\
\therefore X \beta  = B  $$

 

$$ A^T B = B^T A $$

 

$$\therefore (A^T B)^T  =  B^T A      $$  

 

> By referring above eqn

 

$$ A^T B = (A^T B)^T $$

 

$$\therefore A^T B = C$$

 

$$ C = C^T $$

 

$$ (y^T_ {(1 \times n)}(X_{n \times (m+1)} \beta)_{ (m+1) \times n })^T = y^T(X \beta) $$

 

> Hence output is scalar  quantity so both eqn are same  

 

##

 

$$
E =  y^T y - \underline{y^T (X \beta)} - \underline{(X \beta)^T y} + (X \beta)^T (X \beta)
$$

 

$$
E =  y^T y - \underline{2y^T (X \beta)} + \beta^T X^T  (X \beta)
$$

 

$$
\frac{\partial E}{\partial \beta} = 0
$$

 

$$
\frac{\partial }{\partial \beta}   [y^T y - 2y^T (X \beta) + \beta^T X^T  (X \beta)] = 0
$$

 

$$
\frac{\partial }{\partial \beta}(y^T y) - \frac{\partial }{\partial \beta}(2y^T (X \beta)) + \frac{\partial }{\partial \beta}(\beta^T X^T  (X \beta) )= 0
$$

 

$$
0 - 2y^T X + \frac{\partial }{\partial \beta}(\beta^T X^T  X \beta )= 0
$$

 

>> add photo differentiation

 

$$
0 - 2y^T X +2  X^T  X \beta^T= 0
$$

 

$$
 2  X^T  X \beta^T = 2y^T X
$$

 

$$
 \beta^T = y^T X (X^T  X)^{-1}
$$

 

$$
 (\beta^T)^T = [y^T X (X^T  X)^{-1}]^T
$$

 

$$
 \beta=[(X^T  X)^{-1}]^T(y^T X)^T
$$

 

$$
 \boxed{\beta=(X^T  X)^{-1}X^Ty}
$$