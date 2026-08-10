# Retail-Customer-Segmentation
This project describes retail customer segmentation for a POS/retail business using K-Means clustering to identify customer groups and generate actionable business insights.

**Project Title**: Retail Customer Segmentation 

**Model Used**: K-Means Clustering

**Project Overview**
This project applies K-Means clustering to POS retail customer transaction data to identify distinct customer segments based on purchasing behaviour. Transaction data used include: Days Since Last Purchase (Recency), Total Transactions (Frequency), Total Products Purchased, Total Spend (Monetary) and Average Transaction Value, and use a simple clustering algorithm (K-Means) to group customers into two segments:  Cluster 0 - 264 - Low-value and at risk customers; and Cluster 1 - 224 - High-value and Loyal customers.

**Project Objective**
The objective of this project to build an MVP to cluster customers for a POS /retail business that clusters customers based on purchasing behaviour, to help a POS/retail business understand its customers, improve customer retention, develop targeted marketing strategies, and make data-driven decisions.

**Specific Objectives**
- Prepare and clean the retail transaction data – (Retail_pos_basket_data.csv)
- Customer-level behavioural features engineering.
- Scale the numerical features.
- Determine the optimal number of clusters.
- Apply K-Means clustering.
- Profile the resulting customer segments.
- Evaluate the clustering results.
- Generate actionable business recommendations.
  
**Features Used**
The following customer-level features were used for clustering:
- Days Since Last Purchase (Recency)
- Total Transactions (Frequency)
- Total Products Purchased
- Total Spend (Monetary)
- Average Transaction Value
The `user_id` column was excluded from clustering because it is an identifier and does not represent customer behaviour.

**Tools & Technologies**
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
  
**Project Workflow**
1. Data Preparation
2. Feature Engineering
3. Feature Scaling
4. Elbow Method
5. K-Means Clustering
6. Cluster Profiling
7. Model Evaluation
8. Business Recommendations

**Model Evaluation**
The Elbow Method suggested **2 clusters** as the appropriate number of customer segments.
The Silhouette Score for K = 2 was **0.335**, indicating moderate separation between the customer groups.
The final model produced two customer segments:
| Cluster | Number of Customers | Description |
|--------|--------------------:|-------------|
| Cluster 0 | 264 | Low-value / At-risk customers |
| Cluster 1 | 224 | High-value / Loyal customers |

The final K-Means model produced two reasonably balanced clusters containing 264 and 224 customers. The cluster profiles show clear differences in purchasing behaviour, particularly in recency, transaction frequency, number of products purchased, and total spending. These differences indicate that the clustering successfully identified meaningful customer segments.

**Customer Segments**
Cluster 0 — Low-Value / At-Risk Customers
These customers have:
- Longer periods since their last purchase.
- Fewer transactions.
- Fewer products purchased.
- Lower overall spending.
  
**Recommendation:**  
Use targeted re-engagement campaigns, personalised promotions, discounts, and loyalty incentives to encourage repeat purchases.

Cluster 1 — High-Value / Loyal Customers
These customers:
- Purchase more frequently.
- Purchase more products.
- Spend significantly more.
- Have more recent purchase activity.
  
**Recommendation:**  
Focus on retention through VIP rewards, exclusive offers, personalised recommendations, and loyalty programmes.

**Key Business Insights**
The analysis shows that customers have significantly different purchasing behaviours. Identifying these segments allows the business to avoid using a one-size-fits-all marketing strategy.
The business can target each customer group according to its specific characteristics and value.

**Future Improvements**
Future work could include:
- Testing other clustering algorithms such as DBSCAN and Hierarchical Clustering.
- Adding demographic or geographic customer information.
- Building an interactive dashboard using Power BI or Tableau.
- Testing additional clustering evaluation metrics.
- Developing a customer churn prediction model.

Repository Structure
```text
Retail-Customer-Segmentation/
│
├── data/
│   ├── README.md
│   └── Retail_pos_basket_data.csv
│
├── Retail_Customer_Segmentation.ipynb
├── README.md
├── LICENSE
└── .gitignore

**Dataset**
The dataset contains retail transaction records used to analyse customer purchasing behaviour.
The dataset was cleaned and transformed into customer-level features including
- Days since last purchase
- Total transactions
- Total products purchased
- Total spend
- Average transaction value

The raw data is available in the "data"  folder.

**Author**
Ogunjinmi Temitayo Olubunmi
Data Science Capstone Project - Retail Customer Segmentation Using K-Means Clustering
