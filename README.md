# E-Commerce Customer Segmentation using RFM and Clustering

## Project Title
Part 1: E-Commerce Customer Segmentation using RFM and Clustering

## Business Problem
The company wants to design targeted marketing campaigns, improve customer retention, and identify high-value customer groups based on its transaction-level purchase data.

## Dataset Description
The dataset contains e-commerce transactions with columns for invoice number, stock code, product description, quantity, invoice date, unit price, customer ID, and country.
[Dataset Source](dataset_source.md)

## Data Cleaning Summary
- Handled missing Customer IDs and missing product descriptions by removing those rows.
- Dropped rows containing zero or negative quantities and prices.
- Excluded cancelled invoices.
- Removed duplicate records.
- Converted InvoiceDate to a proper datetime type.

## Feature Engineering Summary
We constructed an RFM (Recency, Frequency, Monetary) metric for each customer:
- **Recency**: Days since the customer's last purchase.
- **Frequency**: Distinct count of invoices (transactions).
- **Monetary**: Total revenue (Quantity * Unit Price) per customer.

## EDA Insights
- **Top Geographies**: Calculated and visualized the top countries by revenue.
- **Distributions**: Most customers purchase infrequently and have varied monetary spending, establishing clear segments of low and high-value buyers.

## Clustering Approach
- Log-transformed RFM features to handle right-skewness.
- Scaled features using Standard Scaler.
- Applied the Elbow Method to identify the optimal number of clusters.
- Trained a K-Means model to form customer segments.

## Cluster Interpretation
1. **High Value Loyal**: Buy often, spend highly, and purchased recently.
2. **Occasional / Promising**: Moderate behavior across Recency, Frequency, and Monetary constraints.
3. **At-Risk / Churned**: Haven't purchased in a long time, with minimal value and frequency.
4. **Recent Low Spenders / New**: Bought recently, but with low frequency and monetary value.

## Final Business Recommendations
- **High-Value Loyal**: Deliver VIP benefits, exclusive early access, and high-value suggestions to retain them.
- **At-Risk / Churned**: Design re-engagement campaigns and "we miss you" special discount emails.
- **Occasional / Promising**: Use cross-selling and product bundling to drive up their average order value.
- **Recent Low Spenders**: Offer onboarding journeys and discounts for their second purchase to drive retention.

## How to run the project
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Run the notebook: `jupyter notebook part1.ipynb`
