# FOREX Strategy Analysis and Price Prediction Project
### Can Machine Learning enhance chart patterns?



### Contents:
- [Problem Statement](#Problem-Statement)
- [Executive Summary](#Executive-Summary)
- [Key Project Information](#Key-Project-Information)
- [Recommendations](#Recommendations)
- [References](#References)



# Problem Statement

1. IDEAL

Create a model that identifies two technical indicators and use machine learning to help predicts the subsequent price movement. This will enable traders to have extra information to help inform their trading decisions or to potentially automate parts of it. 

I will also be able to contrast the two candlestick patterns and determine if there is a better strategy to use.


2. REALITY

The FOREX market and all stock market prices are very hard to predict. The price movements are often described as completely random. The time series is effected by a lot of external factors other than date. Therefore the probability of getting a good prediction is low. 

So I will look at adding exogenous or external features to help with the prediction. I will look to include gold prices, volatility and moving Averages.
   
Technical traders believe that these factors are already accounted for in the price or rate. Therefore the chart patterns can be all you need to look at. Using the candlestick patterns will aim to mark key moments in the market. Identifying these patterns help traders make decisions and it may also provide some help for the machine learning models.


3. CONSEQUENCES

If the models are unable to predict the price movement and prove the candlestick patterns offer strong signals of market direction then this will mean traders are unable to be any more informed than before.

4. PROPOSAL


I will compare three time series algorithms ARIMAX, SARIMAX and PROPHET to see which one is best at predicting the price movement. The prediction will be based on the following 5 time frames.

A threshold will be set which is the height of the final candle and at least +/- 0.005 compared to the close price. If the algorithm predicts a price higher or lower than the threshold and the actual price goes beyond this it will be judged a success.

Therefore I will use a confusion matrix to analyse the results and will look at precision, accuracy and recall to determine the performance of the stratey and the models.

After the time series predictions, I will see if by feeding the results into a multi linear regression model as a feature it can help beat the time series results. The model can also be analysed to see which features are impotant by looking at the coefficients. Lasso, Ridge and Elastic Net will be analysed to see which one gives the best results. Precision, accuracy and recall will be used again to determine the performance of the stratey and the models.

This will hopefully yield a successful model or give insight into how it could be used to enhance a strategy or traders performance.



## Executive Summary


## Key Project information


### Data Sources

The EUR/USD data came from the following web page - [FOREX data](https://www.histdata.com/).

The gold data came from the world gold council website - [Gold Data](https://www.gold.org/goldhub/data/gold-prices)


### Workbooks

The files in this repo are organised as follows:

+ 1.0 Load Data and EDA
+ 2.0 Resample, Pattern Matching and Feature Engineering-OOD-B
+ 3.0 Pre-Processing
+ 4.0 Modelling Baseline
+ 5.0 Modelling-ARIMAX
+ 6.0 Modelling Prophet
+ 7.0 Modelling-Multiple linear Regression
+ 8.0 Conclusions and Recommendations


### Exernal Libraries

+ [Prophet Facebook](https://facebook.github.io/prophet/) - for times series forecasting
+ [Plotly](https://plotly.com/python/) - to produce candlestick graphs
+ [pmdarima](https://pypi.org/project/pmdarima/) - help with arimax hyperparameters and acf/pacf plots



## Pattern Descriptions

![fractal](/images/Fractal.png)

A fractal is a pattern where the middel candles high is higher than the highs on the left and right. Then the outer candles a lower again

![Marubozu](/images/Marubozu.png)

The Marubozu pattern i am looking at is when the candle next to it is the same height but in the opposite direction.


## Recommendations


What were your findings?
What risks/limitations/assumptions affect these findings?

#### rec 1

#### rec 2


## References
[Online web property search](https://www.realtor.com/realestateandhomes-search/Ames_IA)

[FOREX data](https://www.histdata.com/)
[Technical Indicators](https://www.histdata.com/)
