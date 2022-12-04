# Multilayer Neural Network
## Definition
A multilayer neural network (or multilayer perceptron ,MLP) is a class of feedforward artificial neural network (ANN). 
It's an extension of perceptrons, with more layers and non-linear activation functions.
## Algorithm 
First, a multilayer neural network has a non-linear activation function in most cases, and sigmoid ( $\sigma(\cdot)$ ), hyperbolic tangent ( $tanh(\cdot)$ ) and rectified linear ( $RELU(\cdot)$ ) activation functions are widely used. 

$$ \sigma(x) = \frac{1}{1 + e^{-x}} $$

$$ tanh(x) = \frac{e^x-e^{-x}}{e^x+e^{-x}} $$$$ RELU(x) = \begin{cases} x & \text{if}\ x > 0,\\0 & \text{otherwise}\end{cases} $$


Further, a MLP consists of many layers (an input and an output layer with one or more hidden layers) of non-linear activating nodes. Since MLPs are fully connected, each node in one layer connects with a certain weight to every node in the following layer.

Learning occurs in MLP by changing connection weights after each piece of data is processed, based on the amount of error in the output compared to the expected result. This is a supervised learning, and is carried out through backpropagation, a generalization of the least mean squares algorithm in the linear perceptron.

The basic idea of backpropagation is to take advantage of the Chain Rule to derive derivative of each layers, from end to start.

Error in an output node $j$ in the $n$ th training example by $e_j(n)=d_j(n)-y_j(n)$, where $d$ is the target value and $y$ is the value produced by the perceptron. The node weights can be adjusted by minimizing the sum square error in the entire output, given by

$$\mathcal{E}(n)=\frac{1}{2}\sum_j e_j^2(n)$$
Using gradient descent, the change in each weight of output layer is

$$\Delta w_{ji} (n) = -\gamma\frac{\partial\mathcal{E}(n)}{\partial v_j(n)} y_i(n)$$
where $y_i$ is the output of the previous neuron, $\gamma$ is the learning rate, $v_j$ is the output of output layer.

It is easy to prove that for an output node this derivative can be simplified to

$$-\frac{\partial\mathcal{E}(n)}{\partial v_j(n)} = e_j(n)\phi^\prime (v_j(n))$$
where $\phi^\prime$ is the derivative of the activation function described above, which itself does not vary. For hidden nodes, it can be shown that the relevant derivative is

$$-\frac{\partial\mathcal{E}(n)}{\partial v_j(n)} = \phi^\prime (v_j(n))\sum_k -\frac{\partial\mathcal{E}(n)}{\partial v_k(n)} w_{kj}(n)$$

## Advantages

* Learn non-linear and complex relationships.
* Fit all continous function, if the hidden layer is more than 2.
* Can work on both classification and regression
* Disadvantage of Perceptron
## Disadvantages
* Too many parameters to turn
* Large model complexity if number of layers and neurons are large
* Slow training process if model is large
* Easy to overfit.
