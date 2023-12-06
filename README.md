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
