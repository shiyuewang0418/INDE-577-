# Ensemble Learning
<img width="510" alt="image" src="https://user-images.githubusercontent.com/119746917/205471218-676a1c0e-0b5c-4814-bd1c-6b269e903c08.png">

## Definition
It is a group of predictors, and it makes decision by majority vote for classification (hard voting classifier) and 
averaging for regression. It's a kind of Supervised learning, which uses multiple learning algorithms to obtain 
better predictive performance than could be obtained from any of the constituent learning algorithms alone. Unlike 
a statistical ensemble in statistical mechanics, which is usually infinite, a machine learning ensemble consists of 
only a concrete finite set of alternative models, but typically allows for much more flexible structure to exist among 
those alternatives.

## Algorithm 
The algorithm of ensemble learning is really simple: take the majority vote (for classification) or average (for regression) of all weak learners, as the prediction of ensemble learning model. Weak learners could be any kinds of machine learning models, so ensemble learning is quite flexible.

But there's a key problem for ensemble Learning: learners of ensemble learning should not be similar wit each other, or there's no difference between only use one learner. That's to say, learners should be uncorrelated. This is very similar to the diversity opinion these days, as people from different religions, cultures and so on may have very different ideas, but together team with high diversity could do a good job.

To deal with this peoblem, bootstrap aggregating is a good way to reduce the correlation of training data among different learners.

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

## Dataset
The datasets included this lecture is:

Wheat seeds dataset:

Similar to iris dataset. The data set contains seed information belonging to three different wheat varieties: Kama, Rosa and Canadian, represented by 1, 2 and 3 respectively
Link:https://www.kaggle.com/datasets/jmcaro/wheat-seedsuci

