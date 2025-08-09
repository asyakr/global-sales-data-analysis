# Analysis Notes

## 1. Missing Data Handling
- **Countries table:** About 0.4% missing values in `alpha_2`, `region`, and `sub_region`. Filled with `'Unknown'` to keep primary key integrity.
- **Events table:** 6.17% missing `country_code` values. Filled with `'Unknown'` to retain essential order data.  
  0.15% missing `units_sold` removed because they can distort analysis.
- **Products table:** No missing values.

## 2. Data Types & Duplicates
- Fixed data types: converted `order_date` and `ship_date` to datetime, `units_sold` to int.
- Standardized `sales_channel` casing.

## 3. Revenue, Cost, and Profit Analysis
- **Top revenue:** Office Supplies (> $400M).
- **High cost but low margin:** Office Supplies, Household, Meat.
- **Efficient categories:** Cosmetics, Clothes — lower costs, higher profits.
- **Unprofitable:** Meat (high cost matches revenue).
- **Promising:** Clothes (low cost, modest revenue, strong profit).

## 4. Sales by Category
- **Highest sales**: Office Supplies (>600k sales).
- **Lowest sales**: Household (>450k sales).
- Profits do not always match sales volume — costs have strong influence.

## 5. Country Analysis
- **High revenue & cost:** Czech Republic, Ukraine, Bosnia and Herzegovina.
- **Efficient:** Andorra (good profit without high cost).
- **Weak markets:** Monaco, Georgia, Iceland.

## 6. Regional Analysis
- Europe leads in revenue (\~$1.4B) and profit (\~$600M).
- Asia significantly behind in all metrics.

## 7. Sales Channel Analysis
- Offline slightly ahead of Online in revenue, cost, and profit.
- Both channels contribute almost equally.

## 8. Shipping Time Analysis
- Slowest categories: Cereal, Office Supplies, Baby Food, Cosmetics.
- Fastest: Personal Care.
- Longest shipping countries: Hungary, Georgia, Austria (>30 days).
- Shortest: Croatia, UK, Denmark (~20 days).
- No strong correlation between shipping time and profit.

## 9. Sales Dynamics
- Office Supplies — irregular sales, stable but lower in 2017.
- Beverages — no clear seasonality, unusual peaks.
- Clothes — growing trend, peaks in Jan and summer.
- Fruits/Vegetables — stable sales.

## 10. Sales by Weekday
- High sales: Monday, Saturday, Sunday.
- Weekends — more food/drink sales.
- Monday — home/office goods.
- Clothes & cosmetics — peak on Tuesday and Saturday.

## Conclusion
Europe dominates in financial performance, with categories like Cosmetics and Clothes showing strong efficiency. Some markets (Andorra) demonstrate high profitability despite smaller scale, while others (Monaco, Georgia) lag in all metrics. Sales vary by weekday and category, offering opportunities for targeted marketing. Shipping speed differences exist mainly at the country level but do not strongly impact profit.

## Notes

All the content in `analysis.ipynb` is also available to run and explore in Google Colab.

You can view the notebook directly on GitHub or open it in Google Colab:

[[Open In Colab](https://colab.research.google.com/drive/15qCmzME-IQRrgViyheOU8Qy-wLRFl9-k?usp=sharing)]