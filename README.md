# AI Market Copilot — AI for Market Trend Analysis (Capstone Project)

🚀 **Live Streamlit Dashboard:**  
https://saibharadwaja-ai-marketcopilot-retail-trend.streamlit.app/

📌 **Streamlit Deployment Repository (App Source Code):**  
https://github.com/SaiBharadwaja-18/AI-MarketCopilot-Retail-Trend

---

## 1. Project Overview
This capstone project was developed under the **IIT Ropar Minor in AI** program as part of the module **"AI for Market Trend Analysis"**.

The goal of this project is to build an **AI-driven Market Trend Analysis + Decision Support system** using real-world e-commerce transaction data.  
The system supports:
- Market trend understanding via EDA
- AI-based revenue forecasting
- Business-ready decision support recommendations (stock/promotions)
- Customer segmentation using RFM + clustering

This project is designed to be **capstone-worthy + portfolio-worthy**, and showcases an end-to-end AI pipeline suitable for real-world retail demand planning and marketing analytics.

---

## 2. Selected Project Track
✅ Track: **AI in Market Trend Analysis**

---

## 3. Problem Statement & Objective

### Problem Statement
Online retail businesses face uncertainty in demand patterns due to seasonal variations, customer behavior changes, and sudden market spikes.  
Manual forecasting and decision making often results in:
- overstocking / understocking,
- missed marketing opportunities,
- inefficient customer retention strategies.

### Objective
To build an AI solution that:
1. Forecasts **future revenue trends**
2. Detects **growth and uncertainty (risk index)**
3. Suggests actionable decisions:
   - **STOCK UP + PROMOTE**
   - **NORMAL STOCK**
   - **REDUCE STOCK**
   - **HIGH RISK – Stock Carefully**
4. Segments customers into personas for business targeting.

---

## 4. Dataset Used

### Dataset Source
Dataset: **Online Retail Dataset (UCI / Kaggle version)**  
Type: Multivariate | Time-series | Sequential transaction data  
Period: **01-Dec-2010 to 09-Dec-2011**

### Columns
- `InvoiceNo`
- `StockCode`
- `Description`
- `Quantity`
- `InvoiceDate`
- `UnitPrice`
- `CustomerID`
- `Country`

---

## 5. Notebook (Main Source of Truth ✅)
As per submission guidelines, the **Jupyter Notebook (.ipynb)** is the main evaluation artifact.

This notebook contains:
1. Problem Definition & Objective  
2. Data Understanding & Preparation  
3. Model / System Design  
4. Core Implementation  
5. Evaluation & Analysis  
6. Ethical Considerations & Responsible AI  
7. Conclusion & Future Scope  

✅ Notebook runs end-to-end with **Markdown + Code cells**.

---

## 6. System / Pipeline Design

### 6.1 Data Preparation
- Removed duplicates
- Handled missing values (CustomerID, Description)
- Filtered invalid transactions (cancellations, negative revenue issues)
- Feature engineering:
  - `Revenue = Quantity × UnitPrice`
  - Date features: Year / Month / Day / DayOfWeek / Hour
  - Aggregations for daily & monthly trend analysis

### 6.2 Forecasting (Time-series AI)
AI Model Used: **XGBoost Regressor**  
Forecast Target: **Daily Revenue**

Feature set includes:
- Lag features: `lag_1`, `lag_7`, `lag_14`, `lag_28`
- Rolling statistics: rolling mean/std for 7/14/28 days
- Calendar features: day of week, month, weekend flag

Evaluation Metrics:
- MAE
- RMSE
- R² Score
- MAPE

### 6.3 Decision Support Layer (Unique Innovation)
After forecasting, a business decision engine is created:
- Growth % estimation
- Volatility measure
- Risk index from uncertainty

Final output recommendations:
- ✅ STOCK UP + PROMOTE
- ✅ NORMAL STOCK
- ✅ REDUCE STOCK
- ⚠️ HIGH RISK — Stock Carefully

This converts raw forecasting into **actionable market strategy**, making the project more industry-aligned.

### 6.4 Customer Segmentation
Method: **RFM Analysis + KMeans clustering**
- Recency
- Frequency
- Monetary

Personas generated:
- **VIP Champions**
- **Loyal Customers**
- **Regular Customers**
- **Lost / At-Risk**

Each segment has recommended business strategies.

---

## 7. Streamlit Dashboard (Deployment)
A professional dashboard was created and deployed using Streamlit Community Cloud.

✅ Live App:  
https://saibharadwaja-ai-marketcopilot-retail-trend.streamlit.app/

✅ App Repository:  
https://github.com/SaiBharadwaja-18/AI-MarketCopilot-Retail-Trend

The dashboard contains:
- KPI cards (rows, unique customers, countries, etc.)
- EDA graphs
- Forecasting visualization
- Decision support recommendations
- Customer segmentation insights

---

## 8. Ethical Considerations & Responsible AI
- Dataset contains geographic bias (majority transactions from United Kingdom)
- Model recommendations are **decision-support**, not guaranteed business outcomes
- Should not be used for financial/critical automation without expert validation
- Model performance impacted by real-world spikes and abnormal seasonal patterns

---

## 9. Conclusion
This project demonstrates a complete AI workflow:
- Preprocessing + EDA
- Time-series ML forecasting using XGBoost
- Decision support system with risk handling
- Customer segmentation into personas
- Deployment with Streamlit

---

## 10. Future Scope
- Add external features: promotions, holidays, macroeconomic signals
- Product-category level forecasting
- Automated alerting for sudden demand spikes
- Advanced time-series models (LSTM/Transformer)
- Recommendation system integration (cross-sell / upsell)

---

## Author
**Ummethala Venkata Datha Sai Bharadwaja**  
B.Tech CSE (AI & ML) | SRM University  
IIT Ropar Minor in AI — Capstone Project
