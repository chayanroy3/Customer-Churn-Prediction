# 🎯 Step 1: Business Understanding & Hypothesis Framing

## 🔍 Business Problem
PowerCo, a major gas and electricity utility provider for small and medium-sized enterprises, is experiencing **customer churn**. With increased competition in the energy sector, customers now have more options than ever, making retention a challenge. PowerCo has engaged data scientists to diagnose the root causes of churn and recommend data-driven solutions.

## ⚡ Understanding Churn
**Churn** occurs when customers leave PowerCo to opt for a competitor’s services. The key question to investigate is:  
➡️ *What factors influence customer churn?*  
One primary hypothesis is that **price sensitivity** plays a significant role in customer retention.

## 📌 Key Hypothesis
We hypothesize that:
✅ Customers are highly **price-sensitive**, meaning an increase in pricing could result in higher churn rates.  
✅ Other factors such as **customer service quality, energy type (clean vs. non-clean), contract terms, and geographical location** might also contribute to churn.

## 📊 Required Data
To test our hypothesis, we need access to:
📂 **Customer Data** – Industry, historical electricity consumption, contract duration, date joined, and other customer characteristics.  
📂 **Churn Data** – Information on whether a customer has left PowerCo.  
📂 **Historical Price Data** – The prices charged for electricity and gas at different time intervals.  
📂 **Competitor Pricing Data** (if available) – To compare PowerCo’s pricing strategy with competitors.  

## Dataset Overview (Business Perspective)

To predict customer churn in an energy services company, we use two main datasets:

### 1. Client Data

This dataset contains detailed information about each client company, including:

- **Customer Profile & Activity**:  
  - Category of business activity (`activity_new`)  
  - Sales channel (`channel_sales`)  
  - Whether the client uses gas (`has_gas`)

- **Consumption History**:  
  - Electricity and gas consumption over the past 12 months (`cons_12m`, `cons_gas_12m`)  
  - Consumption from the last month (`cons_last_month`)

- **Contract Lifecycle**:  
  - Dates of activation, renewal, end of contract, and last modification  
    (`date_activ`, `date_renewal`, `date_end`, `date_modif_prod`)

- **Forecasts & Pricing**:  
  - Forecasted consumption and discount metrics (`forecast_cons_12m`, `forecast_cons_year`,  
    `forecast_discount_energy`)  
  - Forecasted prices and meter rent (`forecast_meter_rent_12m`, `forecast_price_energy_off_peak`,  
    `forecast_price_energy_peak`, `forecast_price_pow_off_peak`)

- **Financial Metrics**:  
  - Gross and net margins, total net margin, and number of active products  
    (`margin_gross_pow_ele`, `margin_net_pow_ele`, `net_margin`, `nb_prod_act`)

- **Customer Tenure**:  
  - Number of years the client has been with the company (`num_years_antig`)

- **Target Variable**:  
  - `churn`: whether the client is expected to leave in the next three months

*Note: Some fields (e.g., sales channel, campaign origin) are anonymized to preserve privacy,  
but may still hold predictive power.*

---

### 2. Price Data

This dataset provides historical pricing information, including:

- **Energy Prices**:  
  - Variable prices for off-peak, peak, and mid-peak energy usage  
    (`price_off_peak_var`, `price_peak_var`, `price_mid_peak_var`)

- **Power Prices**:  
  - Fixed prices for power in the same three time periods  
    (`price_off_peak_fix`, `price_peak_fix`, `price_mid_peak_fix`)

- **Keys**:  
  - Linked via `id` (client identifier) and `price_date` (date of pricing record)

These datasets together enable the development of a machine learning model to identify at-risk customers and guide retention strategies.


## 🛠️ Approach to Analysis
1️⃣ **Define Price Sensitivity** – Establish a metric to quantify how customer churn correlates with price changes.  
2️⃣ **Data Preparation & Feature Engineering** – Clean the data, handle missing values, and engineer relevant features.  
3️⃣ **Exploratory Data Analysis (EDA)** – Identify patterns in the data, visualize trends, and detect key correlations.  
4️⃣ **Modeling Churn Probability** – Use **binary classification models** like Logistic Regression, Random Forest, or Gradient Boosted Machines to predict churn probabilities.  
5️⃣ **Model Selection & Evaluation** – Compare different models based on accuracy, interpretability, and effectiveness in explaining churn.  

## 🎯 Expected Outcome
By completing this analysis, we aim to:
🚀 **Understand the key drivers of churn.**  
🚀 **Determine the extent to which price sensitivity influences customer retention.**  
🚀 **Provide actionable insights to PowerCo** to mitigate churn through pricing strategies and other retention initiatives.  

---
📌 **Next Step:** Proceed to **[Step 2: Exploratory Data Analysis](./step2_eda.md)** 🔍

