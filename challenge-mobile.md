# Flipay Mobile Code Challenge

We believe one of the best ways to understand the engineering team fit is to see the solution and thought process on the problem. Please develop the solution with **iOS or Android** platform and send us the link to your repository to career@flipay.co

## Challenge

### Context

We think that existing cryptocurrency trading platforms are too complicated. A lot of people want to hold Bitcoin but they don't understand how to use those exchanges. **They just want Bitcoin.**

Currently, users need to know complex things in order to buy Bitcoin which bid, offer and orderbook concepts are the big parts of those complexities.  

Our idea is to hide those complexities and allow users to buy Bitcoin by just specifying the amount they want to buy.

### Scope of the test

<img align="right" width="275" height="537" src="./images/mobile-mockup-screen.png">

The scope of the challenge is to build a 1-screen mobile application that can determine the rate of buying Bitcoin from the Coinbase Pro cryptocurrency exchange by using its Restful API.

As you can see from the design, users just need to put the amount they want to buy in USD and then they should be able to see the cryptocurrency amount they gonna get if they press the Buy button.

Users won't be able specify the output amount by themselves, we think that it will add more complexity. 

The output and price should be updated every 5 seconds.

The Buy button doesn't have to work for now.

**More Details**

The application is expected to receive "Buy Amount" in USD from users.  

And expect to display these output,

1. Output Amount (in BTC)
2. Average Price (USD/BTC)

More detail, this is the first screen of the whole application. Later on, users will be able to sell Bitcoin which are not in the scope of this challenge and we don't have the plan to add more kinds of cryptocurrencies in the near future (3 years). 

### How to calculate Average Price?

The "Average Price" in the output will be determined by the ratio of input and output amount in USD. In the case of `BTC-USD`, it will be the number of `USD amount / BTC amount`. And the output amount will be determined by active orders in the order book.

Note that "Average Price" can vary depends on how much "Input Amount" users give.

Don't worry if this confused you, you can take a look at our explanation in [Understanding exchange price calculation](./docs/understanding-exchange-price.md).

### Resources

See [Coinbase Pro documentation](https://docs.pro.coinbase.com) for integration reference. Look at [Product Order Book](https://docs.pro.coinbase.com/#get-product-order-book) section for the market order data.

## Our Expectation

We expect to see the maintainable code which works correctly. We have no development time requirement, so you can take a reasonable time to work on this challenge to show us your capability.

And we value these principles in the development.

**• Security.** To build trust in the product, security is the most important aspect. A financial company can go out of business in a single attack.  
**• Simplicity.** It is easy to build complex things. We should strive for simplicity so that we can maintain the speed of change.  
**• Clarity.** In the team collaboration, we rarely have the same context in communication. Writing code with a clear objective and good readability help team effectiveness.  
**• Reliability.** What can go wrong, will go wrong. But not with the system which has been through the well-thought process of risk and error management.
**• Product.** Engineers are not coders, they should be able to see a big picture of the products. They should understand why users need it and what is the reason behind each feature.

**Extra points** for developers who have design skill, you can show it by adjusting the design as you see fit.  

Certainly, we never expected anything to be perfect, we need to be fast to maximize the learning to be able to maximize the values we can deliver to the world. And feel free to be creative on the solution as long as it satisfies the objective of the application.

For any questions, feel free to discuss in Github issue section, or send us the email at career@flipay.co
