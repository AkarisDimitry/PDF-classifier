# Text Document Clustering

This project provides a Python script for performing unsupervised clustering on text data from PDF and DOC files. The script reads and preprocesses the text data, converts it into a TF-IDF matrix, and then performs four different types of clustering: K-means, hierarchical, Latent Dirichlet Allocation (LDA), and DBSCAN.

## Clustering Algorithms

### K-means

The K-means algorithm partitions the dataset into K distinct, non-overlapping clusters where each data point belongs to the cluster with the closest mean. The algorithm starts by initializing K cluster centroids. Each data point is then assigned to the nearest centroid, and each centroid is updated to be the mean of the data points assigned to it. This process is repeated until the assignments no longer change or a maximum number of iterations is reached.

### Hierarchical Clustering

Hierarchical clustering creates a tree of clusters. The algorithm starts by treating each data point as a single cluster, and then merges the two clusters that are most similar until only one cluster (or K clusters) remains. The result is a tree-based representation of the data (a dendrogram) that shows the order in which clusters were merged.

### Latent Dirichlet Allocation (LDA)

LDA is a type of probabilistic topic model that assumes each document is a mixture of a certain number of topics, and each word in the document is attributable to one of the document's topics. The algorithm uses a generative process and applies Bayes' theorem to infer the mixture of topics and topic assignments that most likely generated the observed documents.

### DBSCAN

DBSCAN (Density-Based Spatial Clustering of Applications with Noise) is a density-based clustering algorithm. The algorithm starts by exploring the dataset from a random point, and if there are at least 'min_samples' points within a distance of 'eps' from that point, a new cluster is created. The algorithm then iteratively adds the nearby points within 'eps' distance to the cluster. If a point is not within 'eps' distance of any other points, it's considered as noise.

## Code Usage

First, ensure that all necessary Python libraries are installed. This includes os, collections, matplotlib, PyPDF2, docx, numpy, nltk, sklearn, gensim, scipy, and wordcloud. Most of these libraries can be installed via pip.

The main script is located in `main.py`. To run the script, navigate to the directory containing `main.py` and type `python main.py` into the terminal.

The script reads all PDF and DOC files in the directory and its subdirectories specified in the `get_text_from_files` function. It then preprocesses the text data, converts it into a TF-IDF matrix, and performs K-means, hierarchical, LDA, and DBSCAN clustering. The clustering results are printed and visualized. 

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.



