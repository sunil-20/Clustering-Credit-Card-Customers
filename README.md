# Clustering Credit Card Customers (Unsupervised Machine Learning)

Customer segmentation project using **K-Means**, **DBSCAN**, and **Gaussian Mixture Models** to identify credit card customer clusters based on spending behavior, credit utilization, repayment patterns, and transaction characteristics.

---

## 1. Project Overview

As the U.S. economy recovers from the financial impacts of COVID-19, credit usage behaviors have shifted significantly. Financial institutions now face increased pressure to understand post‑pandemic consumer behavior and redesign personalized financial products.

This project applies **unsupervised machine learning** to segment **8,950 credit card customers** into meaningful groups to support:

- personalized marketing  
- risk assessment  
- credit limit optimization  
- customer retention strategies  
- targeted financial products  

Using real-world credit behavior data, the project identifies interpretable and business‑relevant clusters that a financial institution can use to improve decision-making.

---

## 2. Dataset

- **Observations:** 8,950 customers  
- **Features:** 18 behavioral and transactional variables  
- **Time span:** 6 months of credit card activity  
- **Source:** Kaggle Credit Card Dataset  
  https://www.kaggle.com/arjunbhasin2013/ccdata

### Data Dictionary (Summary)

- **BALANCE:** Remaining balance  
- **PURCHASES:** Total purchases  
- **ONEOFFPURCHASES:** Largest single purchase  
- **INSTALLMENTSPURCHASES:** Installment-based spending  
- **CASHADVANCE:** Cash withdrawn on credit  
- **PURCHASESFREQUENCY:** Purchase frequency score (0–1)  
- **CASHADVANCEFREQUENCY:** Cash advance frequency score  
- **PAYMENTS / MINIMUM_PAYMENTS:** Payment behavior  
- **CREDITLIMIT:** Individual credit limit  
- **PRCFULLPAYMENT:** Percent of full payments  
- **TENURE:** Customer tenure  

The dataset captures multiple dimensions of consumer spending, repayment habits, and credit utilization—ideal for clustering analysis.

---

## 3. Workflow Summary

### 3.1 Data Cleaning & Preprocessing
- Removed missing or inconsistent entries  
- Standardized numerical features using **StandardScaler**  
- Treated skewness and outliers (log transformation where appropriate)  
- Normalized high‑variance features  
- Removed non-informative columns (e.g., CUSTID)

### 3.2 Exploratory Data Analysis
- Distribution analysis of spending and repayment  
- Correlation heatmaps  
- Credit usage and payment‑behavior relationships  
- Identification of high‑variance features  
- Visualization of behavioral patterns across customers

### 3.3 Clustering Approach
Three clustering methods were used:

#### **K-Means**
- Baseline clustering method  
- Easy to interpret using cluster centroids  
- Number of clusters determined using:
  - Elbow Method  
  - Silhouette Score

#### **DBSCAN**
- Density-based clustering  
- Captures irregular patterns  
- Identifies noise/anomalies (e.g., extreme spenders)

#### **Gaussian Mixture Models (GMM)**
- Soft clustering (probabilistic)  
- Allows overlapping clusters  
- Often more realistic for financial behavior modeling

---

## 4. Results Summary (Cluster Profiles)

### Final Segments Identified

| Cluster | Customer Profile | Key Traits |
|--------|------------------|------------|
| **Cluster 1** | High‑value transactors | High purchasing activity, strong repayment behavior, high credit limits |
| **Cluster 2** | Revolvers | High balances, low full-payment rates, moderate purchases |
| **Cluster 3** | Low‑usage customers | Minimal spending, low frequency of purchases, low transaction volume |
| **Cluster 4** | Cash‑advance dominant users | High cash‑advance transactions, elevated financial risk, low full payments |

### Key Observations

- **High-value customers** have strong financial discipline and represent the best target for premium upgrades.  
- **Revolvers** carry balances monthly, posing potential credit risk but high interest revenue.  
- **Low-usage customers** may benefit from engagement incentives.  
- **Cash-advance users** show elevated financial stress and may need credit-limit adjustments or intervention.

---

## 5. Business Insights

The clustering results yield actionable insights:

- Premium rewards and installment plans can be targeted toward **high-value customers**.  
- **Revolver clusters** should be monitored with customized financial planning support.  
- Engagement campaigns can activate **low-usage** customer groups.  
- **Cash-advance heavy users** require monitoring and targeted risk mitigation strategies.

---

## 6. Future Work

- Use PCA for dimensionality reduction  
- Explore hierarchical clustering  
- Build a dashboard in Tableau or Power BI  
- Develop cluster‑specific marketing simulations  
- Integrate demographic variables for richer segmentation  

---

## 7. Citation

Dataset: https://www.kaggle.com/arjunbhasin2013/ccdata

---
