# Customer-Segmentation-for-Retail-Business



### Project Overview

This project aims to segment retail customers based on their purchasing behavior using the RFM (Recency, Frequency, Monetary) model and K-Means clustering. By identifying customer segments, businesses can tailor their marketing strategies to different customer groups, improving customer retention and increasing sales.

### Dataset

- The dataset used in this project is a retail dataset containing transactions made by customers. Each row represents a transaction, with columns including `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`, and `TotalPrice`.
- **File:** `Online-Data.xlsx`

### Key Steps

1. **Data Preprocessing:**
   - Converted `InvoiceDate` to datetime format.
   - Created a new column, `TotalPrice`, calculated by multiplying `Quantity` and `UnitPrice`.
   - Handled missing values and ensured `Quantity` and `UnitPrice` are numeric.

2. **RFM Calculation:**
   - **Recency:** Days since the customer's last purchase.
   - **Frequency:** Total number of purchases made by the customer.
   - **Monetary:** Total amount spent by the customer.
   - The RFM metrics were calculated and stored in a new DataFrame.

3. **Data Standardization:**
   - Standardized the RFM data to bring all features onto the same scale using `StandardScaler`.

4. **K-Means Clustering:**
   - The optimal number of clusters was determined using the Elbow Method.
   - K-Means clustering was applied with the optimal number of clusters (4 clusters in this case).
   - Each customer was assigned to a cluster based on their RFM metrics.

5. **Visualization:**
   - Boxplots were created to visualize the distribution of Recency, Frequency, and Monetary values across clusters.
   - A heatmap was generated to display the average RFM metrics for each cluster.

6. **High-Value Customer Identification:**
   - The cluster with the highest average monetary value was identified.
   - The top 5 high-value customers were listed based on their monetary value.

### Results

- **Number of High-Value Customers:** 5
- **Top 5 High-Value Customers:**
   - CustomerID: 14646, Monetary: 279489.02
   - CustomerID: 18102, Monetary: 256438.49
   - CustomerID: 17450, Monetary: 187482.17
   - CustomerID: 12415, Monetary: 123725.45
   - CustomerID: 14156, Monetary: 113384.14

### Dependencies

- Python 3.x
- Libraries:
  - pandas
  - numpy
  - sklearn
  - matplotlib
  - seaborn

### How to Run

1. Install the required libraries using `pip install -r requirements.txt`.
2. Place the `Online-Data.xlsx` file in the project directory.
3. Run the Jupyter notebook to preprocess data, perform clustering, and visualize the results.

### Future Enhancements

- Improve the clustering model by experimenting with other clustering algorithms like DBSCAN or hierarchical clustering.
- Add customer segmentation insights to guide marketing strategies.


