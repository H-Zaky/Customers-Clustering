# Customer Segmentation Using KMeans Clustering on Online Retail Data

This project demonstrates customer segmentation using KMeans clustering on an online retail dataset. The dataset contains transactional data for the years 2009-2011. The goal is to cluster customers based on their purchasing behavior and visualize the results using Principal Component Analysis (PCA).

## Features

- **Data Cleaning**: The data is cleaned by removing null values and filtering out canceled transactions.
- **Feature Engineering**: New features such as `TotalSpent`, `NumPurchases`, and `TotalQuantity` are created to summarize customer behavior.
- **KMeans Clustering**: The dataset is clustered into different segments using the KMeans algorithm.
- **PCA for Visualization**: PCA is applied to reduce the dimensionality of the data, making it easier to visualize the clusters.
- **Visualization**: The clusters are visualized in a 2D space using Seaborn and Matplotlib.

## Dataset

The dataset used in this project is the **Online Retail II** dataset, which can be found on Kaggle.

- **File**: `online_retail_II.xlsx`
- **Sheets**: 
  - `Year 2009-2010`
  - `Year 2010-2011`

## Requirements

- Python 3.7+
- Required libraries are listed in the `requirements.txt` file.

## Installation

1. **Clone the repository:**

2. **Install dependencies:**

    ```sh
    pip install -r requirements.txt
    ```

3. **Download the dataset:**
   - Download the **Online Retail II** dataset from [Kaggle](https://www.kaggle.com) and place it in the project directory.

## Running the Project

1. **Load and Clean Data:**
   - The data is loaded from two sheets and cleaned by removing null values and canceled transactions (indicated by `Invoice` numbers starting with "C").

2. **Feature Engineering:**
   - Calculate `TotalSpent`, `NumPurchases`, and `TotalQuantity` for each customer.

3. **Standardize the Data:**
   - The features are standardized using `StandardScaler` to prepare them for clustering.

4. **Determine Optimal Clusters:**
   - The `Elbow Method` is used to determine the optimal number of clusters by plotting the Within-Cluster Sum of Squares (WCSS) for different cluster numbers.

5. **Apply KMeans Clustering:**
   - The data is clustered into 4 segments based on customer purchasing behavior.

6. **Describe Clusters:**
   - A summary of each cluster is provided, including the average spending, number of purchases, and total quantity purchased.

7. **PCA and Visualization:**
   - PCA is applied to reduce the dimensionality of the data, and the clusters are visualized in 2D space.

## Visualization

- **Elbow Method Plot**: Displays the WCSS for different numbers of clusters.
  ![image](https://github.com/user-attachments/assets/9f0c6e40-8d0a-406a-ac4f-5e9ed20b1248)
- **PCA Scatter Plot**: Shows the distribution of customer segments in a 2D space.
  ![image](https://github.com/user-attachments/assets/dfedc76d-07a9-4cfe-806f-81157b26ca13)


## Cluster Descriptions

The clusters identified are as follows:

1. **Regular Customers**:
   - Many customers with low average spending and few purchases.
  
2. **Top Customers**:
   - Very few customers with extremely high spending and a large number of purchases.

3. **Loyal Customers**:
   - Moderate number of customers with consistent purchasing behavior and decent spending.

4. **Major Clients**:
   - Few customers with high spending but fewer purchases than the top customers.

## Example Output

```sh
Cluster 0:
- Number of Customers: 5428
- Average Total Spent: $1417.85
- Average Number of Purchases: 4.01
- Average Total Quantity: 828.57

Cluster 1:
- Number of Customers: 5
- Average Total Spent: $388,765.20
- Average Number of Purchases: 198.80
- Average Total Quantity: 212,321.40

Cluster 2:
- Number of Customers: 420
- Average Total Spent: $13,238.20
- Average Number of Purchases: 27.82
- Average Total Quantity: 7,530.19

Cluster 3:
- Number of Customers: 28
- Average Total Spent: $90,838.97
- Average Number of Purchases: 91.21
- Average Total Quantity: 71,398.25
