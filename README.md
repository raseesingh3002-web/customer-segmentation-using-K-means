# Customer Segmentation using K-Means Clustering

Segmenting 2,216 retail customers to find who drives revenue and how marketing should treat each group.

## Key Findings
- **48% of customers generate 88% of revenue.** The high-value segment spends 8x more per customer (1,121 vs 136).
- **High-value customers respond to campaigns 2.4x more** (39% vs 16% accepted at least one campaign).
- **Low-value customers browse but don't buy:** 6.5 web visits/month vs 4.0, yet less than half the web purchases (2.5 vs 5.8).
- High-value customers buy across all channels, especially store (8.4) and catalog (4.8 vs 0.8).

## Recommendations
| Segment | Action | KPI to track |
|---|---|---|
| High-value (1,060) | Retention: loyalty perks, premium offers, catalog campaigns | Repeat purchase rate, churn |
| Low-value (1,156) | Conversion: targeted web discounts and cart reminders | Web visit to purchase conversion |
| Both | Segment-specific campaigns instead of one mass campaign | Campaign response rate by segment |

## Data
Kaggle "Customer Personality Analysis" dataset: 2,240 customers, 29 columns (demographics, spending by category, purchase channels, campaign responses). 24 rows with missing income were removed, leaving 2,216.

## Approach
1. **Cleaning:** handled missing values, converted dates
2. **Feature engineering:** Age, Total Children, Total Spending, Customer Tenure
3. **EDA:** distributions, income by education, spending by marital status, correlations, campaign acceptance
4. **Clustering:** scaled 7 features, ran K-Means for k = 2 to 9, chose k = 2 by Silhouette Score (0.32)
5. **PCA:** 6 components (96% variance) gave slightly cleaner clusters (0.33) with the same segments
6. **Business analysis:** revenue share, channel mix, campaign response and product mix per segment

## Tools
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
