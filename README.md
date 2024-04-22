# Options Straddle Trader

The inspiration for this project was inspired by a report made by Barclays.

https://www.scribd.com/document/521690968/Barclays-US-Equity-Derivatives-Strategy-Impact-of-Retail-Options-Trading

An option straddle buying or selling a call and put at the money option. If we predict that volatility may significantly increase it might make sense to buy the straddle. Otherwise, it may make sense to sell it. 
In this project, I was trying to predict whether to buy or sell straddles of Apple. To do this, I used important features related to each options contract such as implied volatility, date until expiration, and call to put volume ratio. 
However, most importantly, I was using a rolling window of historical volatility from other stocks in the tech sector to act as a signal for predicting the volatility of the Apple stock. 

To do this, I passed the contract features into a dense layer and the volatilities into an LSTM layer. Eventually the output oof both of these layers would be passed into a final dense layer. The labels were simple 1 or 0 (1 representing buy).
The labels were determined by seeing if buying a straddle generated a profit for a certain contract. 

# Model Architecture 

![image](https://github.com/Collin-G/barclays_modified/assets/118686914/02155b39-d67b-4daf-9f12-9b833138e2bb)
