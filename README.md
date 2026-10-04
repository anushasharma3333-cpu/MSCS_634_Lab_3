# MSCS_634_Lab_3

**Purpose**

The purpose of the current lab is the exploration and comparison of K-Means and K-Medoids clustering algorithms on the Wine Dataset from the sklearn library. The dataset was standardized prior to the clustering process; K-Means and K-Medoids with three clusters were implemented. The performance of clustering was estimated by Silhouette Score and Adjusted Rand Index (ARI) metrics. Moreover, PCA was used to reduce the dimensionality of the dataset to 2D for its visualization and comparison.

**Dataset**

The Wine Dataset includes 178 samples with 13 numerical attributes describing different characteristics of the wine. There are three classes of wines in the dataset. Prior to the clustering process, the features of the dataset were standardized by the StandardScaler.

**Clustering Methods**
The following clustering algorithms have been implemented:
- K-Means with k=3
- K-Medoids with k=3

In K-Means algorithm, clusters are represented by the calculated centroids; in K-Medoids, the cluster centers consist of actual data points.

**Results**
K-Means:
- Silhouette Score: 0.2849
- Adjusted Rand Index (ARI): 0.8975

K-Medoids:
- Silhouette Score: 0.2676
- Adjusted Rand Index (ARI): 0.7411

As seen above, K-Means performed better in terms of both Silhouette Score and Adjusted Rand Index.

**Key Insights**

Both K-Means and K-Medoids algorithm were successful in identifying the cluster structure within the Wine dataset. Nonetheless, K-Means performed better according to the Silhouette Score and ARI criteria.

PCA plot illustrated the distribution and separation of the three clusters. There was some overlap, but the performance of K-Means was much better in terms of clustering.

**Challenges and Decisions**

The problem of using the K-Medoids clustering algorithm was one of the issues encountered in this lab because the algorithm is not provided by the sklearn clustering library. The solution was to use the scikit-learn-extra library that has an implementation of the K-Medoids algorithm. One of the key steps in this experiment was to perform standardization of the Wine Dataset before using clustering algorithms on the dataset. The Wine dataset has 13 features measured on different numerical scales, which could lead to the fact that the feature with bigger values can have more impact on the distance calculation. For this reason, StandardScaler was used to normalize the features using the z-score method and put them on the same scale. The next challenge was the visualization of the dataset having 13 dimensions. It was not possible to represent all the features on a 2D scatterplot; therefore, Principal Component Analysis (PCA) was used to reduce the standardized dataset from 13 dimensions to two principal components.

**Conclusion**

 In this lab, we saw that K-Means and K-Medoids can be used as unsupervised learning methods to discover clusters in the Wine Dataset. The two methods were run with three clusters and evaluated using the Silhouette Score and the Adjusted Rand Index (ARI). The Silhouette Score and the ARI for K-Means were 0.2849 and 0.8975, respectively, while the same indices for K-Medoids were 0.2676 and 0.7411, respectively. From these scores, we can see that K-Means performs better in terms of both the Silhouette Score and the ARI compared to K-Medoids in the standardized Wine Dataset. Moreover, the PCA plot allowed us to visualize the clusters and their positions. In general, this lab showed the importance of data standardization, correct evaluation metrics, and visualization when comparing different methods for clustering.
