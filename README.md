# Retail-Margin-and-Category-Performance-Analysis

**Tools:** Python · pandas · Power BI · Excel  

**Data:** Online Retail II dataset (UCI Machine Learning Repository)  
https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci

**Coverage:** 958K UK transactions · 12 product categories

## Overview

Analyses retail transaction data to identify margin performance, pricing risks, and commercial opportunities across product categories. Products are classified into 12 categories using keyword-based rules, enriched with category-level margin assumptions, and flagged by commercial role — from high-performing stars to hidden gems and underperformers.

## Key Findings

- **20 underperforming SKUs** identified - active products (100+ units sold) earning less than 50% of their category average revenue
- Categories flagged across four commercial tiers: Star, Hidden Gem, Pricing Risk, and Complex Range
- Monthly trends reveal seasonality patterns by category, informing stock and pricing decisions
- Revenue vs margin scatter identifies categories with high volume but thin margins - pricing risk candidates


## Methodology

| Step | Approach |
|---|---|
| Cleaning | Removed returns (Quantity ≤ 0), zero-price rows, null descriptions; filtered to UK only |
| Categorisation | Keyword-based classification into 12 product categories from product descriptions |
| Margin modelling | Category-level gross margin assumptions applied; revenue, cost, and profit derived per transaction |
| Underperformer flag | Products with 100+ units sold but revenue < 50% of category average |
| Commercial flag | Rule-based tiering: Star · Hidden Gem · Pricing Risk · Complex Range · Stable |


## Commercial Flags

| Flag | Criteria |
|---|---|
| ⭐ Star — Protect & Grow | Margin ≥ 60% and revenue > £500K |
| 💎 Hidden Gem — Expand | Revenue < £300K but margin ≥ 55% |
| ⚠️ Risk — Review Pricing | Margin < 50% |
| 🔀 Complex — Rationalise Range | 400+ products and margin < 55% |
| ✅ Stable — Monitor | All others |
