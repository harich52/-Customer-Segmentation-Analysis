Customer Segmentation Analysis (RFM + K-Means)
Segmenting an e-commerce customer base into actionable marketing groups using RFM features and K-Means clustering.

Overview
This project analyses the classic UCI "Online Retail" dataset (541,909 transactions, 4,338 unique customers from a UK-based online gift retailer) and groups customers by purchasing behaviour so that marketing efforts can be targeted per segment.

Tech Stack
Python · pandas · NumPy · scikit-learn (KMeans, StandardScaler) · matplotlib · seaborn · Jupyter Notebook

What the notebook does
Data loading & inspection — structure, dtypes, missing values, duplicates
Cleaning — drops null CustomerIDs, removes cancelled orders/returns and non-positive quantities & prices
Descriptive statistics — average purchase value, orders per customer, customer lifetime value, top products and countries
Feature engineering (RFM) — Recency, Frequency, Monetary value per customer
Scaling — StandardScaler on skew-corrected RFM features
Choosing K — elbow method (inertia) + silhouette score → K = 4
Clustering — K-Means fit and cluster label assignment
Visualisation — RFM distributions, elbow/silhouette curves, cluster scatter plots, segment size and revenue bar charts (10 charts total)
Segment profiling & insights — a recommended marketing action for every segment
Results
Segment	Share of customers	Share of revenue	Recommended action
Champions	17%	65%	VIP perks, early access, referral programme
Loyal / Potential	27%	—	Cross-sell bundles, loyalty points to push frequency
Occasional / Recent	20%	—	Onboarding nurture emails, second-purchase discount
At-risk / Lapsed	37%	6%	Win-back campaign, strong reactivation offer
Key stats: average order value £479.56, 4.27 orders per customer, average customer lifetime value £2,048.69.

Files
Customer_Segmentation_RFM_KMeans.ipynb — fully executed end-to-end notebook
customer_segments.csv — per-customer RFM scores with assigned cluster and segment label
How to run
pip install pandas numpy scikit-learn matplotlib seaborn jupyter openpyxl
jupyter notebook Customer_Segmentation_RFM_KMeans.ipynb
The notebook downloads the Online Retail dataset automatically; alternatively place Online Retail.xlsx next to the notebook.
