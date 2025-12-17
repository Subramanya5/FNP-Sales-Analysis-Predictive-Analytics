#  FNP Sales Analysis & Predictive Analytics Project

##  Project Overview
This project presents an **end-to-end sales analysis for FNP (Flowers & Gifts)**, a business characterized by **occasion-driven demand, seasonal revenue spikes, and time-sensitive deliveries**.

The goal is to move beyond descriptive reporting and build a **data-driven decision framework** using:
- **Excel** for dashboarding and business understanding  
- **MySQL** for data engineering and feature creation  
- **Python** for statistical analysis and machine learning  

This project is designed to reflect **real FNP business challenges**, not generic retail analysis.

---

## 🎯 Business Context (Why FNP Is Unique)
FNP operates in a domain where:
- Purchases are **emotion-driven**
- Demand spikes during **occasions** (Valentine’s Day, Birthdays, Anniversaries)
- **Delivery timing** directly impacts customer satisfaction
- A small subset of customers contributes a large share of revenue  

Ignoring these factors would make any analysis incomplete.

---

##  Data Sources
The analysis is built on three primary datasets:

### *Orders*
- Order & delivery dates and times  
- Quantity, price, revenue  
- Location, occasion, delivery delay  

### *Products*
- Product category  
- Price  
- Occasion relevance  

### *Customers*
- Customer identifiers  
- Location and demographic attributes  
- Purchase behavior  

### *Engineered Features*
- Revenue per order  
- Delivery delay (in days)  
- Month, hour, and delivery day  

---

##  Phase 1 — Excel Dashboard (Business Understanding)

### Objective
To understand **historical performance and patterns**.

### Key Insights
- Sales are highly volatile, not stable
- Strong revenue spikes during key occasions
- Certain locations consistently show higher delivery delays
- A few products and customers drive most revenue  

This phase helped identify **which business problems are worth modeling**.

---

## Phase 2 — SQL Analysis (Data Engineering)

### Objective
To create **clean, structured, ML-ready datasets**.

### Key SQL Outputs
- Daily sales aggregation for forecasting
- Product-level demand summaries
- Customer-level behavioral metrics
- Delivery performance metrics by location and time  

Temporary and calculated fields were intentionally created to reflect **real operational KPIs**.

---

## Phase 3 — Python Analytics & Machine Learning

The Python phase is organized into **four focused notebooks**, each answering a specific FNP business question.

---

## Sales Forecasting (Strategic Planning)

### Business Question
*How will FNP’s sales behave in the near future?*

### Methods Used
- Time-series visualization  
- Augmented Dickey–Fuller (ADF) test  
- ARIMA forecasting  
- Residual diagnostics  

### Key Insight
Sales show **non-stationarity and sharp occasion-driven spikes**.  
Forecasts capture long-term trends but underestimate extreme peaks.

### FNP-Specific Conclusion
Sales forecasts must be **adjusted for major occasions**; historical averages are unreliable for FNP.

---

## Product Demand Prediction (Inventory Planning)

### Business Question
*Which products should FNP stock more of before key occasions?*

### Methods Used
- Descriptive statistics  
- Pearson correlation (price vs demand)  
- Random Forest regression  
- Feature importance analysis  

### Key Insight
- Past demand is the strongest predictor  
- Occasion and seasonality amplify demand  
- Price has a statistically significant negative impact on demand  

### FNP-Specific Conclusion
Inventory planning should be **demand-led and occasion-aware**, not static.

---

## Customer Segmentation (Marketing Strategy)

### Business Question
*Who are FNP’s most valuable customers?*

### Methods Used
- Behavioral feature engineering  
- Standardization  
- Elbow method  
- K-Means clustering  

### Customer Segments Identified
- **High-value occasion buyers** – high spend, moderate frequency  
- **Regular buyers** – steady and predictable revenue  
- **Low-value buyers** – price-sensitive and infrequent  

### FNP-Specific Conclusion
Retention strategies should prioritize **high-value occasion buyers**, while promotions can upgrade mid-tier customers.

---

## Delivery Time Prediction (Operational Excellence)

### Business Question
*What causes delivery delays, and can we predict them?*

### Methods Used
- Distribution analysis  
- ANOVA hypothesis testing (location impact)  
- Gradient Boosting regression  
- Feature importance analysis  

### Key Insight
Delivery delays are **systematic**, driven by:
- Location  
- Order size  
- Time of order  
- Peak occasions  

### FNP-Specific Conclusion
Operational improvements should focus on **high-risk locations and peak periods**, not uniform changes.

---

## 🔗 Cross-Model Insights

| Area | Insight |
|-----|--------|
| Sales | Predictable trends with volatile occasion spikes |
| Products | Demand driven by history and context |
| Customers | Revenue concentrated in a few segments |
| Delivery | Delays are operational, not random |

Together, these insights form a **cohesive decision framework for FNP**.

---

## 💡 Final Business Recommendations for FNP
- Increase inventory **2–3 weeks before major occasions**
- Prioritize logistics capacity in delay-prone locations
- Use sales forecasts for
