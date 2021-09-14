# project_sebastien

# structure

Build the fraud analyst engine.
Train the system with the scenario 1

Then process a one year tx history and see how fast the system adapt

See how fast new trend is detected


# ML training

Step 1 : Take a sample of transaction and train the system with a single scenario
Step 2 : List each different items and define a correlation coef with is fraud


# Engine

Step 1 : Pick transaction in chronological order
Step 2 : Compare transaction détails with account profile,  and rate each gap * risk ratio
Step 3 : Check similarity with fraud trend
Step 4 : Attribute/update risk score to account
Step 5 : Take decision (pass, review, deny) if deny orange flag for transaction and account


# ML
Step 1 : Pick transaction if fraud pass
Step 2 : If fraud red flag account and orange terminal(if terminal already orange flag so red)
Step 3 : Define correlation between fraud and every transaction detail for last 5 /10 / 15 fraud and last month/ 2 month / 3 month
Step 4 : if high correlation 



flag system = no flag = 1 / orange = 1.5 / red = 10


# Decision making

decision_rate = ((risk_rate_trx * flag_trx) + (risk_rate_terminal * flag_terminal) + (risk_rate_profile * flag_profile))/3


# Fraud trend
monitor fraud trend : when detected the system will tag tx with accurate fraud trend

# Human tranasction
red flag = manual review


fraud trend score