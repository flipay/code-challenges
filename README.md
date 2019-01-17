# Flipay Code Challenge

We believe one of the best ways to understand the engineering team fit is to see the solution and thought process on the problem.

Please develop the solution with **Elixir or NodeJS** and send us the link to your repository to review at career@flipay.co.

## Challenge

### Context

You got into the team which is building the cryptocurrency investment platform for users. The users can use the platform to buy and sell cryptocurrency through any existing exchanges.

The team got the idea to let user buy and sell at the best rate by selecting the exchange with the best rate at the time. And you took the challenge to develop this rate comparing system to plug to the existing system.

### Requirements

The scope of the challenge is to build the application or library to able to determine the rate of buying and selling at the time given a certain amount from the Coinbase Pro cryptocurrency exchange. Comparing rate is not in the scope. And it should be taken into consideration that new exchanges can be added later on.

The application will receive these input

1. Exchange name (will be only "coinbase_pro" for now)
2. Input asset
3. Input amount
4. Output asset

And expect to send the output

1. Price
2. Timestamp

The possible "Input-Output assets" are `BTC-USD`, `ETH-USD`, `XRP-USD`. And it can be reversed. Which means we have 6 combinations (3 pairs and reverse of 3 pairs) of input and output assets.

"Input Amount" will always be the same currency as "Input Asset". For example, a user wants to buy BTC using 1,000 USD. The input will be like this.

```json
{
  "exchange_name": "coinbase_pro",
  "input_asset": "USD",
  "input_amount": 1000,
  "output_asset": "BTC"
}
```

The "Price" will be determined by the rate in USD, which means for `BTC-USD`, it will be the number of `USD amount / BTC amount`.

Note that the reason we need "Input amount" is because the "Price" can vary depends on how much input amount users give.

### Resources

See [Coinbase Pro documentation](https://docs.pro.coinbase.com) for integration reference. Look at [Product Order Book](https://docs.pro.coinbase.com/#get-product-order-book) section for the market order data.

## Our Expectation

We expected to see the production-leveled code with proper testing. We have no development time requirement, so you can take a reasonable time to work on this challenge to show us your capability.

And we value these principles in the development.

**Security.** To build trust in the product, security is the most important aspect. A financial company can go out of business in a single attack.  
**Simplicity.** It is easy to build complex things. We should strive for simplicity so that we can maintain the speed of change.  
**Clarity.** In the team collaboration, we rarely have the exact same context in the communication. Writing code with a clear objective and good readability helps team effectiveness.  
**Reliability.** What can go wrong, will go wrong. But not with the system which has been through the well-thought process of risk and error management.

Certainly, we never expected anything to be perfect, we need to be fast to maximize the learning to be able to maximize the values we can deliver to the world. And feel free to be creative on the solution as long as it satisfies the objective of the application.

For any questions, feel free to discuss in Github issue section, or send us the email at career@flipay.co
