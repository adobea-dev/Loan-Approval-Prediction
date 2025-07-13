# Loan-Approval-Prediction

Overview
Meet Kofi — an entrepreneur who needs urgent capital to grow his business. He walks into a bank, uncertain if he'll be approved for a loan. Traditionally, he might wait days for a response.

But what if a machine learning model could analyze his data and provide an instant, accurate loan decision?

This project develops a loan approval prediction system that helps financial institutions make faster, data-driven decisions while improving customer experience.

Project Objective
To build a supervised machine learning model that predicts whether a loan should be approved (1) or not (0), based on customer information available at the time of application.

📁 Dataset
The dataset includes anonymized loan application records with features like:

Gender

Education

Home ownership

Loan purpose

Interest rate

Income and employment information

Credit history length

Debt-to-income ratio

✅ All features used are available at application time — no data leakage.

⚙️ Modeling Workflow
Data Cleaning

Removed post-loan features (like defaults) to prevent leakage

Handled missing values and outliers

Feature Engineering

Created ratios (e.g. loan amount vs income)

Applied log transformations

Preprocessing

Scaled numerical data

One-hot encoded categorical variables

Handled Class Imbalance

Used SMOTENC to oversample minority class while preserving categorical variables

Model Training & Evaluation

Trained Decision Tree, Random Forest, XGBoost, and LightGBM

Selected the best-performing model based on test accuracy, precision, recall, and F1-score

🧠 Best Performing Model: XGBoost
Metric	Value
Accuracy	91.12%
Precision (Approved Loans)	87.1%
Recall (Approved Loans)	70.5%
Precision (Rejections)	92.0%
Recall (Rejections)	97.0%

✅ High precision for approved loans means fewer false approvals.
🔁 Recall can be improved with threshold tuning or retraining with more diverse data.

📌 Key Drivers (Top Features)
SHAP analysis revealed that the model’s predictions were heavily influenced by:

Debt to income ratio

Home ownership rent

Interest rate 

Income

Credit history

Experience 

Loan amount

These insights help explain why the model approves or denies a loan — making it more trustworthy and transparent for business stakeholders.

🖥️ Tech Stack
Python (pandas, scikit-learn, XGBoost, LightGBM)

imbalanced-learn (SMOTENC)

SHAP for model interpretability

Matplotlib & Seaborn for visualization


