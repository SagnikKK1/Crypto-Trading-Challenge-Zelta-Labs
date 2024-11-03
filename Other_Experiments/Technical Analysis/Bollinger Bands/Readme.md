# What are Bollinger Bands?
Bollinger Bands are a set of lines plotted two standard deviations (positively and negatively) away from a simple moving average (SMA) of a financial instrument's price. They were developed by John Bollinger in the 1980s and are used to identify overbought and oversold conditions, gauge volatility, and spot potential price reversals.

## Components of Bollinger Bands
- **Middle Band (SMA)**: This is a simple moving average, usually set to 20 periods.
- **Upper Band**: This is the SMA plus two standard deviations.
-**Lower Band**: This is the SMA minus two standard deviations.
## Formula
The Bollinger Bands are calculated using the following formulas:

### Middle Band (MB):

𝑀𝐵 = 𝑆𝑀𝐴𝑛
where n is the number of periods (commonly 20).

### Upper Band (UB):
𝑈𝐵 =𝑀𝐵 + ( 𝐾 × 𝜎 )
where K is the number of standard deviations (commonly 2), and σ is the standard deviation over the same period as the SMA.

### Lower Band (LB):
𝐿𝐵 = 𝑀𝐵 − ( 𝐾 × 𝜎 )
where K is the number of standard deviations (commonly 2), and σ is the standard deviation over the same period as the SMA.
## Interpretation
- **Volatility**: The width of the bands increases with volatility and decreases during less volatile periods. When the bands are narrow, it indicates low volatility, and when they are wide, it indicates high volatility.
Overbought/Oversold Conditions: Prices near the upper band can indicate an overbought condition, while prices near the lower band can indicate an oversold condition.
- **Trend Reversals**: If prices break above the upper band or below the lower band, it may signal a trend continuation or reversal, depending on the context.
Usage
- **Identifying Breakouts**: When the price moves significantly and breaks through the upper or lower band, it can indicate a strong continuation of the trend. Traders may use this signal to enter trades in the direction of the breakout.
Mean Reversion Strategy: Since prices often revert to the mean (the SMA), traders might sell when the price touches the upper band and buy when it touches the lower band.
- **Band Squeeze**: When the bands are very close together, it often precedes a significant price move. This is known as the "Bollinger Band Squeeze."
- **Use for Bitcoin**:Cryptocurrencies exhibit significant price fluctuations, making Bollinger Bands an effective tool for traders to assess market conditions, predict potential price movements, and make informed trading decisions.
## Results
### Buy Signal Results
- **count**  :  39.000000 ( 39 Buy Signals )
- **mean**   :  -0.024343
- **std**    :   0.035035
- **min**    :  -0.140916
- **25%**    :  -0.030156
- **50%**    :  -0.013077
- **75%**    :  -0.002909
- **max**    :   0.019071 ( maximum profit of 19% )
### Sell Signal Results
- **count**  :  95.000000 ( 95 Sell signals )
- **mean**   :   0.056767
- **std**    :   0.056607
- **min**    :  -0.108787
- **25%**    :   0.025376
- **50%**    :   0.044005
- **75%**    :   0.087266
- **max**    :   0.371869 ( maximum profit of 37% )
