# Marketing Budget Optimization using Linear Regression

## Project Overview
This project analyzes marketing spend data to build a multiple linear regression model. The objective is to understand which marketing channel (TV, Radio, Social Media, Search Ads, Influencer) yields the best return on investment (ROI) and to recommend optimal future budget allocations.

## Business Problem
The leadership team wants to allocate marketing budgets efficiently.
- **Why it matters:** Efficient allocation reduces wasted ad spend and maximizes sales revenue.
- **Predictive Goal:** Sales or Revenue based on marketing spend.
- **Independent Variables:** TV spend, Radio spend, Social media spend, Digital ad spend, Influencer spend.
- **Dependent Variable:** Sales / Revenue.
- **Why Regression:** We are predicting a continuous target (sales) based on linear combinations of continuous variables (marketing spend). It helps directly measure the marginal impact (coefficient) of each channel.

## Dataset Description
The dataset `part_4_marketing_budget_optimization.csv` contains historical campaign performance with marketing spend metrics across different channels and resulting sales.

## Data Cleaning Summary
- Verified data types and handled missing values and duplicates to ensure data quality before model building.

## EDA Insights
- Visualized distributions of all variables.
- Plotted scatter charts to observe raw relationship between each channel spend and sales.
- Generated a correlation heatmap to quantitatively inspect collinearity and target relationship.
- Channels like TV typically show a strong positive correlation with sales.

## Regression Model Summary
A Multiple Linear Regression model was built using `scikit-learn`. The data was split 80/20 into training and testing sets.

## Model Evaluation Results
Evaluated the model using the following metrics on the test set:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

*Refer to the notebook for the exact values generated during runtime.*

## Coefficient Interpretation
The regression coefficients tell us the impact of each channel. A higher, positive coefficient indicates a stronger positive impact on sales per unit of currency spent on that channel.

## Budget Recommendation
- **Increase Budget:** Channels presenting the highest positive coefficients.
- **Decrease Budget:** Channels presenting near-zero or negative coefficients.
- **Context/Risks:** Regression assumes a linear relationship without saturation. Large increases in budget may face diminishing returns.

## How to Run the Project
1. Clone the repository.
2. Install dependencies via: `pip install -r requirements.txt`
3. Open `notebook.ipynb` in Jupyter Notebook or VS Code to run the cells and view analysis and visualizations.