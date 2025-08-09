# Sales Data Analysis

## Description
This project analyzes sales data to explore revenue, cost, and profit across different categories, countries, regions, and time periods.  
The dataset includes order details, product information, and country data.  
Key objectives:
- Identify top and low-performing product categories.
- Compare financial performance by country and region.
- Analyze shipping times and their relation to profitability.
- Study sales dynamics over time and by weekday.

The analysis also covers **cost, revenue, and profit** distribution, highlighting efficiency and market potential.

## Project Structure
- `notebooks/analysis.ipynb` — main Jupyter Notebook with full data cleaning, analysis, and visualizations.
- `docs/analysis_notes.md` — detailed analysis notes with insights.
- `README.md` — project overview.

## Data Sources
The dataset contains:

1. **Countries Table**
- `name`: Full country name
- `alpha_2`: 2-letter country code
- `alpha_3`: 3-letter country code
- `region`: Geographical region
- `sub_region`: More specific sub-region
2. **Events Table (Main table)**
- `order_id`: Unique order identifier
- `order_date`, ship_date: Order and shipping dates
- `order_priority`: Priority level of the order
- `country_code`: 3-letter country code (links to Countries table)
- `product_id`: ID of the purchased product (links to Products table)
- `sales_channel`: Sales platform or method (e.g., Online, Offline)
- `units_sold`: Number of items sold
- `unit_price`: Price per unit
- `unit_cost`: Cost per unit
3. **Products Table**
- `id`: Product identifier
- `item_type`: Type of the product

**Table Relationships**
- df_events.`product_id` → df_products.`id`
- df_events.`country_code` → df_countries.`alpha_3`

## Main Metrics
- **Orders quantity:** 1328  
- **Countries quantity:** 45  
- **Total revenue:** $1,702,129,408.21  
- **Total profit:** $501,434,459.00  
- **Product type quantity:** 12

## Tools & Libraries
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook

## Main Notebook

All the content in `analysis.ipynb` is also available to run and explore in Google Colab.

You can view the notebook directly on GitHub or open it in Google Colab:

[[Open In Colab](https://colab.research.google.com/drive/15qCmzME-IQRrgViyheOU8Qy-wLRFl9-k?usp=sharing)]
