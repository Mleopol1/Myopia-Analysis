# Myopia Analysis

This repository contains a Jupyter Notebook that analyzes data on myopia using various unsupervised machine learning techniques.

## Data

The data used in this analysis is stored in the "myopia.csv" file located in the "Resources" folder.

## Preparing the Data

The first step in the analysis is to prepare the data for machine learning. The myopia.csv file is loaded into a Pandas DataFrame, and the 'Myopic' column is removed, which serves as the target variable. The dataset is then standardized using the normalize function from scikit-learn.

## Applying Dimensionality Reduction

The next step is to apply dimensionality reduction techniques to the dataset. Principal Component Analysis (PCA) is used to preserve 90% of the explained variance in the dataset, resulting in three principal components. A t-distributed stochastic neighbor embedding (t-SNE) algorithm is then applied to the PCA features to visualize the data in two dimensions. A scatter plot of the t-SNE output is created using matplotlib.

## Performing a Cluster Analysis with K-Means

An elbow curve is then created to identify the best candidate for k, which will determine how many clusters should be used on the dataset.

![image](https://user-images.githubusercontent.com/111384049/228656347-24b6600e-62ea-4b66-ac01-b62383666b24.png)

Based on the elbow curve, 4 seems to be the best k before gradually dropping off. Therefore, patients can be clustered into 4 distinct groups. A K-Means algorithm is then used to perform a cluster analysis, and the 4 groups are visualized in the following plot.

![image](https://user-images.githubusercontent.com/111384049/228657542-81244edf-1e81-479b-bc8b-54c7530b0345.png)

## Conclusion

This analysis provides an example of how to use unsupervised machine learning techniques to analyze data on myopia. By applying dimensionality reduction techniques like PCA and t-SNE, we can better understand the patterns and relationships in the data.
