# Final Project Summary

## Summary of my Final Project
Summary of my Final Project for the Data Anlysis with Python module of the IBM Generative AI Engineering Professional Certificate

I worked with the Seattle house price dataset, handling missing values in the `bedrooms` and `bathrooms` columns by replacing them with the mean. I explored the data using value counts, boxplots, and correlation analysis to understand the relationships between features and price.

For model development, I tried a number of different approaches to find the most effective model:
- Simple linear regression using only `long` (longitude) gave a very low R² (≈ 0.0005), showing it's a poor predictor
- Using only `sqft_living` improved the R² to about 0.49
- Multiple linear regression with 11 features increased the R² to about 0.66
- I then used a pipeline with scaling and second-order polynomial features, which raised the R² to about 0.75 on the full dataset
- For a more realistic evaluation, I split the data into training and test sets and used Ridge regression (alpha=0.1). This gave an R² of about 0.65 on the test set
- Finally, I combined Ridge regression with second-order polynomial features, achieving an R² of 0.70 on the test set

## Best Model

The most effective model I built was a Ridge regression with second-order polynomial features (degree=2, alpha=0.1), evaluated on the test set. This model achieved an R² of **0.70**, which means it explains 70% of the variance in house prices on unseen data. This approach balances model complexity and generalization, making it the most effective model in my analysis.