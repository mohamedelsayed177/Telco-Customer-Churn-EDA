
# 📊 Telco Customer Churn – Exploratory Data Analysis (EDA)

## 🔹 Overview
This project explores the **Telco Customer Churn dataset**, which contains detailed information about telecom customers, including their **demographics, service usage, billing details, contract types, and churn status**.
The goal is to **analyze patterns, visualize trends, and extract insights** that can explain **why some customers leave** while others stay.

## 📂 Dataset
- **Rows:** 7043 (after cleaning: 7010)
- **Columns:** 21 (after preprocessing: 20)

### Key Features
| Feature | Type | Description |
|---------|------|-------------|
| `gender` | Categorical | Male / Female |
| `SeniorCitizen` | Categorical (0/1) | Whether the customer is a senior citizen |
| `Partner` | Categorical | Whether the customer has a partner |
| `Dependents` | Categorical | Whether the customer has dependents |
| `tenure` | Numerical | Number of months the customer has stayed |
| `PhoneService` | Categorical | Yes / No |
| `MultipleLines` | Categorical | Yes / No / No phone service |
| `InternetService` | Categorical | DSL / Fiber optic / No |
| `OnlineSecurity` | Categorical | Yes / No / No internet service |
| `TechSupport` | Categorical | Yes / No / No internet service |
| `StreamingTV` | Categorical | Yes / No / No internet service |
| `StreamingMovies` | Categorical | Yes / No / No internet service |
| `Contract` | Categorical | Month‑to‑month / One year / Two year |
| `PaperlessBilling` | Categorical | Yes / No |
| `PaymentMethod` | Categorical | Electronic check / Mailed check / Bank transfer (auto) / Credit card (auto) |
| `MonthlyCharges` | Numerical | Monthly billed amount |
| `TotalCharges` | Numerical | Total billed amount |
| `Churn` | Target | Yes / No |

**Dataset Source:** [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

## 🧹 Data Preprocessing
1. Removed irrelevant column: `customerID`.
2. Converted `TotalCharges` from object → float.
3. Filled missing values in `TotalCharges` with the mean (11 missing values).
4. Converted `SeniorCitizen` to categorical (0/1 → object).
5. Removed 22 duplicated rows.
6. Final dataset shape: **(7010, 20)**.

## 🔎 Exploratory Data Analysis (EDA)

### 1️⃣ Overall Churn
- ~26.45% of customers **churned**, 73.55% **remained subscribed**.
- Indicates a significant portion leaving, which can impact revenue.

### 2️⃣ Demographics & Churn
- **Gender:** Minimal effect on churn.
- **Senior Citizens:** Higher churn → older users may be less satisfied.
- **Dependents:** Customers without dependents churn more → single customers are more flexible in switching.

### 3️⃣ Charges & Spending Behavior
- **Monthly Charges:** Higher charges → higher churn.
- **Total Charges:** Lower for churned customers → they leave earlier.
- Suggests expensive plans discourage long‑term retention.

### 4️⃣ Internet & Additional Services
- **Fiber optic** users churn more than DSL.
- Lack of **OnlineSecurity** or **TechSupport** → higher churn.
- Entertainment services (StreamingTV/Movies) have little effect on retention.

### 5️⃣ Contract & Payment Methods
- **Month‑to‑month contracts** → highest churn.
- **Long‑term contracts** → lower churn → loyalty improves retention.
- **Electronic check** → higher churn; automatic payments → lower churn.

## 💡 Key Insights & Recommendations
1. **Focus retention strategies** on **senior citizens** and **customers without dependents**.
2. Introduce **loyalty programs** or **special offers** for high‑risk groups.
3. Encourage **automatic payments** and **longer‑term contracts** to reduce churn.
4. Improve **support‑related services** like **OnlineSecurity** and **TechSupport** to increase customer satisfaction.

## 🛠️ Libraries Used
- `pandas`, `numpy` – Data manipulation
- `matplotlib`, `seaborn` – Data visualization
- `warnings` – Ignore unnecessary warnings

## 📝 Notebook Structure
1. **About the Dataset** – Overview of features and target.
2. **Data Preprocessing** – Cleaning, missing values, type corrections.
3. **EDA** – Visualizations, pattern discovery, and analysis.
4. **Key Insights** – Summary of findings and actionable recommendations.
