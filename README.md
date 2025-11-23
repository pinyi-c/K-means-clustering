# Customer Segmentation with K-Means

This repository contains two small customer-segmentation projects using K-Means clustering. Both focus on applying unsupervised learning to real-world style datasets and interpreting the resulting customer groups for marketing and business use.

## Project 1: E-commerce 2024 Customer Segmentation

Dataset: `customer_details.csv` (E-commerce Sales Data 2024)

Objective: Segment customers based on how much they spend and how often they purchase.

Steps:
- Clean and rename columns for easier processing.
- Map `frequency_of_purchases` (e.g., Weekly, Monthly, Annually) to numeric values in days.
- Use `purchase_amount_(usd)` and `frequency_of_purchases_days` as clustering features.
- Apply K-Means with K chosen via the Elbow method.
- Visualize the clusters and interpret segments, for example:
  - Frequent, mid-range spenders
  - Moderate-frequency customers
  - Infrequent, higher-ticket customers

This project demonstrates how to convert categorical frequency data into numeric features and build simple yet interpretable customer segments.

## Project 2: Mall Customer Segmentation

Dataset: `Mall_Customers.csv`

Objective: Explore different ways to segment mall customers using demographic and behavioral variables.

Two clustering views:
1. **Age vs Spending Score**
   - Use `age` and `spending_score_(1-100)` as features.
   - Use Elbow method and Silhouette score to select the number of clusters.
   - Apply K-Means and visualize age–spending clusters.

2. **Annual Income vs Spending Score**
   - Use `annual_income_(k$)` and `spending_score_(1-100)` as features.
   - Again use Elbow + Silhouette analysis to select K.
   - Apply K-Means and plot income–spending clusters to identify distinct customer groups (e.g., high-income low-spend, mid-income high-spend).

This project highlights how the same algorithm can yield different business insights depending on the chosen feature space.

## Methods and Tools

- Python, pandas, NumPy
- scikit-learn:
  - `KMeans`
  - `silhouette_score`
- Visualization: Matplotlib, Seaborn
- Model selection: Elbow method (WCSS) and Silhouette analysis

Both projects focus on:
- Structuring raw customer data for clustering
- Selecting features and number of clusters
- Visualizing and interpreting segments in a marketing context
