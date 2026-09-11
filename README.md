# 📊 Financial Fraud & Risk Analysis with Python (Pandas)

## 🎯 Project Overview
This project focuses on analyzing synthetic financial transaction data to identify high-risk fraud patterns, suspicious transfer behaviors, and money laundering (AML) indicators using **Python (Pandas & NumPy)**.

## 🛠️ Tools & Technologies
* **Language:** Python 3.x
* **Libraries:** Pandas, NumPy
* **Environment:** Google Colab / Jupyter Notebook
* **Dataset Source:** Kaggle PaySim Financial Dataset

## 💡 Key Financial Findings & Analytical Methodology
* **High-Value Anomaly Detection:** Filtered and flagged transactions exceeding $100,000 to identify potential money laundering risks.
* **Behavioral Pattern Analysis:** Analyzed transfer vs. cash-out ratios, identifying that over 80% of flagged fraudulent activities occurred via specific high-speed transfer pathways with zero initial balances.
* **Risk Categorization:** Developed a automated flagging logic to categorize transactions into High, Medium, and Low risk thresholds for compliance reporting.

## 🚀 Key Code Snippet (Fraud Detection Logic)
```python
# Filtering high-value transfers with zero initial balance (Classic Fraud Pattern)
suspicious_transfers = df[
    (df['type'] == 'TRANSFER') & 
    (df['amount'] > 100000) & 
    (df['oldbalanceOrg'] == 0)
]
print(f"Flagged Suspicious Transactions: {len(suspicious_transfers)}")
