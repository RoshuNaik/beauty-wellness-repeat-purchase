# Candidate Data Dictionary

Final variables depend on the selected dataset. These are candidate fields.

| Variable | Meaning | Potential use |
|---|---|---|
| Customer ID | Pseudonymous identifier for each customer | Group transactions by customer |
| Purchase date | Date of each transaction | Calculate purchase intervals and observation windows |
| Order amount | Total amount paid for an order | Summarise spending and compare groups |
| Product category | Skincare, makeup, haircare, etc., if recorded | Compare patterns across categories |
| Purchase frequency | Number of orders in a past period | Candidate predictor |
| Days since last purchase | Time between last observed purchase and prediction date | Candidate predictor |
| Repeat purchase outcome | Whether another purchase occurs in a specified future period | Possible target variable |
| Promotion exposure | Whether a customer received an offer, if recorded | Explore campaign relationships, with care |
