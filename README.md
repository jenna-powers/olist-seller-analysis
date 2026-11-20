# What Separates Top Sellers from the Rest?
An analysis of Olist’s Brazilian e-commerce marketplace using SQL and R, presented as a Quarto dashboard.
[View the Live Dashboard](https://jenna-powers-olist-seller-analysis.share.connect.posit.cloud/)

## Key Findings
- The top 20% of sellers generate 82.7% of revenue.
- Reviews, delivery speed, and location don’t explain the gap: ratings are nearly identical (4.10 vs. 4.12), and top sellers deliver about a day slower.
- Top sellers win mainly on volume. They sell about 14 times as many items, at prices only modestly higher.
- Bottom 80% revenue is growing steadily, while top-seller revenue has stalled since early 2018.

## Approach
I tested whether reviews, delivery speed, or location explained the difference. None did. Instead, top sellers stand out mainly on volume: they sell far more items at similar prices. I also forecast revenue for each group over the next six months, choosing models by cross-validation. [Methods](https://jenna-powers-olist-seller-analysis.share.connect.posit.cloud/)

## Data
I used the order items, orders, sellers, and reviews tables from the [Olist Brazilian E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/data), which contains orders made on Olist’s marketplace from 2016 to 2018. The raw data isn't included in the repo due to its size, but it can be downloaded from the above link. 
## Repository Structure
```
├── _setup.qmd          # Packages and plot theme
├── build_database.qmd  # Builds the database
├── analysis.qmd        # Queries, analysis, and forecasting
├── dashboard.qmd       # Dashboard layout and charts
├── styles.css          # Custom styling for the Methods page
└── rds/               # Saved results used by the dashboard
```

## Limitations and Next Steps

### Limitations
- **Short History**: The data covers about 20 months, which limits how reliable the forecast is and means the models can’t learn yearly patterns like Black Friday.
- **How Top Sellers Are Defined**: Top sellers are identified using revenue across the full dataset, so the group was chosen with knowledge of how sellers performed over the entire period. This may make their historical trend look different than it would for a group defined in advance.
- **Associations, Not Causes**: The findings show how top sellers differ from the rest, but can’t show whether those differences cause their success.

### Next Steps
- **Product Categories**: Check whether top sellers are concentrated in certain categories, which could explain their higher sales volume.
- **Predicting Future Top Sellers**: Build a model using sellers’ early activity to predict which new sellers will become top sellers.
- **A Fixed Seller Group**: Define top sellers using 2017 data only, then track how that group performs in 2018 for a cleaner forecast.

## Contact
**Jenna Powers**
- LinkedIn: [linkedin.com/in/jenna-n-powers](https://linkedin.com/in/jenna-n-powers)
- Email: [jennapowers114@gmail.com](mailto:jennapowers114@gmail.com)

