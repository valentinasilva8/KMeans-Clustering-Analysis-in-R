# KMeans-Clustering-Analysis-in-R

This repository contains the code, visualizations, and findings for a clustering lab assignment using the **KMeans** algorithm in **R**. The project walks through methods for determining the optimal number of clusters and visualizing model results across different `k` values.

## 📊 Dataset Overview

The dataset includes the following six features related to product spending:

- `Fresh`
- `Milk`
- `Grocery`
- `Frozen`
- `Detergents_Paper`
- `Delicatessen`

These continuous variables represent annual spending in monetary units across product categories for wholesale customers.

## 🎯 Objective

The goal of this lab is to:
- Apply unsupervised learning through KMeans clustering.
- Identify the most appropriate number of clusters using three distinct evaluation techniques.
- Build models using different `k` values.
- Visualize and compare clustering results for interpretability and insights.

## 🔍 Methodology: Determining the Optimal `k`

Three techniques were used to estimate the best number of clusters:

### 1. Elbow Method
Plots the total within-cluster sum of squares (WSS) against the number of clusters. The “elbow” point suggests an optimal `k`.

### 2. Average Silhouette Method
Measures how similar an object is to its own cluster compared to other clusters. A higher silhouette score indicates better-defined clusters.

### 3. Gap Statistic
Compares the total intra-cluster variation for different `k` values with that expected under a null reference distribution. The optimal `k` is the one that maximizes the gap statistic.

Each method may suggest a different value for `k`, which is explored comparatively.

## ⚙️ Modeling Process

1. Preprocessed and scaled the dataset.
2. Applied the `kmeans()` function in R using the different `k` values identified.
3. Stored clustering results and centroids for each model.

The models were implemented using:
- `cluster`
- `factoextra`
- `fpc`
- `dbscan`
- `dendextend`

## 📈 Visualizations

Generated visualizations using `fviz_cluster()` for each clustering model:

- **Elbow Plot** – Used to visually identify the "elbow" point.
- **Silhouette Plot** – Showed average silhouette width per cluster.
- **Gap Statistic Plot** – Showed gap statistic values across `k`.
- **Cluster Comparison Plot** – Combined output using `fviz_cluster()` to visually compare models side-by-side.


## ✅ Final Comparison & Interpretation

After evaluating each method:
- **Elbow Method** suggested `k = 5`
- **Silhouette Method** suggested `k = 2`
- **Gap Statistic** suggested `k = 10`


Clusters were compared based on compactness and separation. The final recommendation for `k` was based on balancing interpretability and statistical evaluation.

## 🎓 Learnings and Reflections

- Different methods can yield different optimal `k`, reinforcing the importance of triangulating model selection.
- Visual interpretation via `fviz_cluster()` added clarity to otherwise abstract metrics.
- Real-world clustering requires not just technical accuracy but also domain context to validate clusters.


## 🛠️ Tech Stack

- **Language**: R
- **Packages**:
  - `cluster`
  - `factoextra`
  - `fpc`
  - `dbscan`
  - `dendextend`



