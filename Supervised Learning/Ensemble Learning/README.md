# Ensemble Learning
<img width="510" alt="image" src="https://user-images.githubusercontent.com/119746917/205471218-676a1c0e-0b5c-4814-bd1c-6b269e903c08.png">

## Definition
is a group of predictors, and it makes decision by majority vote for classification (hard voting classifier) and 
averaging for regression. It's a kind of Supervised learning, which uses multiple learning algorithms to obtain 
better predictive performance than could be obtained from any of the constituent learning algorithms alone. Unlike 
a statistical ensemble in statistical mechanics, which is usually infinite, a machine learning ensemble consists of 
only a concrete finite set of alternative models, but typically allows for much more flexible structure to exist among 
those alternatives.

# Radom Forest
<img width="634" alt="image" src="https://user-images.githubusercontent.com/119746917/205471351-a2c32026-4c26-4716-9fa1-166c7c8b40e5.png">

## Definition
Briefly, random forest is a kind of ensemble learning which all learners are decision trees and each decision tree uses 
training data sample from bootstrap aggregating. It was first proposed by Ho in 1995.


Random forest is a great ensemble learning model, since each weak learner (a decision tree) is super easy and fast to train, 
and by bootstrap aggregating and other methods (like selecting a subset of features in each split), each decision tree is 
highly uncorrelated, so the results of weak learners are uncorrelated, but the majority vote or average prediction is good.

## Advantages
* Good performance on a large amont of tasks (except images data set).
* Running fast
* General to almost all kinds of classification and regression problems.
* Accept both numeric and categorical data.
* Can deal with missing data and no need of normalization.
* Easy to interprete feature importance

## Disadvantages
* May face a high overfitting risk
* Parameter turning is needed.
* Cannot deal with categoric data with levels


