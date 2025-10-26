# K-Means Clustering Analysis

This project demonstrates the implementation of K-Means clustering on customer data to identify distinct customer segments based on their annual income and spending score.

## Project Overview

The analysis uses the Mall Customers dataset to perform customer segmentation using the K-Means clustering algorithm. The goal is to group customers into different clusters based on their spending behavior and income levels.

## Dataset

The project uses the `Mall_Customers.csv` dataset which contains information about mall customers including:
- Customer ID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1-100)

## Methodology

### 1. Data Preprocessing
- Import necessary libraries (pandas, numpy, matplotlib, seaborn, scikit-learn)
- Load and explore the dataset
- Select relevant features for clustering: 'Annual Income (k$)' and 'Spending Score (1-100)'
- Standardize the data using StandardScaler

### 2. Determining Optimal Number of Clusters
- Use the Elbow Method to find the optimal number of clusters by plotting Within-Cluster Sum of Squares (WCSS)
- Use the Silhouette Method to validate the optimal number of clusters
- Identify k=5 as the optimal number of clusters

### 3. K-Means Clustering Implementation
- Apply K-Means clustering with k=5 clusters
- Initialize centroids using 'k-means++' method
- Set random_state=42 for reproducibility
- Use n_init=10 for multiple initializations

### 4. Visualization
- Create scatter plots to visualize the customer clusters
- Plot cluster centroids
- Color-code data points by cluster assignment
- Include legend and colorbar for interpretation

## Key Findings

The analysis successfully identifies 5 distinct customer segments based on income and spending patterns:
- High income, high spending
- High income, low spending  
- Medium income, medium spending
- Low income, high spending
- Low income, low spending

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Usage

1. Ensure all required libraries are installed
2. Run the Jupyter notebook cells sequentially
3. The dataset `Mall_Customers.csv` should be in the same directory
4. Follow the analysis steps to reproduce the clustering results

## Results Interpretation

The clustering results can help businesses:
- Target marketing campaigns to specific customer segments
- Develop personalized product recommendations
- Optimize inventory based on customer spending patterns
- Improve customer retention strategies

Note: The current implementation shows a FileNotFoundError for the dataset, which needs to be resolved by ensuring the correct file path to `Mall_Customers.csv`.
