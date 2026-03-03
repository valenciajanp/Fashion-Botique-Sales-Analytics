# Fashion-Botique-Sales-Analytics

Overview / Business Problem
A fashion boutique wants to optimize revenue, customer satisfaction, and inventory management.
The boutique faces the following challenges:
-High return rates affecting profitability
-Markdown strategies that may not be effective
-Overstock or understock of products relative to customer preferences
-Understanding how product features, discounts, and customer behavior impact returns and satisfaction
-Goal: Use Python to clean, analyze, and visualize sales and product data to provide actionable business insights.

Dataset
Source: Kaggle (pratyushpuri/retail-fashion-boutique-data-sales-analytics-2025)
Size: 2,176 product purchase records
Columns:
product_id, category, brand, season, size, color,original_price, markdown_percentage, current_price,purchase_date, stock_quantity,customer_rating, is_returned, return_reason

Data characteristics
-Some missing values
-Pricing inconsistencies exist

Steps Taken
  Data Wrangling & Cleaning
  -Converted purchase_date to datetime, and categorical columns to category type.
  -Validated pricing logic: calculated price vs actual price.
  -Handled missing values and flagged potential issues.
  -Created new features:
  -discount_amount = original_price - current_price
  -purchase_month = purchase_date.month

  Exploratory Analysis
  -Calculated overall return rate: 14.7%
  -Compared markdown percentages and ratings between returned and non-returned products.
  -Checked return rates by size to identify high-risk products.
  -Analyzed stock levels and average ratings by brand to highlight inventory misalignment.
  -Checked seasonal markdown patterns.
  -Correlation analysis: price, markdown, and ratings relationships.

  Visualization
  -Scatter plot: markdown_percentage vs customer_rating to detect trends and outliers.

Key Findings
-Return rate is 14.7%, moderate for apparel.
-Higher returns observed for L (17.6%) and XS (15.9%) sizes - potential sizing issues.
-Returned items had slightly higher markdowns (12.76% vs 12.04%).
-Discounts may encourage riskier purchases, but the effect is small.
-Average ratings nearly identical for returned vs non-returned items (2.98).
-Ratings are largely independent of discounts - satisfaction depends on fit, brand, or quality.
-Brands with lower ratings (Mango: 2.78, Zara: 2.91) have stock similar to higher-rated brands - risk of overstocking low-performing products.
-Total difference of 2.5M between calculated and actual prices - indicates manual overrides or inconsistent markdown applications.
-Markdown percentages consistent across seasons (11.84%–12.49%).
-Strong correlation between original_price and current_price (0.915), weak correlation between markdown and rating (0).
-Discounts favor lower-priced items slightly, but customer ratings remain unaffected.
-Scatter plot shows no trend between markdown percentage and customer rating - discounts do not impact perceived product quality.


Business Recommendations
-Investigate sizing for L and XS to reduce return rates.
-Consider automated validation for markdowns to reduce pricing inconsistencies.
-Review inventory allocation for low-rated brands to reduce overstock.
-Maintain consistent seasonal markdown strategy, focusing on products that drive revenue.
-Monitor high-return or high-discount items for potential quality or fit issues.
