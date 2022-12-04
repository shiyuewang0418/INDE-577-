# The Single Neuron Linear Regression Model
<img width="818" alt="image" src="https://user-images.githubusercontent.com/119746917/205466043-873d5827-4153-4fa3-8701-7bfdf8a5f0c8.png">

## Definition
The single neuron model together with the gradient descent algorithm to get the single neuron 
linear regression model in order to solve the linear regression problem.

## Algorithm 
Assume we have an input data set (column vector) $\textbf{X} = (\textbf{x}_1^T, \textbf{x}_2^T, \cdots, \textbf{x}_n^T)$, where $\textbf{x}_i^T = (x_{i1}, x_{i2}, \cdots, x_{ip}) \in \textbf{R}^p$, and want to predict a real-valued output data set (column vector) $\textbf{y} = (y_1, y_2, \cdots, y_n)$ . The linear regression model has the form

$$ y_i = \beta_0 + \sum_{j=1}^{p} {\beta_j x_{ij}} + \epsilon_i $$
Here the $\beta_j’s$ are unknown parameters or coefficients of corresponding input.

To simplify the equation, usually a column of $1$'s are added to the input data matrix, where $\textbf{x}_i^T = (1, x_{i1}, x_{i2}, \cdots, x_{ip})$, and the linear equation becomes

$$ y_i = \textbf{x}_i^T \boldsymbol{\beta} + \epsilon_i $$
Often these n equations are stacked together and written in a matrix form

$$ \textbf{y} = \textbf{X} \boldsymbol{\beta} + \epsilon $$
The linear model either assumes that the regression function $E(Y|X)$ is linear, or that the linear model is a reasonable approximation.

The most popular estimation method is least squares, in which we pick the coefficients $\boldsymbol{\beta} = (\beta_0, \beta_1, . . ., \beta_p)^T$, which minimizes the residual sum of squares

$$ RSS(\boldsymbol{\beta}) = \sum_{i=1}^n {\epsilon_i^2} =\sum_{i=1}^n (y_i - \beta_0 - \sum_{j=1}^{p} {\beta_j x_{ij}})^2 $$
This criterion makes sense if the observations $(\textbf{x}_i, y_i)$ are independent and identically distributed (iid), which means that they are and randomly drawn from the population.

To minimize $RSS(\boldsymbol{\beta})$, first we make the following assumptions:

$E[\epsilon_i]=0$, i.e., $E[y_i]=\textbf{x}_i^T \boldsymbol{\beta}$
$Var[\epsilon_i] = \sigma^2 < \infty$ (homoscedasticity)
$Cov[\epsilon_i, \epsilon_j]=0$ for $\forall i \neq j$, i.e., $\epsilon_i, \epsilon_j$ are uncorrelated,
and $\epsilon_i$ do not depend on $x_i$ .

Rewrite it to matrix form $$ RSS(\boldsymbol{\beta}) = (\textbf{y}-\textbf{X}\boldsymbol{\beta})^T (\textbf{y}-\textbf{X}\boldsymbol{\beta}) $$

Notice that it's a quadratic function with $p+1$ paraeters, take the partial derivative w.r.t $\boldsymbol{\beta}$, we have

$$ \frac{\partial RSS} {\partial \boldsymbol{\beta}} = -2 \textbf{X}^T (\textbf{y}-\textbf{X}\boldsymbol{\beta}) $$$$ \frac{\partial^2 RSS} {\partial \boldsymbol{\beta} \partial \boldsymbol{\beta}^T} = -2 \textbf{X}^T \textbf{X} $$
Assume that $\textbf{X}$ is fully ranked, i.e., $n>p$, then $\textbf{X}^T \textbf{X}$ is positive definite. Set the first partial derivative to $0$, we have $$ \textbf{X}^T (\textbf{y}-\textbf{X}\boldsymbol{\beta}) = \textbf{0} $$

And the solution is $$ \hat{\boldsymbol{\beta}} = (\textbf{X}^T \textbf{X})^{-1} \textbf{X}^T \textbf{y} $$

Note that only when $\textbf{X}$ is fully ranked does the inverse of $\textbf{X}^T \textbf{X}$ exist.

Thus the fitted values of the training inputs are given by

$$ \hat{\textbf{y}} = \textbf{X} \hat{\boldsymbol{\beta}} = \textbf{X} (\textbf{X}^T \textbf{X})^{-1} \textbf{X}^T \textbf{y} $$
To make a prediction given an unobserved input vector $\textbf{x}_0$

$$ \hat{y} = (1, \textbf{x}_0)^T \hat{\boldsymbol{\beta}} $$

## Advantages:

* Best linear unbiased estimator. The least square estimator of linear regression model has great properties. 
  By the Gauss-Markov theorem, the ordinary least squares (OLS) regression produces unbiased estimates that 
  have the smallest variance of all possible linear estimators. This property is called BLUE (Best Linear Unbiased Estimator).

* Simple model. The Linear regression model is the simplest equation using which the relationship between the 
  multiple predictor variables and predicted variable can be expressed, and the ordinary least squares error 
  function is also very simple and straight-forward.

* Computationally friendly. The modeling speed of linear regression is fast as it does not require complicated 
  calculations and runs predictions fast when the amount of data is large.

* Great interpretability of the output. The ability of linear regression to determine the relative influence 
  of one or more predictor variables to the predicted value when the predictors are independent of each other is 
  one of the key reasons of the popularity of linear regression. The model derived using this method can express the 
  what change in the predictor variable causes what change in the predicted or target variable.

## Disadvantages:

* Overly-Simplistic. The linear regression model is too simplistic to capture real world complexity. 
  The linear regression assumes a linear relationship between independent variables and dependent variable, 
  which cannot represent more complex relationships in real world.

* Independence of variables. Assumes that the predictor variables are not correlated which is rarely true. 
  It is important to, therefore, remove multicollinearity (using dimensionality reduction techniques) because 
  the technique assumes that there is no relationship among independent variables. In cases of high multicollinearity, 
  two features that have high correlation will influence each other’s weight and result in an unreliable model.

* Homoscedasticity. The linear regression model assumes that independent variables can represent all expectation and 
  variance of dependent variable (so that $E[\epsilon_i]=0$ and $Var[\epsilon_i] = \sigma^2$), which is always not true 
  because in real world it's hard for people to find exactly all independent variables that affect the dependent variable. 
  Usually people will have input that are dependent and insufficient.
