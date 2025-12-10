# Customer Segmentation using Unsupervised Learning (Mall + Online Retail II)

This project implements unsupervised learning–based customer segmentation on two retail business datasets.  
It includes clustering, dimensionality reduction, persona profiling, and an interactive dashboard for stakeholder use.

---

## Project Overview

Customer segmentation helps businesses understand user behavior, personalize marketing, and improve revenue.  
This project focuses on:

| Dataset | Description | Feature Strategy |
|--------|-------------|-----------------|
| Mall Customers | Demographic and spending data | K-Means + UMAP |
| Online Retail II | Historical e-commerce invoices | RFM (Recency, Frequency, Monetary) + K-Means + UMAP |

---

## Methodology

### Mall Dataset
- Selected features: Age, Annual Income, Spending Score, Gender
- Standardized data using `StandardScaler`
- Dimensionality reduction using UMAP
- Clustering using **K-Means (k = 10)**
- Persona interpretation based on cluster profiles

### Online Retail II Dataset
- Derived RFM metrics:
  - Recency (days since last purchase)
  - Frequency (number of purchases)
  - Monetary (total transaction amount)
- Standard scaling and UMAP projection
- K-Means clustering (k = 10)
- Persona mapping for business insights

---

## Evaluation Metrics

| Dataset | Silhouette Score ↑ | Davies-Bouldin ↓ | Interpretation |
|--------|------------------|----------------|---------------|
| Mall Customers | 0.4207 | 0.8331 | Good separation and structure |
| Online Retail II | 0.4525 | 0.6859 | Better compactness and separation |

---

## Key Business Insights

### Mall Segmentation
Customer groups like:
- High Income Low Spending
- Young High Spenders
- Loyal Moderate Spenders
- Older Low Spending
- Budget Conscious

Use cases:
- Tailored promotions
- Targeted retention campaigns
- Store layout optimization

### Online Retail II Segmentation (RFM)
Personas include:
- Premium / VIP Spenders
- Loyal High Spenders
- Potential Loyalists
- Regular Budget Buyers
- Low Value Customers
- Churn Risk and Lost Customers

Use cases:
- Churn recovery offers
- Loyalty programs for high-value users
- Upselling to regular buyers

---

## Interactive Gradio Dashboard

Features:
- Two datasets integrated into separate tabs
- Customer lookup using CustomerID
- Persona and cluster details displayed
- UMAP visualization of cluster separation

This enables business teams to dynamically explore and validate clusters.

---

## Tools and Technologies

| Category | Tools |
|--------|------|
| Programming | Python |
| ML + Analytics | scikit-learn, UMAP |
| Visualization | Matplotlib, Seaborn |
