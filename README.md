# Market Basket Analysis for Retail Strategy

Association Rule Mining with Apriori on 500,000+ retail transactions to uncover high-lift cross-sell product bundles.

## Dataset
[Online Retail dataset — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail):
Transactions from a UK-based online retailer (Dec 2010 – Dec 2011).

## Method
1. **Cleaning (Pandas):** Removed cancelled orders, missing descriptions, and negative quantities
2. **Basket encoding:** Pivoted invoices × products into a boolean basket matrix
3. **Apriori algorithm (MLxtend):** Mined frequent itemsets at 5% minimum support
4. **Association rules:** Generated and ranked rules by support, confidence, and lift
5. **Visualization:** Plotted top 8 bundles by lift with Matplotlib
6. **Output:** Filtered to bundles with ≥65% confidence; exported rules to CSV for Power BI reporting

## Key Result
Identified high-confidence product bundles (confidence ≥ 65%, lift > 1) for retail cross-sell strategy.

![Top bundles](top_bundles.png)

## Business Impact
Use these bundles for product placement, email recommendations, and promotional bundling to increase AOV [Average Order Value].

## Tech Stack
Python · Pandas · MLxtend · Matplotlib · Power BI.

## Files
- `market_basket_analysis.ipynb`: Full analysis notebook
- `association_rules.csv`: Exported rules for Power BI 
- `top_bundles.png` :Top 8 bundles visualisation
