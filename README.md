Project Objectives
Primary Goal

Develop an enterprise-grade credit risk system capable of:

Predicting borrower default risk
Generating explainable lending decisions
Optimizing credit limits
Evaluating portfolio resilience under economic stress
Business Questions Addressed
Which customers are most likely to default?
How should interest rates vary by risk?
How much capital should be allocated to each customer?
How do macroeconomic shocks affect portfolio risk?
How can credit limits be optimized while controlling risk?
Dataset

This project uses the Give Me Some Credit dataset from Kaggle.

Dataset:

Training file: cs-training.csv
Target variable: SeriousDlqin2yrs

The implementation validates the official dataset structure before use and falls back to synthetic data if a valid dataset is unavailable.

Features
RevolvingUtilizationOfUnsecuredLines
age
NumberOfTime30-59DaysPastDueNotWorse
DebtRatio
MonthlyIncome
NumberOfOpenCreditLinesAndLoans
NumberOfTimes90DaysLate
NumberRealEstateLoansOrLines
NumberOfTime60-89DaysPastDueNotWorse
NumberOfDependents

The project uses an 80/20 train-test split, producing approximately 120,000 training records and 30,000 testing records.

Technologies Used
Programming
Python
Data Science
NumPy
Pandas
Machine Learning
Scikit-Learn
Optuna Hyperparameter Optimization
Explainable AI
LIME
Visualization
Matplotlib
Seaborn
Risk Analytics
Probability of Default (PD)
Risk-Based Pricing
Economic Stress Testing
Credit Line Optimization
Implementation Approach
1. Data Preparation
Dataset validation
Missing value treatment
Feature preprocessing
Standardization
Train-test split
2. Model Development

Multiple classical machine learning models are trained and tuned using Optuna for performance optimization.

3. Credit Risk Scoring

The selected model generates:

Default probabilities
Risk scores
Customer risk rankings
4. Explainable AI

LIME explanations provide local feature importance for individual predictions, enabling transparent lending decisions.

5. Risk-Based Pricing Engine

The platform converts risk estimates into differentiated loan pricing and credit grades. A dedicated Risk-Based Loan Pricing Engine is included.

6. Capital Allocation

Predicted risk metrics are translated into capital requirements and portfolio management metrics.

7. Stress Testing

The platform evaluates portfolio performance under multiple economic scenarios including:

Mild recession
Moderate recession
Severe recession

Stress scenarios modify macroeconomic assumptions and recalculate portfolio risk.

8. Credit Line Optimization

An Enhanced Credit Line Optimization Engine determines customer-specific limits using:

Probability of Default
Income scaling
Expected profitability
Safety constraints

Credit limits are automatically capped within predefined ranges.

Key Features
Credit Risk Prediction

Predict borrower default probability using machine learning.

Explainable Decisions

Generate customer-level explanations using LIME.

Hyperparameter Optimization

Automated tuning with Optuna.

Fairness Evaluation

Assess potential bias across protected groups.

Stress Testing Framework

Simulate economic downturn scenarios.

Risk-Based Pricing

Assign pricing according to borrower risk.

Capital Management

Support enterprise risk and capital planning.

Credit Line Optimization

Generate risk-adjusted credit limits.


How to Run
1. Clone Repository
git clone https://github.com/yourusername/CREDENCE.git
cd CREDENCE
2. Install Dependencies
pip install -r requirements.txt
3. Download Dataset

Download the Give Me Some Credit dataset from Kaggle and place:

cs-training.csv

inside:

data/
4. Run Notebook
jupyter notebook

Open:

CREDENCE.ipynb

and execute all cells.

Outputs

The project generates:

Risk scores
Default probabilities
Explainability reports
Pricing recommendations
Capital allocation tables
Stress testing results
Credit decision reports
Optimized credit limits

Example outputs include:

credit_decisions_with_capital.csv
enhanced_credit_line_optimization.csv
Future Enhancements
Deep learning credit models
Real-time API deployment
Model monitoring dashboards
Drift detection
IFRS 9 Expected Credit Loss (ECL)
Basel III/IV capital integration
MLOps pipeline deployment


