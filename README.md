# RSI-trading-bot
WHY?

This project was inspired by the recent happenings int he trading world and especially cryptocurrencies. Lets take an example of the recent worldcoin(WLD) which has taken everyone by storm where everyone wants to make quick money with it. The coin's price kept rising and the demand kept increasing and for traders their urge for involvement in the trading rises. Said trader will never be active all the time to monitor the prices and thus this is where automation trading is involved using the trading bot.


WHICH DATA TO USE?

The main data for trading crypto such a bitcoin is the previous prices and traded volume of asset  and such is available in the trading platform that we will link our bot for the next step whch is data preparation. Thus need for TA-lib which helps in analysis of the historical data and help bot predict future prices.


DATA PREPARATION

After obtaining the historical market data for the desired trading period including the price and volume data, we now establish a backtesting environment for the bot to compare and thus execute trades with reference to the past data.


MODELLING

The outcome of our trades are based on statistics and probabilities and thus we used RSI as our technical analysis indicator.


HOW?

The trading is done using the binance exchange platform as its basis as it does have the altcoin we are using as an example. Diving into specifics i'll be demonstrating the capabilities of the bot by specialising in one technical analysis indicator. The relative strength index(RSI) is an indicator that helps traders determine whether an asset "which in our case is crypto" mignt be overbought or oversold. This helps one determine potential entry and exit trading signals. The bot does the relative basics of rsi where it cslculates it, measures the momentum and potentially identify trading signals and trends reversals. First a time period is identified and in our case it is 14 days. next the average gains and losses within this time period are added up and devided agaisnt each other and the value becomes the relative strength. The value is plotted on a graph on a scale of 0-100 as this helps measure the momentum ie looking at the assets current value in comparisson with its past values. To identify potential trend changes there are two ranges of the indicator to check. Overbought and oversold. An entry signal can be triggered when an asset is oversold and its rsi goes above 30 in our case and an exit signal can be triggered when an asset is overbought ie its rsi goes below 70. The indicators can be used to spot potential trend reversals through a divergence. This is when an assets price moves one way and the rsi moves in the opposite direction. With our bot as an example it monitors the bullish divergence where an asset makes lowew lows but RSI makes higher lows thus a signal that downward momentum is occuring and a bullish reversal may follow and thus as per our bot instructions it will use the 30 mark as an entry point as it monitors the divergence using the 1m as in one minute interval. 


EVALUATION

Bots produce results depending on the strategies deployed and thus the higher risk strategies produce higher success rate bots. The next step for the bot involes adding more technical analysis indicators and algorithms so as  to improve its capabilities of analysing all outcomes and producing least risk results for the trader as all factors have been factored in.


DEPLOYMENT

Bot is not fully ready for deployment for use in real trading account due to some problems which will be listed below but on monitoring and maintenance of bot I have  to address any technical issues that may arise now as it is and later hwne i keep on adjusting strategies as the market conditions evolve and most importantly assess the bot's profitability as that is its main purpose make profit.


SETUP

I used the binance spot test network.
Created an API_KEY and API_SECRET code to link code to a specific account in the network 


PYTHON DEPENDECIES AND REQUIREMENTS

python-binance, TA-lib, websockets and websockets-client, numpy, json, pprint


USER CONFIGURATION

API_KEY - binance api key generated in the binance spot test network account.

API_SECRET - binance api key generated in the binance spot test network account.

RSI_PERIOD - is a momentum oscillator that measures the speed and change of price movements and in our case we used the default 14.

RSI_OVERBOUGHT - RSI is considered overbought when its range pases 70.

RSI_OVERSOLD - RSI is considered oversold when its range goes above 30.

TRADE_SYMBOL - this is the crypto asset we are monitoring and subjecting to our bot for analysis.

TRADE_QUANTITY - amount of crypto asset being bought or sold.


PROBLEMS ENCOUNTERED

Installation of TA-lib for windows users as even the main website for the python wrapper is down thus a new tool for analysing historical data needed.	


