# CryptoClustering

## **Instructions**

1. Load the <code>crypto_market_data.csv</code> into a DataFrame.
2. Get the summary statistics and plot the data to see what the data looks like before proceeding.

## **Prepare the Data**
* Use the <code>StandardScaler()</code> module from <code>scikit-learn</code> to normalize the data from the CSV file.
* Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.
    * The first five rows of the scaled DataFrame should appear as follows:
  ![ScaledDataframe](images/scaled_DataFrame.png)

## **Find the Best Value for k Using the Original Scaled DataFrame**
Use the elbow method to find the best value for <code>k</code> using the following steps:
   * Create a list with the number of k values from 1 to 11.
   * Create an empty list to store the inertia values.
   * Create a <code>for</code> loop to compute the inertia with each possible value of <code>k</code>.
   * Create a dictionary with the data to plot the elbow curve.
   * Plot a line chart with all the inertia values computed with the different values of <code>k</code> to visually identify the optimal value for <code>k</code>.
   * Answer the following question in your notebook: What is the best value for <code>k</code>?

## **Cluster Cryptocurrencies with K-means Using the Original Scaled Data**
Use the following steps to cluster the cryptocurrencies for the best value for <code>k</code> on the original scaled data:
   * Initialize the K-means model with the best value for <code>k</code>.
   * Fit the K-means model using the original scaled DataFrame.
   * Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
   * Create a copy of the original data and add a new column with the predicted clusters.
   * Create a scatter plot using hvPlot as follows:
        * Set the x-axis as "PC1" and the y-axis as "PC2".
        * Color the graph points with the labels found using K-means.
        * Add the "coin_id" column in the <code>hover_cols</code> parameter to identify the cryptocurrency represented by each data point.
    
## **Optimize Clusters with Principal Component Analysis**
   * Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
   * Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:
        * What is the total explained variance of the three principal components?
   * Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.
        * The first five rows of the PCA DataFrame should appear as follows:

![PCA](images/PCA_DataFrame.png)

## **Find the Best Value for k Using the PCA Data**
Use the elbow method on the PCA data to find the best value for <code>k</code> using the following steps:
   * Create a list with the number of k-values from 1 to 11.
   * Create an empty list to store the inertia values.
   * Create a <code>for</code> loop to compute the inertia with each possible value of <code>k</code>.
   * Create a dictionary with the data to plot the Elbow curve.
   * Plot a line chart with all the inertia values computed with the different values of <code>k</code> to visually identify the optimal value for <code>k</code>.
   * Answer the following question in your notebook:
        * What is the best value for <code>k</code> when using the PCA data?
        * Does it differ from the best k value found using the original data?
    
## **Cluster Cryptocurrencies with K-means Using the PCA Data**
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:
   * Initialize the K-means model with the best value for <code>k</code>.
   * Fit the K-means model using the PCA data.
   * Predict the clusters to group the cryptocurrencies using the PCA data.
   * Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
   * Create a scatter plot using hvPlot as follows:
        * Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
        * Color the graph points with the labels found using K-means.
        * Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
   * Answer the following question:
        * What is the impact of using fewer features to cluster the data using K-Means?





