# **Customer Segmentation using K-Means Clustering**

This project performs customer segmentation using  **K-Means clustering**  on synthetic customer data.  
The goal is to identify distinct customer groups based on:

-   **Age**
    
-   **Annual Income**
    
-   **Spending Score**
    

The notebook includes data preprocessing, clustering evaluation, PCA visualization, and cluster insights.

----------

## **📌 Project Overview**

This project demonstrates the complete clustering workflow:

1.  Data generation (Age, Income, Spending Score)
    
2.  Standardization using  **StandardScaler**
    
3.  Optimal cluster selection using:
    
    -   **Elbow Method (Inertia)**
        
    -   **Silhouette Score**
        
4.  Running  **K-Means**  clustering
    
5.  Dimensionality reduction using  **PCA**
    
6.  Visualization of clusters in 2D
    
7.  Cluster insights and summary statistics
    

----------

## **📂 Technologies Used**

-   **Python**
    
-   **NumPy**
    
-   **Pandas**
    
-   **Matplotlib**
    
-   **Seaborn**
    
-   **Scikit-learn**
    
    -   StandardScaler
        
    -   KMeans
        
    -   PCA
        
    -   Silhouette Score
        

----------

## **📊 Workflow**

### **1. Data Creation**

A synthetic dataset of 200 customers is created using random values for:

-   Age (18–65)
    
-   Annual Income (15k–150k)
    
-   Spending Score (1–100)
    

### **2. Data Scaling**

`scaler = StandardScaler()
X_scaled = scaler.fit_transform(df)` 

### **3. Optimal K Selection**

-   **Inertia plot (Elbow Method)**
    
-   **Silhouette Score plot**
    

Both help identify the best number of clusters.

### **4. K-Means Clustering**

`kmeans = KMeans(n_clusters=4, init='k-means++', n_init=10, random_state=42)
labels = kmeans.fit_predict(X_scaled)
df['Cluster'] = labels` 

### **5. PCA for Visualization**

Reduces 3D features → 2D for plotting.

### **6. Cluster Insights**

Cluster means for Age, Income, and Spending Score are computed.

----------

## **📈 Visualizations**

The notebook generates the following plots:

-   Elbow Method curve
    
-   Silhouette Score curve
    
-   PCA-based 2D cluster visualization
    
-   Cluster centroids
    
-   Pairplot showing variable relationships
    

----------

## **📘 Results**

-   **Optimal K:**  4 clusters (chosen based on visual inspection)
    
-   **Metrics Output:**
    
    -   Inertia value
        
    -   Silhouette Score
        
-   **Cluster summaries:**  Mean values of each feature within each cluster
    

----------

## **📁 Folder Structure**

`├── customer_segmentation.ipynb
├── README.md
└── images/   (optional for plots)` 

----------

## **🚀 How to Run the Project**

1.  Clone the repository:
    

`git clone <your-repo-link>` 

2.  Install required libraries:
    

`pip install numpy pandas matplotlib seaborn scikit-learn` 

3.  Run the notebook:
    

`jupyter notebook customer_segmentation.ipynb` 

----------

## **📌 Future Enhancements**

-   Add real-world dataset (Mall Customer Dataset, E-commerce data, etc.)
    
-   Try other clustering techniques:
    
    -   DBSCAN
        
    -   Agglomerative Clustering
        
-   Perform hyperparameter tuning
    
-   Build a dashboard for cluster exploration
