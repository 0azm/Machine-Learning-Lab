# Lab: Support Vector Machine (SVM) Classification

**Name:** Azam Ahmed Alburiki  
**ID:** 2240005783



## Part 1: Dataset Selection
* **Dataset Used:** Iris Flowers Dataset
* **Format:** Scikit-Learn / Seaborn built-in dataset (DataFrame)
* **Data Source:** `sns.load_dataset('iris')`
* **Contents:** 150 samples with 4 features (sepal length, sepal width, petal length, petal width) and 3 target species (Setosa, Versicolor, Virginica).



## Part 2: Problem Definition
* **Problem Type:** Supervised Learning
* **Machine Learning Task:** Multi-class Classification using Support Vector Machines (SVM).
* **Target Variable:** `species` (Setosa, Versicolor, Virginica).
* **Objective:** Build a classifier that can accurately distinguish between three iris species based on flower measurements. The project emphasizes visual exploratory data analysis and hyperparameter optimization using Grid Search to improve classification accuracy.



## Part 3: Data Inspection Summary
* **Dimensions:** 150 rows and 5 columns.
* **Exploratory Analysis:** * Performed a **Pairplot** analysis which revealed that the *Iris-Setosa* species is highly separable from the others.
    * Developed a **KDE Plot** (Kernel Density Estimate) for Setosa sepal dimensions to visualize the concentration of data points.
* **Findings:** While Setosa is easily classified, Versicolor and Virginica show some overlap, necessitating a robust non-linear classifier like an SVM with an RBF kernel.



## Part 4: Machine Learning Methodology

The project followed a structured pipeline to ensure the most accurate model was selected.

### Methodology Workflow:
1.  **Exploratory Data Analysis (EDA):** Visualizing the feature distributions and class clusters using Seaborn.
2.  **Data Splitting:** Using `train_test_split` to divide the data (70% training, 30% testing) to evaluate the model's generalization capability.
3.  **Baseline Model Training:** Initializing an `SVC()` classifier with default parameters (`gamma='auto'`) and fitting it to the training set.
4.  **Initial Evaluation:** Generating a **Confusion Matrix** and **Classification Report** to identify the baseline accuracy and misclassification patterns.
5.  **Hyperparameter Tuning (Grid Search):**
    * Defining a parameter grid for `C` (0.1, 1, 10, 100, 1000) and `gamma` (1, 0.1, 0.01, 0.001, 0.0001).
    * Implementing `GridSearchCV` to automatically find the optimal combination of parameters.
6.  **Final Optimization:** Retraining the model with the best parameters found by the grid search (`refit=True`).
7.  **Final Evaluation:** Comparing the optimized model against the baseline. The final model effectively minimizes errors between the overlapping Versicolor and Virginica classes.


## Dependencies
* Python 3.x
* Pandas
* Matplotlib / Seaborn
* Scikit-Learn
