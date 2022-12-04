# Perceptron
<img width="622" alt="image" src="https://user-images.githubusercontent.com/119746917/205461265-fdf4a6f5-5a61-4441-b77a-624767a7f46d.png">

## Definition
In machine learning, the Perceptron algorithm is a two-class (binary) classification algorithm. 
Binary classification is a form of classification, the process of predicting categorical variables, 
where the output is restricted to two classes, and it can be used in many data science field. 
It is a type of neural network model, perhaps the simplest type of neural network model. 
It consists of a single node or neuron that takes a row of data as input and predicts a class label

## Algorithm 
First a function that maps input $\mathbf {x}$ (a real-valued vector) to an output value $f(\mathbf {x} )$ (a single binary value) is given by


$$ f(\mathbf{x}) = \begin{cases}1 & \text{if }\ \mathbf{w} \cdot \mathbf{x} + b > 0,\\0 & \text{otherwise}\end{cases} $$


where $\mathbf {w}$ is a vector of real-valued weights, $\mathbf {w} \cdot \mathbf {x} = \sum_{i=1}^{m} {w_{i}x_{i}}$ is the dot product, $m$ is the number of inputs to the perceptron.


Initialize random small weights.
For each sample $\mathbf{x}_j$ and $y_j$ , perform the following steps:
Calculate the actual output:


$$ y_j(t) = f[\mathbf{x}_j^T\cdot\mathbf{w}(t)] $$


Update the weights:


$$ \mathbf{w}(t+1) = \mathbf{w}(t) \boldsymbol{+} \cdot \mathbf{x}_j^T(\mathbf{d} - \mathbf{y}(t)) $$


Updates the weights after steps 2, until meets stopping criterias.
