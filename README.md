# Random Forest Project

This project utilizes publicly available data from [LendingClub.com](www.lendingclub.com). Lending Club connects borrowers with investors, and this project aims to create a model that predicts whether a borrower will pay back their loan in full based on their profile.

## Dataset

The dataset contains lending data from 2007-2010, before Lending Club went public. The data can be downloaded from [here](https://www.lendingclub.com/info/download-data.action) or from the CSV uploaded to the GitHub repository of this project.

### Features

The dataset includes the following columns:

- `credit.policy`: 1 if the customer meets the credit underwriting criteria of LendingClub.com, and 0 otherwise.
- `purpose`: The purpose of the loan (e.g., "credit_card", "debt_consolidation", "educational", etc.).
- `int.rate`: The interest rate of the loan, as a proportion (e.g., 0.11 for 11%).
- `installment`: The monthly installments owed by the borrower if the loan is funded.
- `log.annual.inc`: The natural log of the self-reported annual income of the borrower.
- `dti`: The debt-to-income ratio of the borrower (amount of debt divided by annual income).
- `fico`: The FICO credit score of the borrower.
- `days.with.cr.line`: The number of days the borrower has had a credit line.
- `revol.bal`: The borrower's revolving balance (amount unpaid at the end of the credit card billing cycle).
- `revol.util`: The borrower's revolving line utilization rate (the amount of the credit line used relative to total credit available).
- `inq.last.6mths`: The borrower's number of inquiries by creditors in the last 6 months.
- `delinq.2yrs`: The number of times the borrower had been 30+ days past due on a payment in the past 2 years.
- `pub.rec`: The borrower's number of derogatory public records (bankruptcy filings, tax liens, or judgments).

## Exploratory Data Analysis (EDA)

The following analyses were performed:

1. **Distribution of FICO Scores by Credit Policy**: Histograms to show the distribution.
2. **Distribution of FICO Scores by Not Fully Paid Status**: Histograms to show the distribution.
3. **Count Plot of Loans by Purpose**: Count plot with the color hue defined by `not.fully.paid`.
4. **Trend Analysis**: Jointplot to analyze the trend between FICO scores and interest rates.
5. **Trend Difference Analysis**: Lmplot to see if the trend differed between `not.fully.paid` and `credit.policy`.

## Data Preprocessing

- Converted the categorical feature `purpose` to dummy variables.
- Split the data into training and testing sets.

## Modeling

### Decision Tree

- Trained a Decision Tree model.
- Made predictions and evaluated the model using a confusion matrix and a classification report.

### Random Forest

- Instantiated a Random Forest classifier.
- Trained the model, made predictions, and evaluated it using a confusion matrix and a classification report.

## Results

- **Random Forest Accuracy**: The overall accuracy was better than the Decision Tree.
- **Random Forest Performance**: Performed poorly in terms of recall and F1 score for class 1 compared to the Decision Tree.

## Conclusion

While the Random Forest model had better overall accuracy, it struggled with recall and F1 scores for class 1, indicating room for improvement in predicting borrowers who do not fully repay their loans.

## Files

- `Decision Trees and Random Forest Project.ipynb`: The Jupyter Notebook containing the code and analysis for this project.
