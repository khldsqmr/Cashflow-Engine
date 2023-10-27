# Cashflow-Engine

The Cashflow Engine is a financial forecasting tool designed to project the balances of term deposit products for customers over a specified time period. It utilizes a combination of classification algorithms and regression models, incorporating both internal and external variables to make accurate predictions.

## Step 1: Classification Algorithm

### Dataset:

Consider a dataset with the following variables:

#### Internal Variables:
- Initial deposit amount
- Interest rates
- Maturity date
- Early withdrawal penalties
- Customer demographics (age, income, education level, etc.)
- Account type
- Account status
- Transaction history (number of deposits, withdrawals, etc.)

#### External Variables:
- Economic indicators (e.g., inflation rates, interest rate trends)
- Market conditions
- Regulatory changes affecting interest rates

This dataset will have historical data for a group of customers who have term deposit products.

### Classification Algorithm:

We'll use a decision tree classifier to predict the withdrawal behavior of customers in the next month. This model will take into account the features mentioned above and determine whether a customer is likely to fully withdraw, partially withdraw, or not withdraw at all.

## Step 2: Balance Prediction

### Using Classification Results:

Once we have the classification results, we can proceed with balance predictions for the next month:

- For customers predicted to fully withdraw, set their next month's balance to 0.
- For customers predicted to not withdraw, keep their next month's balance the same as the current month.
- For customers predicted to partially withdraw, use a linear regression model to estimate the amount of withdrawal and adjust the balance accordingly.

## Step 3: Overall Balance Forecasting

### Forecasting for 12 Months:

Using the trained classification and regression models, we can apply them to the entire customer base for the next 12 months. This will give us a forecasted balance for each customer for each of the next 12 months.

### Aggregating Results:

Sum up the forecasted balances for all customers to get the overall balance for the term deposit product for each of the next 12 months.

## Storytelling Results:

### Month 1:

After applying the classification algorithm, we found that 30% of customers are likely to fully withdraw, 50% are expected to not withdraw, and 20% are predicted to partially withdraw.

Using these predictions, we adjusted the balances accordingly. Some customers will start the month with a clean slate, while others will continue with their existing balance.

### Months 2-11:

We continued this process for the next 10 months, adjusting the balances based on the withdrawal behavior predictions.

### Month 12:

As we approach the end of the term, our models predict a surge in withdrawals. This is consistent with typical behavior as customers tend to cash out at maturity.

### Overall Balance:

Over the next year, our forecasts show a steady decrease in overall balance due to anticipated withdrawals. This aligns with expectations for a term deposit product.

Remember, the actual results may vary based on the quality of the data and the accuracy of the models. Continuous monitoring and model refinement will be crucial for maintaining accurate forecasts over time.
