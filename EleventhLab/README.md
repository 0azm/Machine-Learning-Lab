# Lab 11: Credit Card Customer Segmentation (K-Means Clustering)

**Name:** Azam Ahmed Alburiki  
**ID:** 2240005783


## Part 1: Dataset Selection

* **Dataset Used:** Credit Card Dataset for Clustering
* **Format:** CSV File (`CC_GENERAL.csv`)
* **Data Source:** [Kaggle CC General Dataset](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata/data)
* **Contents:** 8,950 samples with 18 behavioral variables (e.g., `BALANCE`, `PURCHASES`, `CASH_ADVANCE`, `PAYMENTS`, `TENURE`) describing credit card usage over a 6-month period.



## Part 2: Problem Definition

* **Problem Type:** Unsupervised Learning
* **Machine Learning Task:** Customer Segmentation using **K-Means Clustering**.
* **Target Variable:** None (Unlabeled data).
* **Objective:** To group credit card holders into distinct behavioral segments. By identifying these clusters, a company can understand different customer profiles and design targeted marketing strategies (e.g., offering rewards to high-spenders or lower interest rates to those relying on cash advances).



## Part 3: Data Inspection & Cleaning Summary

* **Dimensions:** 8,950 rows and 18 columns.
* **Data Cleaning:**
    * **Feature Selection:** Dropped the `CUST_ID` column as it is a unique identifier and does not provide behavioral value for clustering.
    * **Handling Missing Values:** Identified null values in `CREDIT_LIMIT` and `MINIMUM_PAYMENTS`. Applied **Mean Imputation** to fill these gaps.
* **Findings:** The data features exist on different scales. Because K-Means is a distance-based algorithm, **Standardization** (Scaling) was required to prevent features with large ranges from dominating the model.



## Part 4: Machine Learning Methodology

The project followed a structured unsupervised learning pipeline to identify and validate customer segments.

### Methodology Workflow:

1. **Exploratory Data Analysis (EDA):** Analyzed summary statistics and distributions to understand spending and payment patterns.
2. **Data Preprocessing:** Implemented `StandardScaler` to normalize the dataset, ensuring each feature contributes equally to the clustering process.
3. **Optimal Cluster Selection (The Elbow Method):**
    * Ran the K-Means algorithm for a range of cluster values (K).
    * Plotted the **Inertia** (Within-cluster sum of squares) to find the "Elbow" point, which indicated the optimal number of clusters (K=3).
4. **Model Training:** Fitted the final `KMeans` model using the optimal cluster count.
5. **Dimensionality Reduction (PCA):** Applied **Principal Component Analysis** to reduce the data to two dimensions for visual inspection of the cluster separations.
6. **Model Evaluation:** Calculated the **Silhouette Score** to evaluate how well-defined and separated the resulting clusters were.
7. **Final Segment Interpretation:**
    * **Cluster 0 (Active Buyers):** High purchase frequency and balance; valuable for loyalty programs.
    * **Cluster 1 (Cash Advance Users):** High reliance on cash withdrawals; target for interest rate offers.
    * **Cluster 2 (Passive Users):** Low overall activity; target for re-engagement campaigns.



## Dependencies

* **Python 3.x**
* **Pandas / Numpy:** Data manipulation and numerical analysis.
* **Matplotlib / Seaborn:** Data visualization and cluster plotting.
* **Scikit-Learn:** Preprocessing (`StandardScaler`), Clustering (`KMeans`), Dimensionality Reduction (`PCA`), and Evaluation (`Silhouette Score`).
