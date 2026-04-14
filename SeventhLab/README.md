## Lab 7: Advertising Click Analysis (Logistic Regression)  
Name: Azam Ahmed Alburiki  
ID: 2240005783  

# Part 1: Dataset Selection
**Dataset Used:** Advertising Dataset.

**Format:** CSV file containing 1,000 records and 10 features.  

**Data Source:** advertising.csv.

# Part 2: Problem Definition
**Problem Type:** Supervised Learning.

**Machine Learning Task:** Classification (Logistic Regression).  

**Target Variable:** The target is the 'Clicked on Ad' column (Binary: 0 for No, 1 for Yes).    

**Objective:** Build a classification model to predict whether a user will click on an advertisement based on their demographic data and internet usage patterns (Daily Time Spent on Site, Age, Area Income, and Daily Internet Usage).  
  
**Part 3:** Data Inspection Summary
**Dimensions:** The dataset consists of 1,000 rows and 10 columns.  

**Features:** Features include numerical floats and integers (Daily Time Spent on Site, Age, Area Income, Daily Internet Usage, Male) and categorical strings (Ad Topic Line, City, Country, Timestamp). 
  
**Methodology:** Data was inspected using Pandas. Visual exploration via Seaborn (Jointplots and Pairplots) revealed clear clusters, particularly showing that users who spend less time on the internet and are slightly older have a higher probability of clicking an advertisement.

# Part 4: Machine Learning Methodology Diagram  
Included below is the visual workflow of the project, from data ingestion to classification metrics.

**Methodology Steps:**  
**Data Loading:** Importing the Advertising dataset.  

**Exploratory Data Analysis:** Using sns.jointplot and sns.pairplot to identify that "Daily Internet Usage" is a primary separator for the target classes.  

**Feature Selection:** Defining predictors ($X$) as the numerical features (Time Spent, Age, Income, Internet Usage, Male) and the target ($y$) as 'Clicked on Ad'.Data   

**Splitting:** Partitioning the data into Training and Testing sets (67/33 split).  
  
**Model Training:** Utilizing a Logistic Regression estimator from the Scikit-Learn library.  
  
**Evaluation:** Analyzing model performance using a Classification Report and a Confusion Matrix.  
  
**Interpretation:** The model achieved an overall accuracy of 91%, with a very high precision of 0.96 for predicting ad clicks, indicating it is highly reliable for targeting potential customers.
