# Algo-Trading
Played around with time-series forecasting for stock prices and built Long-Short Term Recurrent Neural Net Model using Tensorflow to predict stock opening, closing, high, low, and trading volumes using historic data!

*Note: the model is obviously not extremely accurate, given the difficulty of stock performance prediction, but does a pretty good job of predicting several of the aforementioned features using only historic data

## file decsriptions:
Data_Pull.ipynb = 8 year pull of daily stock data from quandl for Adobe, Nvidia, and Microsoft + some cool time series graphs  
ModelBuilding.ipynb = LSTM model training -- 2 models; one built on selected features available from pulled quandl dataframe and another based on features suggested by this paper *  
save_model_x directories = models saved from Model_test.ipynb to be tested on data in AlpacaTesting.ipynb  
ModelPrediction.ipynb = data pull of live, current data from alpaca stock trading api and testing of saved models (trained on historic data) on this current data  

*referenced paper: https://www.researchgate.net/publication/319343084_Algorithmic_Trading_Using_Deep_Neural_Networks_on_High_Frequency_Data

## requirements to run every file:
jupyter notebook  
tensorflow 2.0+  
pandas, numpy, matplotlib, json, requests  
quandl, alpaca_trade_api (alternatively, you could just use alpaca -- we trained our model using quandl data (historic data), saved it, and tested it on more updated live data from alpaca) -- you will need a quandl and/or alpaca account and associated API keys in order to pull data  
