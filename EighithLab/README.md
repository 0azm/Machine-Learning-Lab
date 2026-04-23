# Lab 7: K-Nearest Neighbors Classification  
Name: Azam Ahmed Alburiki  
ID: 2240005783

## Part 1: Dataset Selection  
Dataset Used: Classified Data (Artificial/Anonymized).
  
Format: CSV file containing 1,000 records and 11 features.  

Data Source: KNN_Project_Data.csv.  

## Part 2: Problem Definition  
Problem Type: This is a Supervised Learning task.  

Machine Learning Task: Classification (K-Nearest Neighbors).  
  
Target Variable: The target is the TARGET CLASS column (Binary: 0 or 1).  

Objective: Build a predictive model to classify data points based on anonymized features. The goal is to demonstrate the importance of feature scaling and find the optimal "K" value using the Elbow Method to minimize classification errors.  

## Part 3: Data Inspection Summary  
Dimensions: The dataset consists of 1,000 rows and 11 columns.  
  
Features: All features are numerical but anonymized (labeled as 'WTT', 'PTI', etc.). The data has varying scales, requiring normalization before processing.
  
Methodology: The dataset was loaded and inspected using the Pandas and NumPy libraries in a Jupyter Notebook environment. Initial exploration through sns.pairplot confirmed that the features are continuous and that the classes are somewhat separable, though scaling is required to avoid distance-calculation bias.
  
## Part 4: Machine Learning Methodology Diagram  
Included below is the logical workflow of the project, from data standardization to final evaluation.
  
### Methodology Steps:
  
Data Standardization: Utilizing StandardScaler from Scikit-Learn to ensure all features have a mean of 0 and a standard deviation of 1.
 
Exploratory Data Analysis: Visualizing relationships and class separation using Seaborn pairplots.

Data Splitting: Partitioning the standardized data into Training and Testing sets (70/30 split).

Baseline Model: Training an initial KNeighborsClassifier with K=1 to establish a performance baseline.

Hyperparameter Tuning: Implementing a for loop to test K values from 1 to 40.

The Elbow Method: Plotting the Error Rate vs. K Value to visually identify the point of diminishing returns (the "elbow").

Final Evaluation: Retraining the model with the optimized K value (K=30) and analyzing the results through a Confusion Matrix and a Classification Report (Precision, Recall, and F1-Score).
