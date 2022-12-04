# K-Nearest-Neighbors
## Definition
The 𝑘-nearest neighbors algorithm, or KNN for short, is a nonparametric algorithm that assumes that similar data exist 
in close proximity. In other words, similar things are near to each other.

KNN captures the idea of similarity (sometimes called distance, proximity, or closeness) with some mathematics we might 
have learned in our childhood— calculating the distance between points on a graph.

KNN is a non-parametric supervised model, and its main idea is to classify or regress by compute the k closest training 
examples in the data set.
## Algorithm 
k is a pre-defined constant, and for
* classification tasks.
An unlabeled data point is classified by assigning the label which is most frequent among the k training samples 
nearest to that query point.

* regression tasks.
An unlabeled data point is predicted by averaging the values among the k training samples nearest to that query point.
For our distance measure, we will choose the Euclidean distance defined by the following equation:
 $$ d(p, q) = \sqrt{(p - q)^{T} (p - q)} $$
## Advantages
* No training period. As discussed before, knn does not have a training period. This kind of learning model is called 
  lazy learner (Instance based learning), which uses sample data set directly to make real-time predictions based on some 
  algorithms. Thus knn is faster than some other algorithms which require training period (who are called eager learners).
* Supper simple. Knn is a very simple model which requires less computational resource, and it's eazy to implement. Also 
  only two hyper-parameters, number of neighbors k and distance function are required to be determined befor implying the algorithm.
* No assumptions needed. Knn requires no assumption on data distribution or other properties.
## Disadvantages
* Poor with large dataset. Computationally expensive when calculation the distances among all samples if the number of data is huge.
* Poor with high dimensions. When number of dimension is high, it's hard for knn to represent the relative space relationship 
  between data points, as data points become supper sparse. Also scales of different dimensions can largely affect the distances 
  between points, so feature scaling must be down before using knn. Moreover, it's also computationally expensive to calculate the 
  distances.
* Outlier, noise and missing value sensitivity. KNN is sensitive to noise and outliers in the dataset, and it cannot deal with 
  missing values.

# Scikit Learn
<img width="1035" alt="image" src="https://user-images.githubusercontent.com/119746917/205502953-c175f5aa-1f0f-428a-910e-3b861dc93938.png">

## Definition
It is an open source machine learning library that supports supervised and unsupervised learning. It also provides various tools 
for model fitting, data preprocessing, model selection, model evaluation, and many other utilities.
## Why Use Scikit-Learn For Machine Learning?
Whether you are just looking for an introduction to ML, want to get up and running fast, or are looking for the latest ML 
research tool, you will find that scikit-learn is both well-documented and easy to learn/use. As a high-level library, 
it lets you define a predictive data model in just a few lines of code, and then use that model to fit your data. It’s 
versatile and integrates well with other Python libraries, such as matplotlib for plotting, numpy for array vectorization, 
and pandas for dataframes.
