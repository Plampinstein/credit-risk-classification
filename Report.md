# Module 20 Report - Credit Risk

## Overview of the Analysis

* Explain the purpose of the analysis.
    The aim of this analysis is to forecast the financial reliability or creditworthiness of borrowers, determining whether a loan should be classified as a "Healthy Loan" or a "High-Risk Loan" based on the provided financial information.
    
* Explain what financial information the data was on, and what you needed to predict.
    I utilized a dataset found in the "lending_data.csv". This dataset encompassed a range of financial and credit-related details pertaining to borrowers. These details comprised information such as loan size, interest rate, borrower income, debt-to-income, number of accounts, derogatory marks, total debt, and loan status. 
    
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`). 
        The variable I aimed to predict was "loan_status," a binary indicator denoting whether a loan is considered healthy (0) or high-risk (1).

* Describe the stages of the machine learning process you went through as part of this analysis.
    The stages I went through are as followed:
    
Split the Data into Training and Testing Sets
    Step 1: Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
    Step 2: Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
    Step 3: Check the balance of the labels variable (y) by using the value_counts function.
    Step 4: Split the data into training and testing datasets by using train_test_split.¶
Create a Logistic Regression Model with the Original Data
    Step 1: Fit a logistic regression model by using the training data (X_train and y_train).
    Step 2: Save the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model.
    Step 3: Evaluate the model’s performance by doing the following:
        a)Calculate the accuracy score of the model.
        b)Generate a confusion matrix.
        c)Print the classification report.
    
    
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
    In this analysis I used a logistic regression model (as requested in the instructions). A logistic regression is a statistical method used for predicting the probability of a binary outcome, in this case whether a loan is considered healthy (0) or high-risk (1).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  
    1.-Accuracy Score: 0.952: This score suggests that the model is correct in its predictions approximately 95.2% of the time.
  
    2.-Precision: For class 0, precision is perfect (1.00), indicating that all instances predicted as class 0 are indeed class 0.
    For class 1, precision is 0.85, meaning that 85% of the instances predicted as class 1 are correct.
    3.-Recall: Class 0 has a recall of 0.99, indicating that the model correctly identifies 99% of all instances of class 0.
    Class 1 has a recall of 0.91, suggesting that the model captures 91% of all instances of class 1.
    

* Machine Learning Model 2:
  * the second model gave me the same results on accuracy score (95.2%), precision class 1, 100% adn class 2 85%) and recall (class 0, 99%, and class 1, 91%)

## Summary

    In summary, the model has high accuracy and performs well in classifying both classes, with particularly good performance for class 0. However, it's essential to consider both precision and recall, as they provide insights into how well the model is doing for each specific class.
