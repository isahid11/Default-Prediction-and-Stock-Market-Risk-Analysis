Financial Default Prediction & Market Risk Analysis

📌 Business Context

This project builds a Financial Health Assessment Tool to help investors and financial institutions:
	•	Predict corporate financial default risk
	•	Identify key financial distress indicators
	•	Analyze stock market risk-return tradeoffs

The project consists of two parts:
	•	Part A: Corporate Default Prediction
	•	Part B: Stock Market Risk Analysis

⸻

PART A — Financial Default Prediction

🎯 Objective

Develop a machine learning model to predict whether a company will default based on projected net worth for the next year.

Default Definition:
	•	1 = Net worth next year is negative
	•	0 = Net worth next year is positive

Dataset:
	•	4,526 companies
	•	51 financial variables
	•	Default rate: 5.5% (highly imbalanced)

⸻

⚙ Methodology

Data Preprocessing
	•	IQR-based outlier treatment
	•	Label encoding for categorical variables
	•	Feature scaling (standardization)
	•	Multicollinearity reduction using VIF (removed features with VIF > 10)
	•	Stratified train-test split (80/20)
	•	Class imbalance handled using:
	•	Class weighting
	•	SMOTE

⸻

🤖 Models Built
	•	Logistic Regression
	•	Random Forest

Evaluation Metrics (Imbalanced dataset):
	•	Recall (priority metric)
	•	Precision
	•	F1-score
	•	ROC-AUC

⸻

📊 Final Model Performance

Logistic Regression (Optimized Threshold = 0.546)
	•	Accuracy: 89%
	•	Precision: 35%
	•	Recall: 92%
	•	F1-score: 0.51
	•	ROC-AUC: 0.89

Random Forest (Tuned)
	•	Accuracy: 95%
	•	Precision: 72%
	•	Recall: 49%
	•	F1-score: 0.56
	•	ROC-AUC: 0.94

⸻

🏆 Final Model Selected

Logistic Regression (optimized threshold)

Why?
	•	Highest recall (91.84%)
	•	Minimizes false negatives
	•	Better for financial risk management where missing a defaulter is costly

⸻

🔎 Key Financial Risk Drivers

Top predictors of default:
	1.	Cumulative Retained Profits
	2.	Total Capital
	3.	Adjusted EPS
	4.	PAT as % of Net Worth
	5.	Debt-to-Equity Ratio
	6.	Contingent Liabilities
	7.	Liquidity Ratios (Current Ratio, Cash-to-Liabilities)

Insight:

Companies with weak profitability, high leverage, and liquidity stress show higher default risk.

⸻

💡 Business Impact

This model enables:
	•	Early identification of high-risk companies
	•	Improved credit risk screening
	•	Data-driven lending decisions
	•	Risk-adjusted capital allocation

⸻

PART B — Stock Market Risk & Return Analysis

📈 Objective

Analyze risk-return characteristics of Indian stocks:
	•	ITC Limited
	•	Bharti Airtel
	•	Tata Motors
	•	DLF Limited
	•	Yes Bank

Using 418 trading days of historical price data.

⸻

📊 Methodology
	•	Calculated logarithmic returns
	•	Computed mean return and standard deviation
	•	Risk-return visualization (Mean vs Volatility plot)

⸻

🔎 Key Findings
	•	DLF Limited: Highest average return with moderate volatility
	•	ITC Limited: Stable returns, low volatility (conservative profile)
	•	Tata Motors: Moderate return, moderate volatility
	•	Bharti Airtel: Growth-oriented but volatile
	•	Yes Bank: Negative average return, highest volatility (high risk)

⸻

💡 Investment Strategy Recommendations
	•	Conservative Investors → ITC, DLF
	•	Growth Investors → Tata Motors, Bharti Airtel
	•	Speculative Investors → Yes Bank (high risk)

Portfolio diversification recommended for balanced risk-return profile.

⸻

🛠 Tools Used

Python
pandas, numpy
scikit-learn
matplotlib, seaborn
