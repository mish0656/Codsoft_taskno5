# Codsoft_taskno5
Credit Card Fraud Detection
This code is a Python script that demonstrates the process of building a logistic regression model to detect fraudulent credit card transactions using a credit card dataset. The code reads the data from a CSV file, preprocesses it, handles outliers, and finally trains a logistic regression model to make predictions. Here's a step-by-step explanation of the code:

1. Importing Libraries:
   - The necessary Python libraries are imported: `numpy`, `pandas`, `matplotlib`, `seaborn`, and `sklearn`.

2. Reading Data:
   - The credit card dataset is read from a CSV file using pandas, and the first few rows of the dataset are displayed using the `head()` function.

3. Data Exploration:
   - The shape of the dataset (number of rows and columns) is displayed using the `shape` attribute.
   - Summary statistics for the 'Time', 'Amount', and 'Class' columns are displayed using `describe()`.
   - The `isna().any()` function is used to check for missing values in the dataset.

4. Class Distribution:
   - The code calculates and prints the number and percentage of fraud and genuine transactions in the dataset.

5. Outliers:
   - A scatter plot is created to visualize the distribution of 'Amount' and 'Time'.
   - Fraudulent and genuine transactions are separated into different dataframes ('fraud' and 'genuine').
   - Summary statistics for the 'Amount' column in both fraudulent and genuine transactions are displayed.

6. Building a Sample Dataset:
   - A balanced sample dataset is created by randomly selecting 492 genuine transactions (to match the number of fraud transactions) using the `sample()` function.
   - The new dataset is constructed by concatenating the genuine sample with the fraud transactions.

7. Data Splitting:
   - The dataset is split into input features (X) and target variable (y).
   - The data is further divided into training and testing sets using the `train_test_split()` function.

8. Model Training and Evaluation:
   - A logistic regression model is created using `LogisticRegression()` from sklearn.
   - The model is trained on the training data using `fit()` function.
   - Predictions are made on the test data, and the accuracy score is calculated using the `score()` function.
   - The confusion matrix is computed using `confusion_matrix()`.
   - The accuracy score and confusion matrix are printed.

The main goal of this code is to demonstrate the process of building a logistic regression model for detecting fraudulent transactions. However, there are a few improvements that can be made, such as handling class imbalance with advanced techniques like resampling (oversampling, undersampling) or using class weights, hyperparameter tuning, and cross-validation for a more robust evaluation of the model. Additionally, it would be helpful to add comments to the code to make it more readable and self-explanatory.
