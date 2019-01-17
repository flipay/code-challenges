## Understanding Exchange Price Calculation

Let's talk about an exchange market knowledge. When we buy, it means someone is selling to us. When we want to calculate the price, we need to look at the prices others set in the market which is in "Order Book". Order Book consists of 2 sides, they are called "Bid" and "Ask". Bid side means the others are buying from us. And ask sides mean others are selling.

The buying (bid) and selling (ask) requests are called "Order". So if we want to buy Bitcoin (Input: USD, Output: BTC), we need to take a look at the Order on selling or ask side (order_book.asks)

For Example, we have these input to buy Bitcoin

```json
{
  "exchange_name": "coinbase_pro",
  "input_asset": "USD",
  "input_amount": 1000,
  "output_asset": "BTC"
}
```

And we get this data from Coinbase Pro

```json
{
  "bids": [
    ["4000", "10", "1"],
    ["3900", "1", "1"],
    ...
  ],
  "asks": [
    ["5000", "2", "1"],
    ["6000", "1", "1"],
    ...
  ]
}
```

Looking from the ask side, there will be several orders sorted from best to worse price. So we should pick order to check from the first one. From the [API documentation](https://docs.pro.coinbase.com/#get-product-order-book) `["5000", "2", "1"]` means there is 2 BTC selling at 5,000 USD/BTC. So if we buy BTC with 1,000 USD, we will receive 0.2 BTC.

```
Order 1 is selling 2 BTC @5,000USD/BTC

Buying BTC with 1,000 USD
--> Spent 1,000 USD to Order 1
--> Received 0.2 BTC
--> Average Price: 5,000 USD/BTC
```

In case you want to buy BTC with 13,000 USD, it will exceed the first order which has only 10,000 USD worth of BTC. So we need to take a look at the next ask order which is selling BTC at 6,000 USD/BTC. We can calculate by deducting first and second order. Which will give us 2 BTC (10,000 USD) + 0.5 BTC (3,000 USD) = 2.5 BTC.

```
Order 1 is selling 2 BTC @5,000USD/BTC
Order 2 is selling 1 BTC @6,000USD/BTC

Buying BTC with 13,000 USD
--> Spent 10,000 USD (2 x 5,000) to Order 1
--> Received 2 BTC
--> Spent 3,000 USD (0.5 x 6,000) to Order 2
--> Received 0.5 BTC
--> Average Price: 5,200 USD/BTC (13,000 / 2.5)
```
