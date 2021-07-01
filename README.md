# Idea
Finance is highly nonlinear and sometimes stock price data can even seem completely random. Traditional time series methods such as ARIMA ,SARIMA and GARCH models are effective only when the series is stationary, which is a restricting assumption that requires the series to be preprocessed by taking log returns (or other transforms). However, the main issue arises in implementing these models in a live trading system, as there is no guarantee of stationarity as new data is added.
This is combated by using Neural Networks(sequential models like LSTM,GRU etc.), which do not require any stationarity to be used. Furthermore, neural networks by nature are effective in finding the relationships between data and using it to predict (or classify) new data.

Machine learning and Deep Learning have found their place in the financial institutions for their power in predicting time series data with high degrees of accuracy and the research is still going on to make the models better.
Agenda of our project :
Data Acquisition
Firstly, we will perform web-scraping on NIFTY 50 wiki page for data collection. We will scrape the ticker symbols for all the companies listed in NIFTY 50 list .
Then we will use Quandl API to fetch stock data for past 7 years.

Label training data as 0(sell) and 1(buy)
Scale data using sklearn preprocessing library
Building Neural Network Model
Since it is a time series data and we will be creating sequences out of the data fetched, it is better to build LSTM model than a simple MLP.
