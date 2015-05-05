# Robinhood NodeJS

NodeJS Framework to make trades with the private Robinhood API. Using this API is not encouraged, since it's not officially available. See this [blog post by @Rohanpai](https://medium.com/@rohanpai25/reversing-robinhood-free-accessible-automated-stock-trading-f40fba1e7d8b) for more information on the API.

> This framework is inspired on the [Python framework](https://github.com/rohanpai/Robinhood) by [@Rohanpai](https://github.com/rohanpai).

## Features

* Placing buy orders (Robinhood.place_buy_order)
* Placing sell order (Robinhood.place_sell_order)
* Quote Information (Robinhood.quote_data)
* _More coming soon..._

## Installation

```bash
npm install --save robinhood
```

## Usage

```js
var Robinhood = require('robinhood');

// Initialize
var trader = Robinhood({
  username: 'user',
  password: 'pass'
});

trader.quote_data('GOOG', function(err, httpResponse, body){
  if(err){
    console.error(err);
    return;
  }
  console.log('Quote data:', body);
});
```

------------------
This framework is still in a very alpha version and will likely change, so production usage is completely discouraged.