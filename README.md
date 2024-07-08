This project implements a K-Means clustering algorithm to group customers of a retail store based on their purchase history. Clustering customers helps in identifying different customer segments, understanding their behaviors, and tailoring marketing strategies accordingly.

Prerequisites Python 3.x Libraries: numpy pandas scikit-learn matplotlib seaborn You can install the required libraries using:

pip install numpy pandas scikit-learn matplotlib seaborn Project Structure . ├── data │ └── customers.csv ├── src │ ├── kmeans_clustering.py │ ├── data_preprocessing.py │ └── visualize.py ├── README.md └── main.py Data The customers.csv file should contain the purchase history data of the customers. It should include the following columns:

CustomerID: Unique identifier for each customer PurchaseHistory: Historical purchase data (e.g., total spending, number of purchases) Steps

Data Preprocessing File: src/data_preprocessing.py
Load the data from customers.csv. Handle missing values if any. Normalize the purchase history data for better clustering performance. 2. K-Means Clustering File: src/kmeans_clustering.py

Implement the K-Means clustering algorithm. Choose the appropriate number of clusters (k) using methods like the Elbow method. Fit the model to the normalized data. 3. Visualization File: src/visualize.py

Visualize the clusters using 2D scatter plots. Optionally, use dimensionality reduction techniques (e.g., PCA) if the data is high-dimensional. 4. Main Script File: main.py

Integrate all the steps. Execute the script to perform clustering and visualize the results. Usage Data Preprocessing

from src.data_preprocessing import preprocess_data

data = preprocess_data('data/customers.csv') K-Means Clustering

from src.kmeans_clustering import kmeans_clustering

clusters = kmeans_clustering(data, n_clusters=5) Visualization

from src.visualize import plot_clusters

plot_clusters(data, clusters) Run the Main Script

