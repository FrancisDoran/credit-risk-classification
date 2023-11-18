# credit-risk-classification
Objective: The analysis aims to predict the likelihood of a loan being healthy or at risk.

Factors Considered: Key factors include loan size, interest rate, borrower's income, debt-to-income ratio, number of borrower's accounts, derogatory marks, total debt, and loan status.

Data Imbalance: The initial dataset had a significant imbalance with a much higher number of healthy loans compared to at-risk loans.

Methodology:

Data Preparation: Involved splitting the data into target and label variables and creating training and testing sets.
Model Training: A Logistic Regression model was used for training.
Model Evaluation: Performance was assessed using accuracy, precision, and recall metrics.

Model:
Accuracy: High (99%), but not fully reliable due to data imbalance.
Precision: 85%, indicating a lower false positive rate.
Recall: 88%, showing effectiveness in identifying high-risk loans.

I can't say whether I would or would not recommend the model to the company unless I knew how costly it was to missclassify, the value of the predicition can be arithmatically computed though:
let f1 be the frequency of risky loans, let f0 be the frequency of healthy loans, let p0 be the precision of predicting healthy loans, let p1 be the precision of predicting risky loans,
if f1((1-p0)(Value of giving a risky loan) + p1(Value of not giving a risky loan)) + f0((1-p1)(Value of not giving a healthly loan) + p0(Value of giving a healthy loan)) > 0, then the company should evaulate the opportunity cost and decide whether to use the model, as if better models exist, even if this model has a positive expected value, the company should opt for the models with higher expected value. Also of note is I used the value of not doing x, but the company could also choose to pursue risky loans but the princple of the calculation doesn't change as being correctly informed as to what type of loan they are pursue will let them make more profitable decision when pursuing a risky loan.
