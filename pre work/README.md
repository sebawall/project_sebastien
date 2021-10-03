# project_sebastien

# structure

* Build the fraud analyst engine.
* Train the system with the scenario 1

* Then process a one year tx history and see how fast the system adapt

* See how fast new trend is detected


# ML training

* Step 1 : Take a sample of transaction and train the system with a single scenario
* Step 2 : List each different items and define a correlation coef with is fraud


# Engine

* Step 1 : Pick transaction in chronological order
* Step 2 : Compare transaction détails with account profile,  and observe each gap * risk ratio
* Step 3 : Check similarity with fraud trend
* Step 4 : Attribute/update risk score to account
* Step 5 : Take decision (pass, review, deny) if deny orange flag for transaction and account


# ML
* Step 1 : Pick transaction in chronological order (try to process with some delay from engine), if fraud pass
* Step 2 : If fraud, red flag account and orange terminal(if terminal already orange flag so red)
* Step 3 : Define correlation between fraud and every transaction detail for last 5 /10 / 15 fraud and last month/ 2 month / 3 month
* Step 4 : Update ratio with corrected ratio (evaluate which periode is the most efficient (last 5 /10 / 15 fraud and last month/ 2 month / 3 month) or mean of this period
* Step 5 : If high correlation add tx to fraud trend dataset with fraud trend ref



flag coef = no flag = 1 / orange = 1.5 / red = 10


# Decision making

decision_score = ((risk_score_trx * flag_trx) + (risk_score_terminal * flag_terminal) + (risk_score_profile * flag_profile))/3


# Fraud trend
monitor fraud trend : when detected the system will tag tx with accurate fraud trend

# Human asction
red flag = manual review

# Perf review
* Evaluate the good decision score
* Monthly report to % tx and amount catch
* Efficiency of trend detection
* Decision accuracy (% false flag)

fraud trend score