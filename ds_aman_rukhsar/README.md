# Trading Behavior vs Market Sentiment Analysis

## Project Overview

This project analyzes the relationship between cryptocurrency trading behavior and market sentiment using real-world data from Hyperliquid traders and the Fear & Greed Index. The analysis covers 211,218 transactions from 32 traders across 246 different cryptocurrencies over a 2-year period (May 2023 - May 2025).

## Research Question

How does market sentiment (Fear, Greed, Neutral, and their extremes) influence trader profitability, trading patterns, and decision-making in cryptocurrency markets?

## Data Sources

**Trading Data:**
- 211,224 transactions with execution prices, trade sizes, profit/loss data
- 32 unique trader accounts
- 246 different cryptocurrencies including BTC, ETH, SOL, HYPE, and others
- Timeframe: May 2023 to May 2025

**Sentiment Data:**
- 2,644 daily Fear & Greed Index records
- Classifications: Extreme Fear, Fear, Neutral, Greed, Extreme Greed
- Sentiment scores ranging from 0-100
- Timeframe: February 2018 to May 2025

## Key Findings

### 1. Extreme Greed Performs Best

Contrary to the popular trading wisdom of "buy fear, sell greed," the data reveals that traders actually achieve their highest profitability during periods of Extreme Greed. During these periods, traders maintained an 89.17% win rate with an average profit of $130.21 per trade, resulting in a profit factor of 11.02. This significantly outperforms all other sentiment categories.

### 2. Selling Strategy Outperforms Buying

The most profitable trading action is selling during Extreme Greed periods, which generates an average profit of $114.58 per trade. In contrast, buying during these same periods only yields $10.50 on average. This suggests that the optimal strategy involves accumulating positions during calmer periods and liquidating them when market sentiment reaches peak greed.

### 3. Fear is Still Profitable

While Extreme Greed leads in profitability, Fear periods also show strong performance with an 87.29% win rate and $112.63 average profit per trade. This indicates that traders who can overcome the emotional discomfort of fearful markets are rewarded with solid returns.

### 4. Time of Day Matters Significantly

Trading performance varies dramatically by time of day. The best trading hours are concentrated in the morning and around lunch (7am-1pm), with noon showing the highest average profit at $243.82. Late night trading (after 9pm) consistently underperforms, with 11pm being the worst hour at only $36.80 average profit.

### 5. Coin-Specific Sentiment Sensitivity

Different cryptocurrencies respond differently to market sentiment:

- **@107** is highly sentiment-dependent, generating $1.99 million in profits during Extreme Greed but losing $136,000 during Extreme Fear
- **HYPE** is the most reliable, remaining profitable across all sentiment conditions with $840,000 earned during Fear periods
- **ETH** performs well during Fear but turns negative during Extreme Greed
- **SOL and BTC** both show strong performance during Fear periods

### 6. Top Traders Share Common Patterns

The most successful traders maintain win rates above 80% and show a preference for trading during Fear and Greed periods rather than the extremes. One trader achieved a remarkable 99.12% win rate across nearly 10,000 trades, focusing primarily on Fear period trading.

### 7. Volume Correlates Negatively with Sentiment

Trading volume actually increases during Fear periods rather than Greed. The correlation between sentiment score and trading volume is -0.27, meaning traders are more active when the market is fearful. However, profitability peaks during Greed, creating an interesting disconnect between activity and returns.

### 8. Risk Varies by Sentiment

Extreme Fear periods show the highest volatility with a standard deviation of $1,628 in profit/loss, while Neutral periods are the safest with only $743 volatility. Interestingly, Extreme Greed offers a favorable risk-reward balance with high returns but only moderate volatility at $1,058.

## Strategic Implications

### For Active Traders

The data suggests a counter-intuitive but evidence-based approach:
- Focus trading activity during Extreme Greed periods when profit potential is highest
- Use Fear periods for strategic accumulation rather than aggressive trading
- Prioritize selling over buying when sentiment reaches peak Greed
- Trade primarily during morning hours (7am-1pm) and avoid late-night sessions
- Maintain position sizing discipline, especially during high-volatility Extreme Fear periods

### For Coin Selection

- Choose HYPE for stable, all-weather performance
- Trade BTC and SOL during Fear periods for reliable returns
- Use @107 exclusively during Greed and Extreme Greed phases
- Avoid ETH during Extreme Greed periods due to negative performance

### For Risk Management

- Target a minimum win rate of 80% as demonstrated by top performers
- Reduce position sizes during Extreme Fear due to elevated volatility
- Increase exposure during Extreme Greed given favorable risk-reward metrics
- Monitor time-of-day performance and adjust trading schedules accordingly

## Methodology

The analysis involved several key steps:

1. **Data Cleaning and Integration:** Merged trading data with sentiment data by date, achieving a 99.99% match rate with 211,218 successfully paired records

2. **Profitability Analysis:** Calculated win rates, average profit per trade, profit factors, and total profits across different sentiment categories

3. **Behavioral Pattern Recognition:** Analyzed buy versus sell performance, trading volume patterns, and time-of-day effects

4. **Coin-Specific Performance:** Evaluated how individual cryptocurrencies perform under different sentiment conditions

5. **Trader Profiling:** Identified characteristics and strategies of the most profitable traders

6. **Correlation Analysis:** Examined relationships between sentiment, volume, profitability, and trading activity

7. **Risk Assessment:** Measured volatility and maximum drawdown across different market conditions

## Limitations and Considerations

This analysis has several important limitations:

- The sample includes only 32 traders, which may not represent the broader market
- The 2-year timeframe covers limited market cycles
- Leverage data was not available, which could significantly impact profitability patterns
- Transaction costs and slippage are not fully accounted for in the profit calculations
- Survivorship bias may exist if unsuccessful traders left the platform

## Future Research Directions

Several areas merit further investigation:

- Impact of leverage on sentiment-based performance patterns
- Integration of macro-economic indicators like interest rates and inflation
- Machine learning models for sentiment prediction and trade timing
- Cross-market analysis to see if patterns hold in stocks, forex, or commodities
- Individual trader psychology and decision-making processes

## Technical Implementation

The analysis was conducted using Python with the following libraries:
- pandas for data manipulation and analysis
- numpy for numerical computations
- matplotlib and seaborn for data visualization
- Statistical methods for correlation and distribution analysis

All code is available in the Jupyter notebook included in this repository.

## Project Structure
```
ds_analysis/
├── notebook_1.ipynb                      # Complete analysis code
├── csv_files/
│   ├── summary_statistics.csv            # Aggregated metrics
│   └── merged_trader_sentiment_data.csv  # Full merged dataset
├── outputs/
│   ├── comprehensive_trading_analysis.png
│   ├── sentiment_trends_analysis.png
│   ├── trader_strategy_analysis.png
│   └── final_summary_dashboard.png
└── ds_report.pdf                         # Detailed written report
```

## Conclusion

This analysis challenges conventional trading wisdom by demonstrating that Extreme Greed periods offer the best risk-adjusted returns in cryptocurrency trading. The data reveals that successful trading is less about contrarian timing and more about recognizing when conditions align for profitable exits. The most effective strategy appears to be: prepare positions during Fear, execute sales during Extreme Greed, and maintain discipline around time-of-day and coin-specific patterns.

The finding that selling into Extreme Greed generates 11 times more profit than buying during the same conditions represents a fundamental insight for traders. Combined with the strong performance during Fear periods, this suggests a nuanced approach that neither blindly follows nor completely rejects market sentiment, but rather uses it strategically for timing entries and exits.
