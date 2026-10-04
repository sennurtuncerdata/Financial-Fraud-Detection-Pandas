# Financial Fraud & Risk Analysis with Python (Pandas)

This project focuses on automated Anti-Money Laundering (AML) transaction monitoring scenarios using Python and Pandas.

## Tools & Technologies
- **Language:** Python 3.x
- **Libraries:** Pandas
- **Environment:** Google Colab / Jupyter Notebook
- **Dataset:** AML Bank Transactions Dataset (`aml_bank_transactions.csv`)

## Key Financial Findings & Analytical Methodology
- **High-Value Threshold Detection:** Filtered and flagged transactions exceeding $5,000 to identify potential high-risk activities.
- **Money Mule Account Analysis:** Aggregated transaction counts and volumes per sender to flag accounts acting as potential money mules.
- **High-Volume Receiver Identification:** Identified recipient accounts receiving disproportionate transaction volumes (Structuring / Smurfing risks).
- **Transaction Type Risk Breakdown:** Analyzed risk distribution across different transaction types (Transfer, Withdrawal, Deposit).

## Key Code Snippet (AML Monitoring Logic)
```python
# Filtering successful high-value transactions (> $5,000)
high_risk_txns = df[(df['Transaction_Amount'] > 5000) & (df['Status'] == 'Success')]
print(f"Flagged High-Risk Transactions: {len(high_risk_txns)}")
