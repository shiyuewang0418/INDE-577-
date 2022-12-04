# Principal Component Analysis (PCA)
<img width="756" alt="image" src="https://user-images.githubusercontent.com/119746917/205460571-3fbf8b66-a2bd-42c1-8100-172b5793addd.png">

## Definition
Principal Component Analysis (PCA) is used in exploratory data analysis and for multidimensionality reduction. 
The main idea is to project data points onto only the first few principal components to obtain lower-dimensional 
data while preserving as much of the data’s variation as possible. In other words, using PCA we remove the 
redundant and highly-correlated data and we keep only the most significant data features for further analysis.

## Algorithm
PCA is defined as an orthogonal transformation that transforms the data to a new coordinate system such that the greatest variance by some scalar projection of the data comes to lie on the first coordinate (called the first principal component), the second greatest variance on the second coordinate, and so on.

Consider an $n \times p$ data matrix $X$, with column-wise zero , where each of the rows represents a different repetition of the experiment, and each of the columns gives a particular kind of feature .

The $k$-th component can be found by subtracting the first $k$ principal components from $X$:

$$\mathbf{\hat{X}}_k = \mathbf{X} - \sum_{s = 1}^{k - 1} \mathbf{X} \mathbf{w}_{(s)} \mathbf{w}_{(s)}^{\mathsf{T}}$$
and then finding the weight vector which extracts the maximum variance from this new data matrix $$\mathbf{w}_{(k)} = \mathop{\operatorname{arg\,max}}_{\left\| \mathbf{w} \right\| = 1} \left\{ \left\| \mathbf{\hat{X}}_{k} \mathbf{w} \right\|^2 \right\} = \arg\max \left\{ \tfrac{\mathbf{w}^\mathsf{T} \mathbf{\hat{X}}_{k}^\mathsf{T} \mathbf{\hat{X}}_{k} \mathbf{w}}{\mathbf{w}^T \mathbf{w}} \right\}$$

And the full principal components decomposition of $X$ is given by $$ \mathbf{T} = \mathbf{X}\mathbf{W} $$

## Advantages 
PCA can help us improve performance at a very low cost of model accuracy. Other benefits of PCA include reduction 
of noise in the data, feature selection (to a certain extent), and the ability to produce independent, uncorrelated 
features of the data.

## Disadvantages
Although this is great, PCA does have some issues. The most major one is that the results are directly dependent 
on the scale of the variables. If one variable seems to have more variation because it is on a larger scale than 
the others, this variable will be dominant in the principal components and will produce less than ideal results. 
On a similar note, the effectiveness of PCA is greatly influenced by the appearance of skew in the data with thick tails. 
Lastly, PCA can be quite challenging to interpret, especially since this method mixes variables together to maximize variability.
