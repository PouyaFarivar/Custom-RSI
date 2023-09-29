# Custom-RSI
Custom RSI Indicator with long calculation ranges for BTC price action

The model can be used with other securities, commodities price actions, and different time bins. You would only have to change the ticker of the yfinance downloader to the ticker of your choice and re-run the entire cells.

This repository started as an attempt to use changes in the price from each day to be able to predict anything meaningful for the future.

The problem with the said goal is that the price action changes look like a normal distribution as shown in the notebook.

This meant that any attempt to find a strategy like buying after ’n’ red candles wouldn’t yield a positive expected value in the long run. this I shown in the RSI Notebook as an attempt to find the probability of getting a maximum red candle day in a row.

The Final attempt which turned into the Custom RSI indicator was to sum up the price changes of the underling in a moving average style, Which means summing up the price changes for different time bins consecutively to get the Custom RSI.

The final result is the 100-day sliding RSI which appears to be a good predictor of volatility in BTC price action. This means that it can be used to find tops or bottoms. As seen in the final graph local tops and bottoms in the underlying appear to happen at the peaks of the Custom RSI Indicator.

Overall the Custom RSI Indicator Can be used to find events of extreme volatility in the market. Meaning that a local peak in the 100-day sliding RSI Indicators indicates a local bottom or a top in the underlying. 

This can be used as a good measure for getting in and out of long-term positions in the underlying.

