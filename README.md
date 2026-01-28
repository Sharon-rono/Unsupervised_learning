##K-Means Clustering on Iris Dataset  
A comprehensive implementation of K-Means clustering algorithm applied to the classic Iris dataset, demonstrating unsupervised learning techniques for pattern discovery and data segmentation.  

📋 Project Overview 

This project explores unsupervised machine learning through K-Means clustering on the Iris dataset. The analysis includes data preprocessing, feature scaling, cluster visualization, and optimal cluster selection using the elbow method.

🎯 Objectives  

Implement K-Means clustering on the Iris dataset
Demonstrate the importance of feature scaling in distance-based algorithms
Visualize natural groupings in the data
Determine optimal number of clusters using the elbow method
Analyze cluster characteristics and patterns

📊 Dataset  
The Iris dataset contains 150 samples of iris flowers with the following features:

SepalLengthCm: Sepal length in centimeters
SepalWidthCm: Sepal width in centimeters
PetalLengthCm: Petal length in centimeters
PetalWidthCm: Petal width in centimeters
Species: Target variable (not used in clustering)

🔧 Technologies Used  

Python 3.x
pandas: Data manipulation and analysis  
matplotlib: Data visualization  
scikit-learn: Machine learning algorithms  
StandardScaler: Feature scaling  
KMeans: Clustering algorithm  

🚀 Getting Started  
Ensure you have Iris.csv in your working directory
Open the Jupyter notebook:

bashjupyter notebook Unsupervised_Learning_Iris_KMeans.ipynb

Run all cells sequentially

📈 Analysis Pipeline  
1. Data Exploration

Load and inspect the Iris dataset
Examine data shape and statistical summary
Visualize feature relationships through scatter plots

2. Feature Engineering

Remove non-feature columns (Species, Id)
Analyze feature pair separability
Identify that Petal Length vs Petal Width shows the most distinct natural groupings

3. Feature Scaling

Apply StandardScaler to normalize features
Ensure all features contribute equally to distance calculations
Critical step for K-Means as it relies on Euclidean distance

4. K-Means Clustering

Train K-Means model with 3 clusters (k=3)
Assign cluster labels to data points
Identify cluster centroids

5. Visualization

Plot clusters with distinct colors
Mark centroids with 'X' markers
Transform scaled centroids back to original scale for interpretation

6. Optimal Cluster Selection

Implement elbow method
Calculate Within-Cluster Sum of Squares (WCSS) for k=1 to k=10
Identify optimal k value where WCSS reduction diminishes

🔍 Key Findings
Feature Analysis

Petal measurements (length and width) provide clearer cluster separation compared to sepal measurements.  
Natural groupings are most visible in petal feature space

Clustering Results

The algorithm successfully identifies 3 distinct clusters
Clusters show clear separation, especially using petal features
Patterns are primarily defined by petal size characteristics

Elbow Method

The elbow occurs at k=3, confirming the choice of 3 clusters
This balances between maximizing cluster granularity and minimizing model complexity
Aligns with the known number of species in the Iris dataset

💡 Why Feature Scaling Matters
Feature scaling is crucial for K-Means because:

The algorithm relies on distance calculations (Euclidean distance)
Features with larger scales can dominate the clustering process
Without scaling, features measured in larger units would have disproportionate influence
StandardScaler ensures all features contribute equally to cluster formation

📊 Visualization Highlights
The notebook includes:

Scatter plots comparing sepal and petal measurements
Color-coded cluster assignments
Centroid markers showing cluster centers
Elbow curve for WCSS analysis

🎓 Learning Outcomes
This project demonstrates:

Unsupervised learning discovers patterns without labeled data
Data preprocessing is critical for algorithm performance
Feature selection impacts cluster quality
Visualization aids in understanding cluster structure
Validation methods help determine optimal hyperparameter
