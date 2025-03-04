# Sound-Clustering

# Clustering Analysis and Dimensionality Reduction

## **Project Overview**
This project explores **clustering techniques** to identify patterns within a dataset. The primary goal was to apply different clustering algorithms, evaluate their effectiveness, and determine the best method for grouping data points.

Dimensionality reduction techniques, such as **Principal Component Analysis (PCA)** and **t-Distributed Stochastic Neighbor Embedding (t-SNE)**, were used to visualize the high-dimensional data effectively. Clustering algorithms, including **K-Means** and **DBSCAN**, were applied to identify meaningful clusters, and various evaluation metrics were used to assess their performance.

## **Tasks Performed**
### **1. Data Preprocessing**
- Loaded the dataset and checked for missing values or anomalies.
- Applied **feature scaling** to standardize the dataset before clustering.

### **2. Dimensionality Reduction**
- Applied **PCA (Principal Component Analysis)** to reduce the dataset dimensions while preserving variance.
- Applied **t-SNE (t-Distributed Stochastic Neighbor Embedding)** for better cluster visualization.
- Observed that **t-SNE outperformed PCA** in visual separability, as it captured local structures more effectively.

### **3. Clustering Algorithms**
#### **K-Means Clustering**
- Used the **Elbow Method** to determine the optimal number of clusters (`K=2`).
- Applied **K-Means** clustering with the chosen `K` value.
- Evaluated cluster quality using:
  - **Silhouette Score:** 0.2269 (low but indicates some structure)
  - **Davies-Bouldin Index:** 1.6356 (moderate cluster separation)
  - **Inertia:** 29,322,746 (sum of squared distances to cluster centroids)

#### **DBSCAN Clustering**
- Applied **DBSCAN (Density-Based Spatial Clustering)** with different `eps` and `min_samples` values.
- Despite tuning, **DBSCAN failed to form meaningful clusters**, likely due to a lack of density variations in the dataset.
- Most points were either labeled as noise or assigned to a single cluster.

### **4. Clustering Evaluation & Comparison**
- **K-Means performed better** in this scenario, as it formed moderately distinct clusters.
- **DBSCAN struggled**, indicating that the dataset might not have the density-based structure it relies on.
- **Dimensionality reduction** improved visualization but did not significantly impact DBSCAN’s clustering quality.

### **5. Key Observations**
- **PCA vs. t-SNE:** t-SNE provided better cluster separability than PCA in visualization.
- **K-Means vs. DBSCAN:** K-Means worked well with structured clusters, whereas DBSCAN was ineffective due to data distribution.
- **Real-World Relevance:** In practical applications like speech or text clustering, choosing the right algorithm based on dataset characteristics is crucial.

## **Conclusion**
This project demonstrated the importance of **dimensionality reduction** in clustering, the effectiveness of **K-Means for structured data**, and the challenges of using **DBSCAN when density variations are absent**. The results highlight the need for **data-driven algorithm selection** to achieve meaningful clustering outcomes.

## **Future Work**
- Experiment with different distance metrics in K-Means.
- Apply **Hierarchical Clustering** to explore alternative approaches.
- Improve DBSCAN performance by adjusting feature scaling or selecting alternative similarity measures.

