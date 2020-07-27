# Problem Statement

1. IDEAL

Create a model that identifies technical indicators and then predicts the subsequent price movement in the market. This will initially focus on Marubuzo.


2. REALITY

The FOREX market and all stock market prices are very hard to predict. The price movements are often described as completely random. The time series is effected by a lot of external factors other than date. Therefore the probability of getting a good prediction is low. 

So I will look at adding key exogenous or external features to help with the prediction.

I will look to include:
   + Inflation rates
   + Interest rates
   + Volatility
   + Moving Averages on 3 time lags
   

Technical traders believe that these factors are already accounted for in the prices or rates. Therefore the chart patterns can be all you need to look at. It will be interesting to see if they do have an impact on price prediction.


3. CONSEQUENCES

Currently traders have trouble predicting their entry and exit points. They are often right but either miss a trade, get stopped out too soon or in trying to find maximum profit miss time their exit. Without this model to give them guidelines to work with

4. PROPOSAL

After comparing 3 algorithms ARIMAX, SARIMAX and Prophet I will create a final model to predict the highest stock price in the next 3 time frames. 

I will use RMSE as my accuracy score. My benchmark will be predicting the current price. I choose this due to high correlation in the prior prices. Given the nature of the randomness of the stock market this might be harder to beat than it sounds.


A key area would be to infer what the strategy implications are and explain the key factors to success or failure of the model.


Bonus:
+ Learn how to implemnet a bot on a trading account
+ Create a python based web app to track results

## Executive Summary



### Contents:

- [Data Dictionary](#Data-Dictionary)
- [Data Collection](#Data-Collection)
- [Visualising and Relationships in the data](#Visualising-and-Relationships-in-the-data)
- [Key Outside Research Summary](#Key-Outside-Research-Summary)
- [Recommendations](#Recommendations)
- [References](#References)


## Data Dictionary





## Data Collection

Data collection was challenging due to the large amounts os missing data. I tried to impute where possible. I used a range of techniques such as using averages, predicting with SLR and using 0 to remove any weighting.

I also used the original Kaggle data to check any outliers.


## Visualising and Relationships in the data

The work book contains many visualisations. The following box plot shows some of the key relationships with sales price.

![Correlations](/images/key_correlations.png)



## Key Outside Research Summary


## Recommendations

#### rec 1

#### rec 2


## References
[Online web property search](https://www.realtor.com/realestateandhomes-search/Ames_IA)


