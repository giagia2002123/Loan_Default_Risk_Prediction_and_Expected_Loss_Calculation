# Loan Default Risk Prediction and Expected Loss Calculation

This project focuses on predicting the probability of loan default using machine learning techniques and utilizing these predictions to calculate the expected loss for each loan. The dataset used in this project contains various loan attributes, such as credit score, loan amount, interest rates, etc., which are employed to build the prediction model.

## Project Overview

### 1. **Objective**

The main objective of this project is to predict the probability of default for each loan in the dataset and subsequently calculate the expected loss based on these probabilities. This allows financial institutions to better understand the potential risks associated with lending.

### 2. **Dataset**

The dataset used in this project contains 10,000 records and 8 columns. Below is a brief description of each attribute:

1. **customer_id**: A unique identifier for each customer.
2. **credit_lines_outstanding**: The number of credit lines (loans, credit cards, etc.) the customer currently has outstanding.
3. **loan_amt_outstanding**: The current outstanding amount on the customer's loan.
4. **total_debt_outstanding**: The total debt amount, including all other liabilities, that the customer has.
5. **income**: The annual income of the customer.
6. **years_employed**: The number of years the customer has been employed.
7. **fico_score**: The customer's FICO score, which is a measure of creditworthiness.
8. **default**: A binary variable indicating whether the customer has defaulted on the loan (1 = defaulted, 0 = not defaulted).

This dataset is used to predict the probability of loan default based on various customer attributes and calculate the expected loss for each loan.


### 3. **Methodology**

- **Data Preprocessing**: 
    - Handle missing values
    - Apply correlation test
    - Feature selection
    - Handle class imbalance with SMOTE
    - Using train-test-split
    - Apply standard scaler
- **Modeling**: A variety of machine learning models are applied, including logistic regression and other classification techniques.
- **Prediction of Default Probability**: The models output the likelihood of a loan defaulting.
- **Expected Loss Calculation**: Using the predicted probability of default, the expected loss is calculated as:
    - `Expected Loss = (1 - recovery_rate) × PD × loan_amt_outstanding`
        - Where
            - **recovery_rate**: The percentage of the loan amount that is expected to be recovered in the event of default. (For this problem, recovery_rate is set at 0.10)
            - **PD**: Probability of Default, which indicates the likelihood that a borrower will default on their loan.
            - **loan_amt_outstanding**: The total amount of the loan that is currently outstanding.



### 4. **Results**

The model is evaluated using metrics such as accuracy, precision, recall, and ROC-AUC. After identifying the best-performing model, we use it to predict the probability of default on unseen data and calculate the expected loss for each loan.

### 5. **Conclusion**

This model provides a robust framework for predicting default risk and calculating expected losses, helping to minimize risk in lending portfolios.

## Repository Structure

- `notebooks/`: Contains the main Jupyter notebook file where the analysis and model building are performed.
- `data/`: Raw dataset used in the project.

## Usage

After running the notebook, you will be able to:
- View the entire process of preprocessing dataset.
- Train the predictive model.
- Make predictions for probability of default.
- Calculate the expected loss.

## Technologies Used

- **Python**: For data analysis and modeling.
- **Google Colab**: For running the Jupyter notebook online.
- **Libraries**: 
  - `pandas`
  - `imbalanced-learn`
  - `scikit-learn`
  - `xgboost`

## Author

- **Ngo Trieu Gia Gia** - [GitHub Profile](https://github.com/giagia2002123)

## Data Source

The dataset used in this project was provided by the **Quantitative Research JPMORGAN CHASE & CO** career simulation on the [Forage website](https://www.theforage.com/). This dataset was part of a training exercise to develop skills in financial analysis and quantitative research.