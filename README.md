# Customer Data Analysis


## Product 
***

This is a module in some financial investment startegies. Through analysing the trend of index, we can build some macro timing or portifolio adjustment signals.

![index_trend.png](https://raw.githubusercontent.com/litaotao/Spark-in-Finance-Quantitative-Investing/master/docs/index_trend.png)


### Screenshot

`similarity line and predict trend`

![similarity.png](https://raw.githubusercontent.com/litaotao/Spark-in-Finance-Quantitative-Investing/master/docs/similarity.png)

`prediction close index change percent`

![fitting.png](https://raw.githubusercontent.com/litaotao/Spark-in-Finance-Quantitative-Investing/master/docs/fitting.png)


## Architecture

Below is the brief indroduction:

- During the transaction time:
    - Spark cluster loads all the history data;
    - Dirver loads today's data;
    - Driver broadcasts today's data to the cluster;
    - Spark cluster parallelly calculates similarity data;
    - Dirver collects the calculation results;
    - Dirver parses the calculation results;

![architecture.png](https://raw.githubusercontent.com/litaotao/Spark-in-Finance-Quantitative-Investing/master/docs/architecture.png)


## Data Used

This application used several data bellow:

- Index minute bar in the previous several years;
- Index minute bar of today, refresh every one minute;

## Algorithms 

Just for the demo, I used the basic similarity algorithm.

## Value of Product

This application is a module in some quantitative funds, it can be used in macro timing and portfolio rebalancing.

For the future, there are endless imaging and extension space. For example, as the data growing more and more, we can put more data in the algorithm, and design several different algorithms to do the prediction parallelly, leverage the power of big data and Spark, completing a calculation round within 1 second, build high-frequency signals in the market. Which will be a revolution in the financial market.

I currently use a more complex algorithm do calculate the similarity and build macro signals in my private investment account, it really works, and I believe it will do much better in the future.


## Improvement

- More data:
    - Using more history data
    - Using more kinds data
        - price
        - volume
        - money flow
- Signals
    - Macro timing
    - Portfolio rebalance
    - Ticker timing
    - Ticker pair trading strategy
- Larger cluster



