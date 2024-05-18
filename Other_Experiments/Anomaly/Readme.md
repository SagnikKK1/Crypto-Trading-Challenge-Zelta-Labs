# Introduction
Anomaly detection, a fundamental concept in financial data analysis and trading strategies, plays a pivotal role in tading strategies. Anomalies, often indicative of irregularities or outliers in market behavior, serve as crucial signals for identifying potential trading opportunities. In this context, we leverage anomaly detection techniques to scrutinize historical Bitcoin price data, seeking deviations from expected patterns derived from moving averages (MA), relative strength index (RSI), and golden ratio bounds. By identifying anomalies, the code aims to capture market inefficiencies and capitalize on transient deviations from normal market behavior. This introduction sets the stage for understanding how anomaly detection is utilized within the code to drive trading decisions and enhance portfolio performance.

## Aspects that were considered
- **Anomaly Identification**:
Anomalies in the Bitcoin price data are identified by analyzing various factors, including moving averages (MA), relative strength index (RSI), and golden ratio bounds. These indicators are used to detect instances where the market behaves abnormally, potentially signaling favorable entry or exit points for trades.

- **Improved Anomaly Detection**:
The code implements an improved anomaly detection mechanism by combining multiple criteria to identify anomalies more accurately. For example, anomalies are detected when the Bitcoin price falls outside the bounds defined by the moving averages and the RSI exceeds a certain threshold, indicating overbought or oversold conditions.

- **Trade Triggering**:
Detected anomalies serve as triggers for executing trades in the trading strategy. When an anomaly is detected, the code evaluates whether to initiate a trade based on predefined conditions, such as the presence of an open position and the cool-off period since the last trade. If the conditions are met, the code executes a buy order to enter a new position in the market.

- **Risk Management**:
Anomaly detection also plays a role in risk management within the trading strategy. For instance, the code dynamically adjusts the trade size based on rolling historical volatility, ensuring that trade sizes are proportional to market conditions. Additionally, the code implements a trailing stop-loss mechanism to limit potential losses in case anomalies persist or worsen after a trade is initiated.

- **Performance Evaluation**:
The effectiveness of anomaly detection is evaluated based on the performance of the trading strategy, as reflected in key metrics such as portfolio returns, maximum drawdown, and risk-adjusted ratios like the Sharpe and Sortino ratios. By analyzing the trade history and performance metrics, users can assess the robustness of the anomaly detection mechanism and its impact on overall strategy performance.
## Results
- Initial Portfolio Value : **100$**
- Final Portfolio Value: **42513.75$**

We assumed 0.2% cost of slippage and transactions.
### Some more metrics about our strategy returns
- count    138.000000 ( A total of 138 trades were executed)
- mean       0.054831
- std        0.142640
- min       -0.050000
- 25%       -0.032844
- 50%        0.002389
- 75%        0.074824
- max        0.775420 ( Maximum return was 77% )
