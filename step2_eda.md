# 📊 Step 2: Exploratory Data Analysis (EDA)

## 🔍 Objective
The goal of Exploratory Data Analysis (EDA) is to understand the structure of the dataset, identify patterns, and detect potential issues such as missing values or outliers. This helps us derive meaningful insights before proceeding to feature engineering and modeling.

## 📂 Dataset Overview
We analyze the PowerCo dataset, which includes customer details, pricing history, and churn information. The key attributes include:

- **Customer ID**: Unique identifier for each customer
- **Industry**: The sector in which the customer operates
- **Contract Duration**: Length of time the customer has been with PowerCo
- **Electricity & Gas Consumption**: Usage data over time
- **Churn Status**: Whether the customer has left PowerCo
- **Price Data**: Historical pricing for each customer

## 📌 Steps in EDA
### 1️⃣ Data Cleaning
- **Handling Missing Values**: Identify and address missing data in key variables.
- **Duplicate Removal**: Ensure each record is unique.
- **Data Type Consistency**: Convert categorical and numerical fields to appropriate formats.

### 2️⃣ Univariate Analysis
- **Distribution of Numerical Features**: Use histograms and box plots to examine customer consumption and contract duration.
- **Categorical Feature Analysis**: Use bar charts to visualize industry types and churn rates across sectors.

### 3️⃣ Bivariate Analysis
- **Churn vs. Price Sensitivity**: Analyze the relationship between price changes and churn rates.
- **Churn vs. Contract Duration**: Determine if longer contracts lead to lower churn.
- **Churn vs. Industry**: Identify high-risk industries with elevated churn rates.

### 4️⃣ Correlation Analysis
- Compute the correlation matrix to understand relationships between numerical features.
- Use a heatmap to visualize strong and weak correlations.

### 5️⃣ Data Visualization
- **Boxplots & Violin Plots**: Show distribution of energy consumption across churned and retained customers.
- **Histograms**: Display frequency distributions of contract length and pricing.
- **Scatter Plots**: Explore relationships between price fluctuations and customer retention.

## 🎯 Key Findings
- Customers with higher **price sensitivity** exhibit a higher likelihood of churn.
- Certain **industries have higher churn rates** due to competitive energy pricing.
- **Longer contract durations** are correlated with lower churn rates.
- High variability in **electricity and gas prices** could be influencing customer decisions.

## 📌 Next Steps
Proceed to **[Step 3: Feature Engineering & Modeling](./step3_feature_engineering_modeling.md)** to refine data and build predictive models.

