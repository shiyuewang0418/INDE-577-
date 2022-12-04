# The Single Neuron Logistic Regression Model
<img width="840" alt="image" src="https://user-images.githubusercontent.com/119746917/205464608-93605531-d7da-40ea-892d-e50c93c57cb9.png">


## Definition
In some machine learning classification problems, it is difficult to make some direct and clear classfication 
because of overlapping. In this case, we consider the probabilistic binary classfication problem. 
Instead of creating a single neuron model for predicting a class deterministic label, we will next build 
a single neuron model that predicts a class probability.

## Algorithm 
There are two primary types of logistic regression:
* Binary (e.g. determine whether a tumor is malignant or benign, or if a person will default on a bank loan)
* Multi-linear functions that predict class labels (e.g. is the information describing a cat, dog, or a sheep)

Model:
<img width="247" alt="image" src="https://user-images.githubusercontent.com/119746917/205508573-f9081ea0-6be2-493e-8271-8270686d19aa.png">


Cost Function:
<img width="816" alt="image" src="https://user-images.githubusercontent.com/119746917/205508588-0a1a75eb-fe49-418a-8aa2-f45f391e18f1.png">



## Advantages
* Easier to implement, interpret, and very efficient to train.
* Running fast
* No assumptions about distributions of classes in feature space.
* Can use coefficients to interpret feature importance
* Can deal with missing data and no need of normalization.
* Easy to interprete feature importance
## Disadvantages
* Assume linear relations
* Cannot deal with the situation that number of features is larger than number of samples
