# Clsutering Project 1 

## Overview 
The data is hard to interpreet by human eye since it is just numbers with slightly high dimensionality. 
We need to cluster this data with the best clustering method using k means algorithhm 
data shape (98000, 30)

---

## Key Steps

### 1. infering meaning from our data
describe() method expalins the data and i see that our data points are close with a std of raning between 1 -4 but this does not mean that  the actual feature values do not differ significantly in magnitude. Since i am planning to apply umap, i need to scale my data, since UMAP (and many clustering algorithms) rely on distance metrics, scaling can help maintain the integrity of the clustering process by ensuring that the distances reflect the true relationships between data points.

Clustering alogrithms may be snesitive to differnet scales in the data and we plan to feeed our data to k means alogirthm  scaling beforehand can help maintain consistency across your workflow.


---

### 2. Umap implemenatiton 
#### Key Benefits of Using UMAP in Clustering

Dimensionality Reduction: UMAP reduces the number of features in your dataset while preserving the relationships between data points, allowing for more effective clustering.
Noise Filtering: By focusing on the most relevant features, UMAP helps filter out noise and irrelevant data, enhancing the performance of clustering algorithms like K-Means.
Improved Clustering Performance: Reducing dimensionality mitigates the "curse of dimensionality," leading to more meaningful clusters as the data becomes denser in lower dimensions.
Enhanced Visualization: UMAP enables visualization of high-dimensional data in 2D or 3D, making it easier to interpret clustering results and understand data structure.
Better Interpretability: Clusters formed in a lower-dimensional space are easier to analyze and interpret, ensuring that the results are more meaningful and actionable.
I implenmented umap iwth 2 components, since further i plan to plot the clustered data in the 2D space. The data has to be represented in 2D space for this. 

Here is the dataframe format of what we obtained with umap:
![UMAP]{screenshots/umap.png}


---

### 3.Elbow method and silhouette score 
Elbow method tells me to choose 4 as the number of clusters for the k means algorithm
![UMAP]{screenshots/elbow.png}

---

### 4. Results
In the images we can see that our data is separated first in 2D space (umap n_components=2) and the second image in 3 D space (umap n_components=3)
2D:
![UMAP]{screenshots/2D.png}
3D:
![UMAP]{screenshots/3D.png}

---

## Conclusion



