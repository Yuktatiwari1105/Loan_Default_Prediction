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




