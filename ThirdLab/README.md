# Lab 3: Exploratory Data Analysis (EDA) - Titanic Dataset

**Name:** Azam Ahmed Alburiki  
**ID:** 2240005783

## Project Objective
The primary goal of this lab was to perform an in-depth **Exploratory Data Analysis (EDA)** on the Titanic passenger dataset. By identifying patterns, handling anomalies, and visualizing relationships, we establish a solid foundation for building predictive machine learning models in future labs.

## Key EDA Findings

### 1. Fare Distribution (Economic Diversity)
* **Visualization:** Histogram with Kernel Density Estimate (KDE).

* **Finding:** The ticket prices are **right-skewed**.
* **Analysis:** Most passengers paid low-cost fares ($10–$30), representing the large population of 3rd Class. A few "outlier" fares represent the luxury suites in 1st Class.

### 2. Survival Rate by Passenger Class
* **Visualization:** Bar Plot.
* **Finding:** There is a clear linear correlation between socio-economic status and survival probability.
* **Analysis:** 1st Class passengers had significantly better access to lifeboats and higher priority during evacuation compared to 3rd Class passengers.

### 3. Survival Probability Trend by Age
* **Visualization:** Line Plot (Trend Analysis).

* **Finding:** The highest survival probability is found at **Age 0 (Infants)**.
* **Analysis:** This provides empirical evidence for the "Women and Children First" protocol. The trend line peaks for infants and children, dips for young adults, and fluctuates for the elderly.

## Technical Implementation
* **Data Grouping:** Ages were "binned" into 5-year intervals to create a smoother, more readable trend line.
* **Libraries Used:** `Pandas` for data grouping and statistical aggregation.
    * `Seaborn` and `Matplotlib` for high-quality statistical visualizations.
* **Data Cleaning:** Focused on identifying missing values and understanding the 80/20 rule of data science (80% preparation, 20% modeling).

## Conclusion
This EDA process revealed that survival on the Titanic was not random. **Class** and **Age** emerged as primary predictors of survival. These insights will be used to select the most relevant features for the Classification models in the next stage of the project.
