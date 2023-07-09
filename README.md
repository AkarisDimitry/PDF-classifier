**#README**
##Overview
This project provides a Python script for performing unsupervised clustering on text data from PDF and DOC files. The script reads and preprocesses the text data, converts it into a TF-IDF matrix, and then performs four different types of clustering: K-means, hierarchical, Latent Dirichlet Allocation (LDA), and DBSCAN. The results are printed and visualized.

##Algorithms
###K-means
The K-means algorithm partitions the dataset into K distinct, non-overlapping clusters where each data point belongs to the cluster with the closest mean. The algorithm starts by initializing K cluster centroids. Each data point is then assigned to the nearest centroid, and each centroid is updated to be the mean of the data points assigned to it. This process is repeated until the assignments no longer change or a maximum number of iterations is reached. K-means is efficient and scales well to large datasets, but the number of clusters K must be specified in advance, and the algorithm is sensitive to the initial choice of centroids.

###Hierarchical Clustering
Hierarchical clustering creates a tree of clusters. The algorithm starts by treating each data point as a single cluster, and then merges the two clusters that are most similar until only one cluster (or K clusters) remains. The result is a tree-based representation of the data (a dendrogram) that shows the order in which clusters were merged. Hierarchical clustering does not require the number of clusters K to be specified in advance, and it can capture complex cluster structures. However, it is more computationally intensive than K-means, especially for large datasets.

###Latent Dirichlet Allocation (LDA)
LDA is a type of probabilistic topic model that assumes each document is a mixture of a certain number of topics, and each word in the document is attributable to one of the document's topics. The algorithm uses a generative process and applies Bayes' theorem to infer the mixture of topics and topic assignments that most likely generated the observed documents. LDA can capture the semantic structure of the documents and uncover the hidden topics that pervade the documents. However, the number of topics must be specified in advance, and the algorithm assumes that the order of the words in the documents does not matter (bag-of-words assumption).

###DBSCAN
DBSCAN (Density-Based Spatial Clustering of Applications with Noise) is a density-based clustering algorithm. The algorithm starts by exploring the dataset from a random point, and if there are at least 'min_samples' points within a distance of 'eps' from that point, a new cluster is created. The algorithm then iteratively adds the nearby points within 'eps' distance to the cluster. If a point is not within 'eps' distance of any other points, it's considered as noise. Unlike K-means and hierarchical clustering, DBSCAN does not require the number of clusters to be specified in advance, and it can discover clusters of arbitrary shape. However, it is sensitive to the choice of 'eps' and 'min_samples' parameters, and it does not perform well when the density varies across the clusters.

**#Why This Code is Good for Classification**
This code provides a comprehensive suite of clustering methods, which allows it to handle a wide variety of text data and meet different needs. The preprocessing steps included in this code (stopword removal, tokenization, and TF-IDF transformation) help to reduce the noise and dimensionality of the text data, making it easier for the clustering algorithms to detect the underlying patterns. The use of TF-IDF ensures that the importance of each word is properly weighted, which improves the quality of the clusters. Furthermore, the code includes functions for visualizing the results, which can help in understanding the clustering output and assessing the quality of the clusters.




