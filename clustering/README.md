# Customer Segmentation Using RFM & K-Means

This project segments customers based on purchasing behavior using **RFM metrics** (Recency, Frequency, Monetary) and **K-Means clustering**.  
RFM alone gives broad categories, but machine learning uncovers deeper, more actionable customer groups.

---

## 1. Problem Statement
Marketing efforts were generic and low-impact because all customers were treated the same.  
Goal: create **data-driven segments** to enable targeted campaigns, improve retention, and increase customer lifetime value.

---

## 2. Data & Features
From transaction data, the following RFM features were engineered:

- **Recency**: Days since last purchase  
- **Frequency**: Total number of transactions  
- **Monetary**: Total spending value  

Data preprocessing steps:
- Outlier handling  
- `log1p` transformation for skewed variables  
- Feature scaling using StandardScaler  

---

## 3. Methodology
1. Compute RFM metrics per customer  
2. Explore distributions and correlations  
3. Apply transformations and scaling  
4. Run K-Means for k = 2–8  
5. Use **Elbow method** + **Silhouette score** to select optimal k  
6. Train K-Means  
7. Profile clusters using median R/F/M and business indicators  
8. Assign business meaning to each segment  

---

## 4. Why K-Means Is Better Than RFM Alone
- **RFM** uses fixed rules → creates broad, rigid buckets  
- **K-Means** finds natural patterns in customer behavior  
- ML reveals differences that RFM cannot separate, such as:
  - high-value but low-recency customers  
  - recent medium spenders  
  - dormant but historically valuable customers  
  - growth-potential users  

Machine-learning segmentation = **more precise**, **more actionable**, and aligned with KPIs.

---

## 5. Cluster Summary (Example)
- **Cluster 2 — Reward**: High-value, loyal customers → VIP perks  
- **Cluster 1 — Nurture**: Recently active, mid-value → cross-sell  
- **Cluster 0 — Re-engage**: Dormant customers → win-back campaigns  
- **Cluster 3 — Growth Potential**: Moderate spenders → upsell & frequency boosters  

> RFM alone could not cleanly separate these groups — K-Means did.

---

## 6. Recommendations
- Reward high-value segments (Cluster 2) with early access and exclusive offers  
- Nurture mid-value recent users (Cluster 1) through product/tier incentives  
- Re-engage dormant customers (Cluster 0) via targeted win-back promotions  
- Invest in customers with growth potential (Cluster 3) using frequency-boosters  

Campaigns should be validated with A/B tests and tracked using:
- Repeat purchase rate  
- AOV (Average Order Value)  
- Retention metrics  
- Incremental revenue  

---

## 7. Tools & Libraries
- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib / Seaborn  
- Jupyter Notebook  

---

## 8. Next Steps (Improvements)
- Add product-level and channel-level features  
- Test alternative clustering models (GMM, HDBSCAN)  
- Build automated segmentation pipeline  
- Add Streamlit or PowerBI dashboard  
- Validate segments over multiple time windows  

---

## 9. Impact Statement
This project transforms raw transaction data into **operational customer segments** that enable targeted campaigns and measurable improvements in retention and revenue.

