# Sephora Website Data Analysis Project

## Project Overview
This project analyzes Sephora's product data to identify factors influencing pricing and customer engagement. Using a dataset of 6,108 products, the analysis follows the **DCOVAC framework** (Define, Collect, Organize, Visualize, Analyze, Conclusion) to explore relationships between predictors like product ratings, exclusivity, and customer feedback, and outcomes such as price and customer affinity (measured by "LOVE" counts). The goal is to provide actionable insights for optimizing pricing strategies and improving customer satisfaction.

## Features
- **Data Exploration**: Summary statistics and variable transformations (e.g., categorical conversions).
- **Visualizations**: Density plots, scatter plots, correlation matrices, and regression diagnostics.
- **Predictive Modeling**:
  - **Linear Regression**: Predicts `PRICE` using variables like `SIZE`, `RATING`, and `VALUE_PRICE` (Adjusted R² = 97%).
  - **Logistic Regression**: Predicts binary `CAT.PRICE` (price above/below $50) with high sensitivity (94.7% training, 95.7% validation).
- **Model Refinement**: Outlier analysis and residual checks to improve validity.

## Tools Used
- **R Libraries**: `tidyverse`, `GGally`, `caret`, `flexdashboard`.
- **Visualization**: `ggplot2`, `ggpairs`.
- **Modeling**: Linear regression, nominal logistic regression.

## Key Findings
1. **Price Sensitivity**: Higher-priced products receive significantly fewer "LOVE" counts, indicating a price-sensitive customer base.
2. **Predictors of Price**:
   - Strong positive correlation with `VALUE_PRICE` (discounted products).
   - Negative correlations with `NUMBER_OF_REVIEWS` and `LOVE`.
3. **Model Performance**:
   - Linear regression explains 97% of price variance, highlighting the impact of exclusivity and limited editions.
   - Logistic regression achieves <3% error in classifying high/low-priced products.

## Business Impact
- **Pricing Strategy**: Sephora can optimize pricing by focusing on exclusivity (`EXCLUSIVE`) and limited-time offers (`LIMITED_EDITION`), which positively influence price without reducing customer engagement.
- **Customer Experience**: Emphasize mid-range products ($0–$50) to align with observed customer preferences and boost "LOVE" metrics.
- **Inventory Management**: Prioritize high-rated products with moderate review counts, as these correlate with stable pricing and customer interest.
