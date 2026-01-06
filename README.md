## Project Description

In this project, I explored and deepened my understanding of PySpark, Databricks, Databricks MLflow, and Databricks Dashboards. I worked through a series of notebooks where I performed data ingestion, transformation, and analysis using PySpark within the Databricks environment. I leveraged Databricks MLflow to track experiments, manage model versions, and streamline the machine learning workflow. Additionally, I utilized Databricks Dashboards to visualize key metrics and share insights interactively. This hands-on approach allowed me to gain practical experience with the Databricks platform and its integrated tools for big data processing, machine learning, and collaborative analytics.

## Unsupervised Clustering Methods

As part of my analysis, I applied two different types of unsupervised clustering methods: DBSCAN and hierarchical clustering. These techniques enabled me to identify patterns and groupings within the data without relying on labeled outcomes. By comparing the results from both methods, I gained insights into the structure and distribution of the dataset, enhancing the overall analytical depth of the project.

## Cluster Analysis & Interpretation

Below is the summary statistics for each cluster. Let's interpret the clusters based on their characteristics:

 Cluster | Units Purchased | Loyalty Segment | Num Orders | Count |
---------|----------------|----------------|------------|-------|
 **1**   | Moderate units, moderate spend, moderate tenure, low recency | Average loyalty, moderate order count, moderate product/category diversity | Represents steady, engaged customers with consistent purchasing behavior. | **16** |
 **2**   | Lower units, higher spend, high avg order value, long tenure | Slightly higher loyalty, fewer orders, higher product/category diversity | Likely high-value, less frequent buyers who purchase larger baskets. | **7** |
 **3**   | Very high units, very high spend, single order, long tenure | No loyalty, single product/category | Outlier: Possibly a one-time bulk purchase, not a typical loyal customer. | **1** |
 **4**   | High units, extremely high spend, single order, moderate tenure | High loyalty, single product/category | Outlier: Another one-time, very high-value purchase, possibly a business or special event. | **1** |

**Business Insights:**
- **Cluster 1:** Target for loyalty programs and retention strategies; these are your core, repeat customers (**16** customers).
- **Cluster 2:** Upsell/cross-sell opportunities; focus on increasing purchase frequency (**7** customers).
- **Cluster 3 & 4:** Investigate for special cases (bulk/corporate orders); may require different engagement or service models (**1** customer each).

These interpretations can guide marketing, retention, and product strategies tailored to each segment.

## Findings & DBSCAN Limitations

While hierarchical clustering produced meaningful and interpretable segments, DBSCAN did not perform as well on this dataset. DBSCAN struggled to identify distinct clusters due to the relatively small sample size and the presence of clusters with varying densities. Many data points were labeled as noise or grouped into a single large cluster, making it difficult to extract actionable insights. This highlights the importance of choosing clustering algorithms that match the data characteristics—DBSCAN is best suited for larger datasets with well-separated, dense clusters, whereas hierarchical methods can be more robust for smaller, less uniform datasets.