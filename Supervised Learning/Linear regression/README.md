# The Single Neuron Linear Regression Model
<img width="818" alt="image" src="https://user-images.githubusercontent.com/119746917/205466043-873d5827-4153-4fa3-8701-7bfdf8a5f0c8.png">

## Definition
The single neuron model together with the gradient descent algorithm to get the single neuron 
linear regression model in order to solve the linear regression problem. 


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

## Dataset
The datasets included this lecture is:

Wheat seed dataset:

Similar to iris dataset. The data set contains seed information belonging to three different wheat varieties: Kama, Rosa and Canadian, represented by 1, 2 and 3 respectively
Link:https://www.kaggle.com/datasets/jmcaro/wheat-seedsuci
