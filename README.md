
## 📊 Objective

To classify cryptocurrencies by examining their percentage changes over:

- 24 hours
- 7 days
- 30 days
- 60 days
- 200 days
- 1 year

The goal is to:
- Normalize the data using `StandardScaler`.
- Apply **K-Means Clustering** on both the original scaled dataset and PCA-reduced dataset.
- Use the **Elbow Method** to find the optimal number of clusters.
- Visualize clustering results.
- Analyze PCA feature importance.

## 🧪 Technologies Used

- Python 3.x
- Pandas
- Scikit-learn (`StandardScaler`, `KMeans`, `PCA`)
- Matplotlib
- Jupyter Notebook

## 🧼 Data Preparation

1. Load `crypto_market_data.csv` into a DataFrame.
2. Set the `coin_id` as the index.
3. Normalize the price change percentage columns using `StandardScaler`.

## 🔍 Clustering with K-Means

### Step 1: Original Scaled Data
- Elbow method used to find optimal `k`.
- Applied K-Means with best `k`.
- Scatter plot generated with:
  - X-axis: `price_change_percentage_24h`
  - Y-axis: `price_change_percentage_7d`

### Step 2: PCA Optimization
- Applied PCA to reduce to 3 components.
- Explained variance of components extracted.
- Elbow method re-run on PCA-transformed data.
- Re-clustered using K-Means.
- Scatter plot generated with:
  - X-axis: `PC1`
  - Y-axis: `PC2`

## Feature Importance with PCA

A DataFrame was generated to display the weights of original features on each of the three principal components, helping to determine which time intervals had the strongest influence.

## Key Questions Answered

- What’s the optimal number of clusters (k)?
- How does PCA affect clustering?
- Which features most influence each principal component?
