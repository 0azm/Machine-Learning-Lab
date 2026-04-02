## Lab 6: Ecommerce Customer Analysis (Linear Regression)  
Name: Azam Ahmed Alburiki  
ID: 2240005783  

# Part 1: Dataset Selection  
**Dataset Used:** Ecommerce Customers Dataset.  

**Format:** CSV file containing 500 records and 8 features.  

**Data Source:** Ecommerce Customers.csv.  

# Part 2: Problem Definition  
**Problem Type:** This is a Supervised Learning task.  

**Machine Learning Task:** Regression (Linear Regression).  

**Target Variable:** The target is the **Yearly Amount Spent** column (numerical).  

**Objective:** Build a predictive model to estimate the total annual spend of a customer based on their behavior metrics (session length, time on app, time on website, and length of membership) to determine whether the company should focus on their Mobile App or Website.  

# Part 3: Data Inspection Summary  
**Dimensions:** The dataset consists of 500 rows and 8 columns.  
 
**Features:** Data types include floats for behavioral metrics (**Avg. Session Length**, **Time on App**, **Time on Website**, **Length of Membership**, **Yearly Amount Spent**) and objects/strings for identifying information (Email, Address, Avatar).  

**Methodology:** The dataset was loaded and inspected using the Pandas and NumPy libraries in a Jupyter Notebook environment. Initial exploration confirmed the data consists of continuous numerical values with strong correlations, making it ideal for a Linear Regression model.  

# Part 4: Machine Learning Methodology Diagram  
Included below is the visual workflow of the project, from data loading to coefficient interpretation.  

**Methodology Steps:**  

1. **Data Loading:** Importing the Ecommerce Customers dataset.  
2. **Exploratory Data Analysis:** Visualizing relationships using Seaborn pairplots and identifying the strong correlation between Length of Membership and Spending.  
3. **Feature Selection:** Defining predictors (X) as the numerical behavior columns and the target (y) as Yearly Amount Spent.  
4. **Data Splitting:** Partitioning the data into Training and Testing sets (60/40 split).  
5. **Model Training:** Utilizing a Linear Regression estimator from the Scikit-Learn library.  
6. **Evaluation:** Analyzing model accuracy using metrics (MAE: 7.74, RMSE: 9.68).  
7. **Interpretation:** Examining the model coefficients to determine that the **Mobile App** (37.89) has a much higher impact on spending than the **Website** (0.56).  
