## Loan_Default_Prediction

# Project Overview
The loan default prediction project focuses on predicting whether a borrower will fully pay off their loan or default (charge off), using the LendingClub loan dataset (2007 to 2018). It combines structured financial information with borrower provided text descriptions to make the prediction. This project is build in multiple phases starting with data cleaning and preprocessing, followed by text processing, model training and model evaluation. In phase three the model is trained using machine learning models on three types of input : 
- Structured data only : income, interest rate, loan amount, credit history, etc.
- Text data only : TF-IDF features extracted from the borrower's written loan description.
- Hybrid : structured data + text data combined.<br>
The goal is to see which model and which feature combination best predicts loan default. 

# Dataset
In the project LendingClub dataset is used covering loans from 2007 to 2018. The original dataset contains approximately 2.26 million records and 151 columns. After selecting the relevant loan outcomes, the dataset contains 1,345,310 records. The target variable is loan_status, if fully paid denoted as 1 and charged off (defaulted) denoted as 0. 

# Project Structure 
The project is divided into following phases: 
1. Dataset loading and cleaning
2. Exploratory data preparation
3. Feature selection and preprocessing
4. Borrower text preprocessing
5. TF-IDF feature extraction
6. Creation of structured, text and hybrid feature sets
7. Handling class imbalance using SMOTE
8. Machine learning model training
9. Model comparison and evaluation

# Data Preprocessing 
The original dataset contains a large number of columns, including many columns with a high percentage of missing values or information that is not required for this prediction task. The preprocessing phase includes removing unwanted columns, keeping only fully paid and charged off loans, converting the target variable to binary values (0 or 1), selecting features, filling missing numerical values and categorical values, normalising numerical features. After feature selection, 18 columns were retained, including the target variable and borrower description.

# NLP and Text Processing
The borrower 'desc' column is used for the text based part of the project. Many records do not contain a borrower description, so missing descriptions are converted to empty strings. The text preprocessing includes converting text to lowercase, removing numbers, removing punctuation, splitting text into words, removing english stop words. TF-IDF is then used to convert the cleaned borrower descriptions into numerical features. 

# Feature Sets
Three different feature sets are used in the modelling stage:
1. Structured features contains financial and borrower information from the dataset.
2. Text features contain the TF-IDF representation of borrower descriptions.
3. Hybrid features combine the structured features with the TF-IDF text features. This allows the performance of the models to be compared across the three approaches.

# Machine Learning Models
The following models are implemented : Logistic Regression, Random Forest and XGBoost. And each model is trained using Structured features, Text features and Hybrid features. 

# Model Evaluation
The models are evaluted using accuracy, precison, recall, f1 score.

# Current Results
The current model comparison shows that the best F1 score in the present implementation is obtained by XGBoost using the structured features. The text only models currently perform considerably worse than the structured and hybrid approaches. 





