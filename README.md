# Group-3_DSEB64B
# 📊 Credit Risk Prediction Project

## 📝 Overview
This project was developed as the final assignment for the course *Data Preparation and Visualization* at National Economics University (NEU), Vietnam.

We aim to build a reliable and interpretable credit risk prediction model using **Logistic Regression** to assess the likelihood that a customer will default on their loan, based on a comprehensive financial dataset from Home Credit.

## 🎯 Objectives
- Clean, preprocess, and engineer features from multiple relational datasets.
- Build a predictive model to classify credit applicants as either low-risk (good credit) or high-risk (potential default).
- Optimize model performance using AUC-ROC as the evaluation metric.

## 👨‍💻 Team Members
- Nguyễn Đức Anh - 11220322
- Nguyễn Mạnh Dũng - 11221492
- Nguyễn Khánh Toàn - 11226276
- Nguyễn Tiến Tuấn Thành - 11225815
- Chu Cao Nguyên - 11219281

## 📂 Dataset
The dataset includes information from Home Credit such as:
- `application.csv`: Main application data
- `bureau.csv`: Credit history from other institutions
- `bureau_balance.csv`: Monthly credit balance status
- `credit_card_balance.csv`: Monthly credit card data
- `POS_CASH_balance.csv`: Point of Sales loan balances
- `previous_application.csv`: Previous loan application details
- `installments_payments.csv`: Payment history

## 🔍 Exploratory Data Analysis (EDA)
Key findings:
- 91% of applicants were not in default.
- Female applicants applied twice as much as males, but males defaulted at a higher rate.
- Married applicants dominated the sample, but civil marriage showed the highest default rate (9.9%).

## 🧹 Data Cleaning
- Replaced invalid date values (e.g., > 1000 years) with `NaN`.
- Converted invalid categorical values (`'XNA'`, `'Unknown'`) to `NaN`.
- Removed features with more than 80% missing values.
- Retained other features and applied imputation.

## ⚙️ Preprocessing
- **Imputation**: Median for numerical values; mode for categorical values.
- **Encoding**: Label Encoding (binary features) and One-Hot Encoding (multi-class).
- **Special Encodings**: Encoded weekday and education level with domain-specific mappings.

## 🧠 Model Building
**Algorithm**: Logistic Regression (selected over Decision Tree due to better performance and interpretability in this context)

### Parameters:
- `max_iter=1000`: Increased to ensure convergence
- `solver='liblinear'`: Suitable for smaller datasets and allows regularization

### Performance:
- Metric: AUC-ROC
- Final AUC: **0.55** (improved from baseline 0.50)

## 🧪 Feature Engineering
- Created **polynomial features** to capture non-linear relationships.
- Engineered **domain-specific features** using aggregation (sum, min, max, mean, count) from related tables.

## 📈 Result
While the project uses basic models (Logistic Regression), through careful **data cleaning, feature engineering**, and **preprocessing**, the team was able to improve prediction capability (AUC 0.55) and provide interpretability for credit decision-making.

## 📎 Tools & Technologies
- Python (Pandas, NumPy, Scikit-learn)
- Jupyter Notebook
- Git & GitHub

## 📚 Report
Detailed methodology and analysis are available in the final report: [Group3_DSEB64B_Report.pdf](./Group3_DSEB64B_Report.pdf)

