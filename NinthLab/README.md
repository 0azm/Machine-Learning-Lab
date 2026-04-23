# Lab 9: Decision Trees and Random Forests
Name: Azam Ahmed Alburiki  
ID: 2240005783  

## Part 1: Dataset Selection
Dataset Used: LendingClub.com Loan Data (2007-2010).

Format: CSV file containing 9,578 records and 14 features.

Data Source: loan_data.csv.

## Part 2: Problem Definition
Problem Type: This is a Supervised Learning task.

Machine Learning Task: Classification (Decision Tree and Random Forest).

Target Variable: The target is the not.fully.paid column (Binary: 1 if the loan was not paid back, 0 otherwise).

Objective: Predict whether a borrower will pay back their loan in full based on their credit profile (FICO score, debt-to-income ratio, purpose of loan, etc.) and compare the performance of a single Decision Tree against a Random Forest ensemble.

## Part 3: Data Inspection Summary
Dimensions: The dataset consists of 9,578 rows and 14 columns.

Features: Includes numerical data (FICO score, interest rate, installment) and categorical data (loan purpose).

Methodology: The data was loaded using Pandas. Since "purpose" is a categorical feature, I utilized dummy variables (pd.get_dummies) to convert it into a format the models could process. Initial EDA using Seaborn histograms showed a clear relationship between higher FICO scores and a higher probability of credit policy approval.

## Part 4: Machine Learning Methodology Diagram
Included below is the logical workflow of the project, comparing two tree-based models.

### Methodology Steps:

Exploratory Data Analysis: Creating overlapping histograms of FICO scores and countplots of loan purposes to understand the distribution of risky vs. safe borrowers.

Categorical Encoding: Converting the "purpose" column into multiple dummy variable columns using pd.get_dummies to handle non-numerical data.

Data Splitting: Partitioning the data into Training and Testing sets (70/30 split) using train_test_split.

Decision Tree Training: Initializing and fitting a single DecisionTreeClassifier to the training data.

Decision Tree Evaluation: Analyzing performance via a Confusion Matrix and Classification Report.

Random Forest Training: Initializing a RandomForestClassifier with 600 estimators to provide an ensemble approach and reduce the risk of overfitting.

Comparative Analysis: Comparing the two models to observe how the Random Forest averages multiple trees to improve overall accuracy and stability across the test set.
