# Loan Default Prediction

## Area of Interest 

The area of interest is predicting loan defaults in the financial sector, specifically within the domain of lending and credit

## The Problem Area

The financial sector is a critical pillar for most developed economies as it enables transactions, investments and provides credit which stimulates growth. However, it faces several challenges, one of which is loan defaults. Loan defaults occur when borrowers are unable to meet the obligations of the repayment terms as agreed with the lending institution. The negative effects of loan defaults include financial loss for lending institutions, reduced trust in financial systems, decreased credit availibility, and in some cases, financial crises. Additionally, over-predicting defaults can lead to missed opportunities and unfair lending practices where creditworthy customers are denied loans. Accurately predicting loan defaults is therefore a significant concer for both lenders and borrowers. 

## How Might We Statement

'How might we leverage sophisticated machine learning techniques to accurately predict loan defaults, thereby assisting financial institutions in making more informed decisions, reducing financial losses, maximizing customer acquisition and promoting fair lending practices.'

## Affected Parties

Financial institutions that provide loans to individuals and businesses experience these challenges. Additionally, borrowers who are denied loans due to inaccurate predictions are also negatively affected. The ripple effects can also significantly impact the financial health of the economy at large as witnessed during the US financial crash in 2008. By utilizing sophisticated machine learning techniques and improving the accuracy of loan default predictions, financial institutions can benefit from improved decision making, enhanced risk management and more effective customer acquisition. For borrowers, improved accuracy cam reduce the likelihood that creditworthy individuals are unfairly denied loans. 

## Proposed Data Science Solution

The objective of this project is to develop a robust model capable of accurately predicting loan defaults. The machine learning techniques being considered include Logistic Regression, Decision Trees, Random Forests and Support Vector Machines (SVM). The dataset contains 17 features excluding the target, however, following data pre-processing (one-hot encoding) and feature engineering (creating new features based on interactions between existing features), there will be many additional features. As a result, it will be important to consider these ML techniques and their suitability for different aspects of the problem at hand. 

## The Impact and Business Value

Accurate loan default predictions can lead to substantial savings for financial lending institutions. According to data published by Statista, as of Q2 2023, approximately 2.36% of all consumer loans at commercial banks in the United States were reported as delinquent. The project's aim, even by a modest margin, could translate to billions of dollars in savings, given the vast sums involved in lending. A simplistic approach to quantifying an rough estimate of the impact of this improved accuracy can be done by calculating 2.36% (delinquency rate in 2023) of $17 trillion (Fed reported total consumer debt in 2023) which is approx. $400 billion. A mere 1% improvement in prediction accuracy could result in approx. $4 billion in savings which is significant. 

## Description of the Dataset

The dataset was obtained from Kaggle and the original source is a challenge hosted by Coursera where it is defined as a 'real world dataset' without revealing the actual company or specifics surrounding where the data originated. It encapsulates details of individuals who have taken out loans. Features emcompass demographics, financial particulars and loan specifics. The target variable is `Defaut`. 

`LoanID`: 'Unique identifier for the loan.'
`Age`: 'Age of the borrower.'
`Income`: 'Income of the borrower.'
`LoanAmount`: 'Amount of loan taken.'
`CreditScore`: 'Borrower's credit score.'
`MonthsEmployed`: 'Duration (in months) the borrower has been employed.'
`NumCreditLines`: 'Number of credit lines the borrower has.'
`InterestRate`: 'Interest rate of the loan.'
`LoanTerm`: 'Term of the loan in months.'
`DTIRatio`: 'Debt-to-Income ratio.'
`Education`: 'Education level of the borrower.'
`EmploymentType`: 'Type of employment (e.g., Full-time, Part-time).'
`MaritalStatus`: 'Marital status of the borrower.'
`HasMortgage`: 'Whether the borrower has a mortgage.'
`HasDependents`: 'Whether the borrower has dependents.'
`LoanPurpose`: 'Purpose for which the loan was taken.'
`HasCoSigner`: 'Whether there is a co-signer for the loan.'
`Default`: 'Whether the loan defaulted (1 for Yes, 0 for No).'

## EDA Findings

1) Data Imbalance: A significant imbalance was observed in the target variable, with a much larger proportion of loans not defaulting compared to those that did. This imbalance has implications for modeling and evaluation strategies
2) Initial Hypotheses: Preliminary analysis suggested potential relationships between borrower characteristics and loan default likelihood. For example, factors like education level, employment level and income appeared to influence the likelihood of a loan default, showing a slight correlation with lower default rates. It must be noted, however, that these correlation figures were very low.
3) Key Insights: The EDA highlighted the need for careful feature engineering and data preprocessing, especially in attempting to address the data imbalance of the target variable and also attempting to add some more complexity to the model.

## Baseline Modeling Efforts

1) Model Selection: Logistic Regression and Decision Tree models were utilized as the baseline models to predict loan defaults
2) Performance Evaluation: Both models demonstrated varying levels of accuracy and precision. The Logistic Regression model showed high overall accuracy (89%), but struggled with extremely low recall (5%) for the default class. The Decision Tree provided a slightly more balanced performance across classes but with lower accuracy (80%) and precision (19% for defaults).
3) Challenges: The initial models highlight the challenges presented by imbalanced datasets. This necessitates a deeper exploration of advanced modeling techniques, including handling imbalanced data, model tuning and more sophisticated feature engineering. 
