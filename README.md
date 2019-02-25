To build an AMAZING AND WONDERFUL client to place a market order to buy and sell BitCoins

Coinbase is an electronic service and "wallet" for bitcoins and digital currency. Users can transfer currency, pay merchants, and make other payments instantly. The Coinbase API allows developers to access and integrate the functionality of Coinbase with other applications. Some example API methods include retrieving account information and balances, trading, sending money, requesting money, and managing user information.

General API Endpoint - https://coinbase.com/api/v1/
API Portal / Home Page - https://coinbase.com/api/doc

We will still be using legacy Coinbase API (v1) for learning purpose (Coinbase has New APi (v2) called Wallet API which we will not use for Mid-term). 

We are only concerned with exchange rates so we DO NOT execute buy and sell orders.  

The endpoint - https://coinbase.com/api/v1/currencies/exchange_rates is what you'll point your HTTP client to interact with data. Figure 1 shows the screenshot of their documentation.

Code uses REPL mode to execute the following commands.

•	BUY <amount>[currency]
Currency is optional. If a currency is provided (USD, EUR, etc.), the order will buy as many BTC as the <amount> provides at the current exchange rates. For example BUY 10 USD, display a message “Order to BUY 10 USD worth of BTC queued @ 613.45 BTC/USD (0.015897750831403948 BTC)”
Otherwise it will place an order to buy as many BTC as the <amount> and display a message “Order to BUY 10 BTC queued”
Currency is not valid. For example BUY 10 UCD. Display a message “No known exchange rate for BTC/UCD. Order failed”.
If <amount> is invalid. Display a message “No amount specified”. 

•	SELL <amount>[currency] 
Same rules apply as BUY

•	ORDERS – This command saves all current orders in a CSV format (use the same modules as market-research.js to generate CSV) as well as displays the current orders on console as follows. 
		 === CURRENT ORDERS ===
Wed Oct 05 2016 22:09:40 GMT+0000 (UTC) : BUY 10 : UNFILLED
