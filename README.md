# Shane's Swing Trading Strategy

## WINRATE (11/20 - 12/4): 16W/3L (84%)

Generally, stocks have support levels, which signify that a stock is unlikely to go below a certain point. When a stock reaches a supposed support level, that would signify a buying opportunity. Here is a year graph of PG, with the potential support levels underlined in red (source: Robinhood).

![Alt text](/images/PG%20support%20lines.png?raw=true "Optional Title")

However, good stocks also tend to go up over time. Naturally, its support levels would also go up; it's illogical for a stock to have the same support levels as it did when it was trading for half the price. Here's a year graph of JPM, where it's easy to see that the potential support levels slowly move up over time.

![Alt text](/images/JPM%20support%20lines.png?raw=true "Optional Title")

If we want to utilize support levels to signify buying opportunities, we need to adjust for the shifting of support levels over time. To do this, we can use the 200-Day SMA (Simple Moving Average), which is a good indicator for measuring the overall trend of a stock as short-term volatility has little impact on the 200-Day SMA. If we take the difference between the current price of a stock and its 200-Day SMA, then we remove the long-term trend from the equation and are just left with the short-term price changes.

Here's the same graph of JPM, except where the differences between the price and the 200-Day SMA at the various support levels are indicated with red lines.

![Alt text](/images/JPM%20200%20SMA.png?raw=true "Optional Title")

Note that these red lines are roughly around the same length; this means that there are support levels that prevent stocks from dropping too far below "where they are expected to be based on the long-term trend."

Here is another example with NVDA.

![Alt text](/images/NVDA%20200%20SMA.png?raw=true "Optional Title")

Now, this consistency isn't present in all stocks, so here are some steps I take to identity these stocks. Note that some of the numerical criteria are unspecificed; I am still deciding the proper levels.

1. Reduce my search to the S&P 500. I only want to trade in highly liquid, reliable environments, so that generally means choosing high market-cap stocks.
2. Select stocks whose 200-Day SMA graphs have a decently positive slope (at the current day, meaning at the far right of the graph). We only want to select stocks that are trending upwards, otherwise we risk trying to "catch a falling knife", so to speak.
3. Calculate the difference between the closing price and the 200-Day SMA for the last 200 days. We denote this value as $D$.
4. Identify some number of "troughs" (I choose 7) in the graph of $D$. I define a trough as a low point in this graph that isn't close to any other troughs, where "closeness" is defined as being within 5 business/market days. Think of troughs as downwards spikes, rather than flat lows.
5. Calculate the standard deviation of these troughs and compare it to some threshold to see if the troughs are consistent. Only continue if they are consistent.
6. And lastly, check that $D$ for the current day is less than the mean of the troughs. This means that we are currently at a support level.

If all of these criteria are met, then this is a buying opportunity. Buy and look to sell when the underlying goes up or down 3-5% to take profit but to also avoid losing too much to falling knives. It's best to run this algorithm once a day, late enough where the markets aren't as volatile but early enough so that theres still enough time in the day to reap upward movement from reversals. I like doing my trades at 1 P.M. EST.

I will update this page later with the results of my paper trading with this algorithm.
