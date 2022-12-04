# Decision Tree
<img width="737" alt="image" src="https://user-images.githubusercontent.com/119746917/205470238-352f2832-c4c4-4cac-ba33-239f0485af47.png">

## Definition
The decision tree algorithm works based on the decision on the conditions of the features. 
Nodes are the conditions or tests on an attribute, branch represents the outcome of the tests, 
and leaf nodes are the decisions based on the conditions.


n decision analysis, a decision tree and the closely related influence diagram are used as a visual and 
analytical decision support tool, where the expected values (or expected utility) of competing alternatives are calculated.

## Algorithm 

* Get list of rows (dataset) which are taken into consideration for making decision tree (recursively at each nodes).
* Calculate uncertanity of our dataset or Gini impurity or how much our data is mixed up etc.
* Generate list of all question which needs to be asked at that node.
* Partition rows into True rows and False rows based on each question asked.
* Calculate information gain based on gini impurity and partition of data from previous step.
* Update highest information gain based on each question asked.
* Update best question based on information gain (higher information gain).
* Divide the node on best question. Repeat again from step 1 again until we get pure node (leaf nodes).

## Advantages
* Easy to use and understand.
* Can handle both categorical and numerical data.
* Resistant to outliers, hence require little data preprocessing.

## Disadvantages
* Prone to overfitting.
* Require some kind of measurement as to how well they are doing.
* Need to be careful with parameter tuning.
* Can create biased learned trees if some classes dominate.
