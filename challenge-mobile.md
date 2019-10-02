# Flipay Mobile Code Challenge

We believe one of the best ways to understand the engineering team fit is to see the solution and thought process on the problem. Please develop the solution with **iOS or Android** pltform and send us the link to your repository to career@flipay.co

## Challenge

### Context

<img align="right" width="275" height="537" src="./images/mobile-mockup-screen.png">

You got into the team which is building the cryptocurrency exchange platform for users. The users can use the platform to buy and sell cryptocurrency through any existing exchanges.

The team had and idea to display users the expected output of buying and selling before submitting the order as in the mockup image.   


### Requirements

The scope of the challenge is to build the simple mobile application that can determine the rate of buying and selling from the Coinbase Pro cryptocurrency exchange. And the new exchanges can be added later on.


**User Story**

> As a casual investor,  
>
> I want to see the average price and expected amount of cryptocurrency I am buying.
>
> So that I can make a decision on buying and selling better by seeing these information instead of not knowing result on the usual market order.

**More Details**

The application is expected to receive "Input Amount" in USD from users.  

And expect to display these output,

1. Output amount (in BTC)
2. Average price (USD/BTC)


Please note that in the future, the users will also be able to change the input currency, output currency and exchange.


### How to calculate Average Price?

The "Average Price" in the output will be determined by the ratio of input and output amount in USD. In the case of `BTC-USD`, it will be the number of `USD amount / BTC amount`. And the output amount will be determined by active orders in the order book.

Note that "Average Price" can vary depends on how much "Input Amount" users give.

Don't worry if this confused you, you can take a look at our explanation in [Understanding exchange price calculation](./docs/understanding-exchange-price.md).

### Resources

See [Coinbase Pro documentation](https://docs.pro.coinbase.com) for integration reference. Look at [Product Order Book](https://docs.pro.coinbase.com/#get-product-order-book) section for the market order data.

## Our Expectation

We expected to see the production-leveled code with proper testing. We have no development time requirement, so you can take a reasonable time to work on this challenge to show us your capability.

And we value these principles in the development.

**• Security.** To build trust in the product, security is the most important aspect. A financial company can go out of business in a single attack.  
**• Simplicity.** It is easy to build complex things. We should strive for simplicity so that we can maintain the speed of change.  
**• Clarity.** In the team collaboration, we rarely have the exact same context in the communication. Writing code with a clear objective and good readability help team effectiveness.  
**• Reliability.** What can go wrong, will go wrong. But not with the system which has been through the well-thought process of risk and error management.

Certainly, we never expected anything to be perfect, we need to be fast to maximize the learning to be able to maximize the values we can deliver to the world. And feel free to be creative on the solution as long as it satisfies the objective of the application.

For any questions, feel free to discuss in Github issue section, or send us the email at career@flipay.co
