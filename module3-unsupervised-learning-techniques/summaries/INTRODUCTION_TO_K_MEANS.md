# Introduction to K-means

K-means is an unsupervised partitioning algorithm used to organize unlabeled data into groups or clusters. The algorithm creates a logical scheme to make sense of the data by defining each cluster with a central point, or centroid, representing the center of that cluster. The name **K-means** comes from the fact that the centroid is the mathematical mean of the data points in the cluster. There are four main steps to building a K-means model:

### **Step 1: Choose the Number of Centroids (K)**
The first step involves selecting the number of clusters, represented by **K**. You need to decide how many centroids (clusters) should be used. This could be based on prior knowledge or experimentation. For instance, if you're analyzing customer types for a product with five variations, you might choose K=5. However, if you don't know the number of clusters in advance, you can try different K values and determine which yields the best results.

### **Step 2: Assign Data Points to Nearest Centroid**
Once the centroids are chosen, each data point is assigned to the nearest centroid. The nearest centroid is simply the one closest in space to each data point. For example, if two data points are closer to the blue centroid, they will be assigned to the blue cluster.

### **Step 3: Recalculate the Centroids**
After assigning data points to clusters, the centroids are recalculated. The new centroid of each cluster is determined by taking the mean of all data points within that cluster. The centroids shift to the new center of their respective clusters.

### **Step 4: Repeat Steps 2 and 3 Until Convergence**
Steps 2 and 3 are repeated iteratively. Each iteration assigns data points to their nearest centroids, and the centroids are recalculated based on the new assignments. This process continues until the algorithm reaches convergence, meaning the centroids stop changing or move only minimally.

### **Example of K-means Clustering**
If the data is simple and few in number, like the example with just four data points, the model may converge quickly. With larger datasets, the centroids would move closer to their respective clusters over time. However, it's essential to run the model with different initial positions for the centroids to avoid poor clustering due to local minima. This happens when the algorithm converges to a suboptimal solution because the starting centroids are not well-positioned.

For instance, if the initial centroids are poorly placed, the resulting clusters may not make sense, as seen in the example where the data points were not grouped intuitively. Running the algorithm multiple times with different initializations helps to avoid such issues.

### **Partitioning vs. Clustering**
Though K-means is a partitioning algorithm, it is often discussed as a clustering algorithm. The distinction is important: in clustering algorithms, data points can exist outside any clusters (outliers), but K-means assigns every data point to a cluster, meaning there are no outliers. This is a key feature of partitioning algorithms.

### **Summary**
- **K-means** is an unsupervised learning technique that groups unlabeled data into **K** clusters based on similarity.
- The clustering process involves four steps: selecting centroids, assigning points, recalculating centroids, and repeating until convergence.
- The value for **K** is a decision that the modeler makes, and multiple models should be built to avoid poor clustering.
- K-means is a **partitioning algorithm** that assigns all data points to a cluster, unlike other clustering methods that may allow outliers.

In the next section, you will learn how to determine the best value for **K** and explore the limitations of K-means models.
