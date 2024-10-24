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


I will compare three time series algorithms ARIMAX, SARIMAX and PROPHET to see which one is best at predicting the price movement. The prediction will be based on the next 5 time frames.

A threshold will be set which is the height of the final candle and at least +/- 0.005 compared to the close price. If the algorithm predicts a price higher or lower than the threshold and the actual price goes beyond this it will be judged a success.

Therefore I will use a confusion matrix to analyse the results and will look at precision, accuracy and recall to determine the performance of the stratey and the models.

After the time series predictions, I will see if by feeding the results into a multi linear regression model as a feature it can help beat the time series results. The model can also be analysed to see which features are impotant by looking at the coefficients. Lasso, Ridge and Elastic Net will be analysed to see which one gives the best results. Precision, accuracy and recall will be used again to determine the performance of the stratey and the models.

This will hopefully yield a successful model or give insight into how it could be used to enhance a strategy or traders performance.



## Executive Summary


Using candlestick patterns, time series modelling and multiple linear regression (MLR) together has proven to be succesful. This combination predicts whether the market will move over a set threshold. The precision that this combination has produced is 84% and the accuracy is 72%. This would be a useful tool for traders to use to help enhance their trading strategies. It means that when the model predicts a move up or down as appropriate then the market has a 84% chance of at least breaking this threshold price.

The best combination was using fractals, Arimax and MLR using Elastic net regularisation. The ARIMAX prediction that fed into the MLR was high up the coeffient ranks and only behind the prior days price.


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

A fractal is a pattern where the middle candles high, is higher than the highs on the left and right. Then the outer candles are lower again.

![Marubozu](/images/Marubozu.png)

The Marubozu pattern I am looking at is when the candle next to it is the same height but in the opposite direction.


## Recommendations


Overall there have been some good success:

+ Using ARIMAX, MLR and the fractal pattern has shown some good results.
+ It shows that Machine Learning can be used to optimise parts of the candlestick pattern trading

However this can be tempered by:

+ Getting the market decision correct may not lead to profit. The model assumes that there are no stop losses. Therefore it doesnt factor in that a correct decision over 5 time frames may move initially in the wrong drectino before recovering at which point the trade has already been closed at a loss.

+ It also doesnt factor in the cost of entry and exit from positions. The spread may lead to a significant reduction in profit. Although 50pips would be a worthwhile trade for a spread bet it still may not be enough if it doesnt satify risk reward levels.

## Further study

+ More strategies: The OOD design means I would just have to code the subclass and then it would be ready to go.
+ More markets: Feeding new currency pairs into the superclass means that it will be quick to try other markets.
+ Other Models: I would like to try RNN and XG Boost to see if the results improve further.
+ Increase the parameters: If I spent more time tuning the model with more features then maybe Increasing the threshold might lead to a more tradable strategy.
+ Risk Management: Use the model to predict the opposite low/high point and then determine where an appropriate stop loss can be placed.
+ Create a strategy: Usee this to create a strategy and backtest it to see how it performs.



## References
[Online web property search](https://www.realtor.com/realestateandhomes-search/Ames_IA)
[FOREX data](https://www.histdata.com/)
[Technical Indicators](https://www.histdata.com/)
