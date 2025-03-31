# 🛠️ Step 3: Feature Engineering & Modeling

## 🔍 Objective
Feature engineering is a crucial step in building an effective churn prediction model. It involves transforming raw data into meaningful features that enhance the model's predictive power. Once the features are engineered, we proceed with model selection, training, and evaluation.

## 📂 Feature Engineering
### 1️⃣ Handling Missing Values
- Impute missing values in numerical columns using median or mean.
- Fill missing categorical values with the most frequent category.

### 2️⃣ Encoding Categorical Variables
- Convert categorical features (e.g., **Industry**, **Tariff Type**) into numerical format using **One-Hot Encoding** or **Label Encoding**.

### 3️⃣ Creating New Features
- **Price Sensitivity Score**: Compute percentage price change over time to capture how customers respond to pricing fluctuations.
- **Contract Age**: Calculate the duration a customer has been with PowerCo.
- **Usage Patterns**: Identify seasonal trends in energy consumption.
- **Billing Variability**: Measure fluctuations in monthly billing amounts.

### 4️⃣ Feature Scaling
- Apply **Standardization** (Z-score normalization) or **Min-Max Scaling** for numerical features to ensure uniform scale across all variables.

## 📊 Model Selection
### 1️⃣ Choosing a Model
We experiment with multiple classification models to predict churn:
- **Logistic Regression** – Simple, interpretable model for baseline comparison.
- **Random Forest** – Handles non-linearity and provides feature importance.
- **Gradient Boosting (XGBoost, LightGBM, CatBoost)** – Effective for structured data with strong predictive power.

### 2️⃣ Model Training & Evaluation
- Split data into **train (80%)** and **test (20%)** sets.
- Use **Cross-Validation (k-fold)** to ensure robustness.
- Evaluate performance using:
  - **Accuracy** – Overall correctness of predictions.
  - **Precision & Recall** – Measure model effectiveness in identifying churned customers.
  - **ROC-AUC Score** – Indicates how well the model differentiates between churned and retained customers.

## 🎯 Key Insights
- Feature selection based on **importance scores** helps in improving model performance.
- **Gradient Boosting models (XGBoost, LightGBM)** outperform simpler models due to their ability to capture complex relationships.
- Price fluctuations and contract duration play a significant role in predicting churn.

## 📌 Next Steps
Proceed to **[Step 4: Findings & Recommendations](./step4_findings_recommendations.md)** to derive actionable insights from the model results.

