# Stock Price Prediction Neural Network

This repository contains code for a neural network designed to predict stock prices based on historical price data. It consists of two files:

- `py_stock_price_pred.py`: A Python script containing the implementation of the neural network.
- `jup_stock_price_pred.ipynb`: A Jupyter Notebook file with the same code for interactive exploration.

## Getting Started :zap:

To run the code, follow these steps:

1. Clone this repository to your local machine.
2. Install the required dependencies.
3. Open and execute either `py_stock_price_pred.py` or `jup_stock_price_pred.ipynb` in your preferred environment!

## Usage :chart_with_upwards_trend:

Once the code is executed, it will fetch historical stock data from Yahoo Finance, preprocess it, train the neural network, and make predictions. You can customize the parameters in the code to experiment with different configurations.

## Dependencies :computer:

The following dependencies are required to run the code:

- `yahoo_fin`: For fetching historical stock data from Yahoo Finance.
- `scikit-learn`: For data preprocessing.
- `Keras`: For building and training the neural network.
- `numpy`: For computations.
- `matplotlib`: For data visualization.

`pip install` these if needed!

## Model :brain:

### Loss & Optimization
- Loss Function: Mean Squared Error (MSE)
- Optimizer: Adam


### Parameters
For each day in one year, the model takes the adjusted close price of the desired stock for the previous N days as input, where N is an integer defined by the user.

### Predicts
It predicts the price of the stock M days into the future, where M is an integer defined by the user.

### Structure
The neural network architecture consists of the following layers:

- LSTM Layer of 64 nodes
- Dropout (20%)
- LSTM Layer of 128 nodes
- Dropout (20%)
- Dense layer of 32 nodes
- Dense layer of 16 nodes
- Dense layer of 1 node (output; compared to ground truth)


## Next Steps :rocket:
Excited to...
- **Utilize More Price Information**: Incorporate additional data from Yahoo Finance, such as open prices and trading volume, to improve the model's accuracy and robustness.
- **Consider Earnings and Dividend Dates**: Take into account earnings and dividend dates as factors that could influence stock prices, possibly incorporating them as additional features (maybe as a binary feature... 1 if within a week of earning and 0 if not).
- **Implement Stock Sentiment Analysis**: Develop a web scraper for Bloomberg/X stock news/opinion pieces to gather sentiment data related to the stock, and integrate it into the prediction model for more informed decision-making (again, possibly as a binary feature).

