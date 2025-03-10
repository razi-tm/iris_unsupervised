# README: Iris Dataset Unsupervised Classification using KMeans

## Description
This project performs unsupervised classification on the Iris dataset using the KMeans clustering algorithm. The optimal number of clusters is determined using the elbow method, and the initialization problem is addressed by running multiple initializations and selecting the best clustering outcome.

## Features
- **Determining the optimal number of clusters** using the elbow method.
- **Handling the initialization problem** by running KMeans multiple times and selecting the best clustering result.
- **Accuracy evaluation** by comparing clustering labels with actual species labels.

## Dependencies
Ensure you have the required dependencies installed using:
```bash
pip install numpy scikit-learn matplotlib
```

## Implementation Details
1. **Elbow Method for Finding Optimal Clusters**:
   - Runs KMeans for different values of `k` (from 1 to 10).
   - Plots distortions (inertia) to identify the optimal number of clusters.

2. **Handling Initialization Problem**:
   - Runs KMeans multiple times for each `k`.
   - Selects the clustering result with the best accuracy compared to ground truth labels.

3. **Final Classification & Accuracy Calculation**:
   - Runs KMeans 30 times with `k=3` (optimal for Iris dataset).
   - Chooses the best clustering result.
   - Computes accuracy based on alignment with actual labels.

## Notes
- Since KMeans is an unsupervised method, labels may not directly match the actual species labels. Accuracy is based on the best label alignment.
- The clustering accuracy is approximate and may vary slightly across runs due to the random initialization of KMeans.
