# Problem Statement

1. IDEAL

Create a model that identifies two technical indicators and then predicts the subsequent price movement in the market. This will enable traders to have extra information to help inform their trading decisions or potentially automate parts of it. I will also be able to contrast the two candlestick patterns and determine if there is a better strategy to use.


2. REALITY

The FOREX market and all stock market prices are very hard to predict. The price movements are often described as completely random. The time series is effected by a lot of external factors other than date. Therefore the probability of getting a good prediction is low. 

Using the candlestick patterns 

So I will look at adding key exogenous or external features to help with the prediction.

I will look to include:
   + Gold prices
   + Volatility
   + Moving Averages
   
Technical traders believe that these factors are already accounted for in the price or rate. Therefore the chart patterns can be all you need to look at.


3. CONSEQUENCES

If the models are unable to predict the price movement and prove the candlestick patterns offer strong signals of market direction then this will mean traders are unable.

4. PROPOSAL


I will compare 3 algorithms ARIMAX, SARIMAX and PROPHET to see which one is best at predicting the price movement. The prediction will be based on the following 5 time frames.

A threshold will be set which is the height of the final candle and at least +/- 0.005 compared to the close price. If the algorithm predicts a price higher or lower than the threshold and the actual price goes beyond this it will be judged a success.

Therefore I will use a confusion matrix to analyse the results and will look at precision, accuracy and recall to determine the performance of the stratey and the models.

The best model w

I will then use MLR exploring penalty features such as Lasso, Ridge and Elastic Net to help create predictions



A key area would be to infer what the strategy implications are and explain the key factors to success or failure of the model.




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


