# CODTECH-TASK-1


NAME- DHANANJAYA B
COMPANY- CODTECH IT SOLUTIONS
INTERNSHIP ID- CTWDS2433
DOMAIN- DATA SCIENTIST
DURATION - 30TH NOV 2024 TO 15TH JAN 20215


OVERVIEW OF THE PROJECT 

OBJECTIVEVE : Explore unsupervised learning techniques by performing clustering
analysis on a dataset without predefined labels. Implement clustering
algorithms such as K-means, hierarchical clustering, or DBSCAN to
identify natural groupings or patterns within the data. Evaluate the
clustering results using metrics like silhouette score or Davies–Bouldin
index, and visualize.  


Unsupervised Learning: Clustering Analysis with Java
Overview
Unsupervised learning techniques aim to identify hidden patterns or intrinsic structures in datasets without predefined labels. Clustering is a common technique used to group similar data points together. The goal is to partition the dataset into clusters such that similar items are grouped together, and dissimilar items are placed in separate clusters.

In this code, we implement three popular clustering algorithms:

K-Means Clustering
Hierarchical Clustering
DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
We also evaluate the clustering results using the Silhouette Score and the Davies-Bouldin Index.

Clustering Algorithms Implemented
K-Means Clustering

Goal: Partition the dataset into k clusters based on the similarity of data points.
Method:
Randomly initialize k cluster centers (centroids).
Assign each data point to the nearest centroid.
Recompute centroids as the mean of assigned points.
Repeat until convergence (centroids no longer change significantly).
Pros: Simple, fast, and effective for spherical clusters.
Cons: Sensitive to initial centroids and requires specifying k.
Hierarchical Clustering

Goal: Build a hierarchy of clusters either by merging smaller clusters (agglomerative) or splitting larger clusters (divisive).
Method:
Agglomerative: Start with individual points as clusters and iteratively merge the closest clusters based on distance.
Divisive: Start with one large cluster and recursively split it.
Pros: Does not require k; produces a dendrogram (tree structure).
Cons: Computationally expensive for large datasets.
DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

Goal: Discover clusters of arbitrary shape and separate noise points.
Method:
Groups points that are close enough based on a distance threshold (ε) and a minimum number of points (minPts).
Points with fewer than minPts neighbors are labeled as noise.
Pros: Identifies noise and clusters of arbitrary shapes.
Cons: Performance can degrade with high-dimensional data and requires tuning ε and minPts.
Evaluation Metrics
Silhouette Score

Measures how similar a point is to its own cluster compared to other clusters.
Formula:
𝑠(𝑖)=𝑏(𝑖)−𝑎(𝑖)max(𝑎(𝑖),𝑏𝑖))s(i)= max(a(i),b(i))b(i)−a(i)
​
 Where:
𝑎(𝑖)a(i) = average distance to points in the same cluster.𝑏(𝑖)b(i) = average distance to points in the nearest cluster.Range: -1 to 1.
A higher score indicates better clustering.Davies-Bouldin Index (DBI)

Measures the ratio of the sum of within-cluster scatter to between-cluster separation. A lower DBI indicates better clustering.
Formula:
𝐷𝐵=1𝑘∑𝑖=1𝑘max
⁡𝑗≠𝑖(𝑠𝑖+𝑠𝑗𝑑𝑖𝑗)DB= k1​  i=1∑k  
j=imax​ ( d ij​ s i+s j​  )
Where:𝑠 𝑖s i = average distance between points in cluster 𝑖i.𝑑𝑖𝑗d ij = distance between the centroids of clusters 
𝑖i and 𝑗j.




Explanation of Code
Dataset Preparation:

The dataset is a set of 2D data points that are converted into DoublePoint objects (used for clustering).
K-Means Clustering:

The code initializes a KMeansPlusPlusClusterer with 3 clusters (k=3) and applies it to the dataset.
It then prints the points in each of the resulting clusters.
Silhouette Score Calculation:

The silhouette score for each data point is calculated by computing the mean distance to other points in the same cluster and the nearest cluster.
The overall silhouette score for the clustering is the average of all individual silhouette scores.
Conclusion
This code demonstrates K-Means clustering with silhouette score evaluation. You can similarly implement Hierarchical Clustering or DBSCAN by using appropriate libraries or algorithms. These techniques help identify natural patterns in data and evaluate the effectiveness of clustering using metrics like silhouette score and Davies-Bouldin index.






