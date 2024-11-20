# Shane's Swing Trading Strategy

* Stocks have support levels
    * e.g. MSFT hits recent low of $400 on May 1st, then hits a similar low of $390 on Aug 5th
    * Stocks reaching support levels is a buying opportunity
* However, good stocks trend up
    * This means the support level of good stocks rise over time
    * Thus it's difficult to rely on historical price data to determine support levels
* To adjust for this, we calculate support levels not by historical price but rather historical difference between price and 200 SMA
    * 200 SMA is a good indicator for the general direction of a stock
    * The difference between the price and the 200 SMA then measures the residual of the price from its expected price
