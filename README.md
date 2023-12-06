# CryptoClustering

## **Instructions**

1. Load the <code>crypto_market_data.csv</code> into a DataFrame.
2. Get the summary statistics and plot the data to see what the data looks like before proceeding.

## **Prepare the Data**
* Use the <code>StandardScaler()</code> module from <code>scikit-learn</code> to normalize the data from the CSV file.
* Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.
    * The first five rows of the scaled DataFrame should appear as follows:
