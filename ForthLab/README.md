# Titanic Data Preprocessing & Dimensionality Reduction

This Lab demonstrates a robust data science pipeline for cleaning and analyzing the Titanic passenger dataset. The primary focus is on handling missing values, managing outliers, and evaluating the relationship between passenger ticket costs (**Amount**) and passenger **Age**.

## 🚀 Lab Overview
In this analysis, we explore the correlation between financial metrics and passenger demographics. Our findings show that ticket amounts and ages operate independently, which provides a unique challenge for predictive modeling (e.g., predicting survival).

## 🛠️ Data Preprocessing Steps

### 1. Data Cleaning & Imputation
* **Missing Values:** Handled null entries in the `Amount` column using **Median Imputation** to maintain data integrity without introducing significant bias.
* **Outlier Management:** Implemented **Winsorization (Capping)** at the 5th and 95th percentiles. This prevents extreme ticket prices (luxury suites) from skewing the statistical analysis while retaining all records.

### 2. Feature Scaling
* **Standardization:** Applied `StandardScaler` to normalize the scales of `Amount` and `Age`.
* **Result:** Features are transformed to a Mean of **0** and a Standard Deviation of **1**, making them suitable for machine learning algorithms like PCA and K-Means.

### 3. Correlation Analysis
* **Heatmap Visualization:** Generated a correlation matrix to quantify the relationship between features.
* **Findings:** A correlation coefficient of approximately **-0.013** was observed, indicating **no linear relationship** between the cost of a ticket and the age of the passenger.

### 4. Dimensionality Reduction (PCA)
* **Technique:** Principal Component Analysis (PCA).
* **Evaluation:** Due to the low correlation between features, PCA was utilized primarily for demonstration. The explained variance ratio showed that information is split across components, suggesting that dimensionality reduction offers limited benefits for this specific dataset.

## 📊 Visualizations
* **Correlation Heatmap:** Highlighting the independence of numerical features.
* **Scatter Plot:** Visualizing the "cloud" distribution of standardized data to confirm the lack of linear patterns between Age and Fare.

## 💻 Tech Stack
* **Language:** Python 3.12
* **Libraries:** * `Pandas` & `NumPy`: Data manipulation
    * `Scikit-Learn`: Scaling and PCA
    * `Matplotlib` & `Seaborn`: Statistical visualization

## 📂 How to Run
1. Ensure you have Python installed.
2. Install dependencies:
   ```bash
   pip install pandas scikit-learn matplotlib seaborn
