## Lab 5: Feature Engineering (Classification)  
Name: Azam Ahmed Alburiki  
ID: 2240005783  

# Part 1: Dataset Selection  
**Dataset Used:** Talabat-style Orders Dataset.  

**Format:** CSV file containing 100,000 records and 23 features.  

**Data Source:** talabat_enhanced_orders.csv.  

# Part 2: Problem Definition  
**Problem Type:** This is a Supervised Learning task.  
  
**Machine Learning Task:** Multi-class Classification.  

**Target Variable:** The target is the Order_Status column (categorical: Delivered, Cancelled, In Transit).  

**Objective:** Build a baseline model to predict the status of an order and understand how feature engineering choices (time, price, and distance-based) affect model performance and feature importance.  

# Part 3: Data Inspection Summary  
**Dimensions:** The dataset consists of 100,000 rows and 23 columns.  

**Features:** Data types include a mix of integers (Quantity), floats (Total_Price, Delivery_Distance_km, Lat/Lon coordinates), and objects/strings (Item_Name, City, Traffic_Level).  

**Methodology:** The dataset was loaded and inspected using the Pandas and NumPy libraries in a Jupyter Notebook environment. Initial checks confirmed the data is clean with no missing values or duplicate rows.  

# Part 4: Machine Learning Methodology Diagram  
Included below is the visual workflow of the project, from data loading to feature importance interpretation.  

**Methodology Steps:**  

**Data Loading:** Importing the enhanced orders dataset.   

**Feature Selection:** Defining predictors while avoiding data leakage (e.g., removing Delivery_Time which directly determines status).  

**Feature Engineering:** Creating new metrics such as time-based (hour, day), price-based, and distance-based features.  

**Preprocessing:** Encoding categorical features using OneHotEncoder and scaling numerical data.  

**Model Training:** Utilizing a Random Forest classifier within a Scikit-Learn Pipeline.  

**Evaluation:** Analyzing performance via Classification Reports and interpreting Feature Importance scores.
