# Cryptocurrency Clusters

## Background

* An investment bank is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. They’ve require a report that includes what cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system for this new investment. The data that is to be used will need to be preprocessed first and then fit to a machine learning model.

### Data Preparation

* Loaded `crypto_data.csv` into Pandas. The dataset was obtained from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).

* Discarded all cryptocurrencies that are not being traded and dropped the `IsTrading` column from the dataframe.

* Removed any rows that have null values.

* Filtered dataset for cryptocurrencies that have been mined.

* `CoinName` dropped from the original dataframe as it added no value and the data must be numerical.

* Converted `Algorithm` and `ProofType` into numerical data using pd.get_dummies.

* Standardized the dataset.

### Dimensionality Reduction

* Preserved 90% of the explained variance in dimensionality reduction. 

* Further reduced the dataset dimensions with t-SNE. Created a scatter plot of the t-SNE output.
* ![image](https://user-images.githubusercontent.com/85084734/154164782-6a803f6e-869c-4f6c-9a54-07c4c768c197.png)

### Cluster Analysis with k-Means

* Created an elbow plot to identify the best number of clusters.
* ![image](https://user-images.githubusercontent.com/85084734/154164712-88d4f132-d3aa-4e11-86dc-ecb6320aa5b7.png)
* ![image](https://user-images.githubusercontent.com/85084734/154164834-db9305ac-d4d5-4fab-8840-86028ea1c8f2.png)
