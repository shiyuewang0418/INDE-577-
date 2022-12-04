# K-Means Clustering
<img width="715" alt="image" src="https://user-images.githubusercontent.com/119746917/205459851-ce10ec06-ed5e-4e95-8dfb-6f8d0cb7357e.png">

## Algorithm 
Step-1: Select the value of K, to decide the number of clusters to be formed.

Step-2: Select random K points which will act as centroids.

Step-3: Assign each data point, based on their distance from the randomly selected points (Centroid), to the nearest/closest centroid which will form the predefined clusters.

Step-4: place a new centroid of each cluster.

Step-5: Repeat step no.3, which reassign each datapoint to the new closest centroid of each cluster.

Step-6: If any reassignment occurs, then go to step-4 else go to Step 7.

Step-7: FINISH

## Advantages
* Relatively simple to implement.
* Scales to large data sets.
* Guarantees convergence.
* Can warm-start the positions of centroids.
* Easily adapts to new examples.
* Generalizes to clusters of different shapes and sizes, such as elliptical clusters.

## Disadvantages
* Choosing k manually
* Being dependent on initial values.
* Clustering data of varying sizes and density.
* Clustering outliers:
Centroids can be dragged by outliers, or outliers might get their own cluster instead of being ignored. 
Consider removing or clipping outliers before clustering.
* Scaling with number of dimensions.


