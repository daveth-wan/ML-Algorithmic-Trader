ML Algorithmic Trader
A defensive, machine learning-based algorithmic trading strategy designed to navigate varying market regimes and overcome high transaction fees (0.3%). This project dynamically trades a diversified portfolio of U.S. technology equities (QQQ) and Gold (GLD) against a Thai Baht (THB) cash reserve. Instead of maximizing raw returns, the engine prioritizes capital preservation and risk-adjusted performance across volatile bull and bear markets.
Key Features:
Dual-Model Architecture: Utilizes Random Forest to map non-linear price movements in the Nasdaq-100 (QQQ) and XGBoost to detect multi-variable, inter-market patterns driving Gold (GLD).
Fee-Optimized Targets: Models are trained specifically to predict daily returns greater than the 0.3% transaction fee, ensuring they only act on high-conviction signals.
Hysteresis Logic (Hold Zone): Decouples entry and exit probability thresholds (e.g., 60% confidence to Buy, 40% to Sell) to eliminate "whipsawing" and prevent rapid capital drain from excessive trading in choppy markets.
Macro Trend Filtering: Implements a 50-day Simple Moving Average (SMA50) trend filter to provide the ML models with macroeconomic context, mathematically preventing the algorithm from trying to catch falling knives during market crashes.
Robust Feature Engineering: Incorporates asset-specific technical indicators (SMA, Rolling Volatility) alongside broader macroeconomic signals like the CBOE Volatility Index (VIX) and the 10-Year U.S. Treasury Yield (TNX).
Results
In backtesting, the strategy successfully acted as a capital-preservation engine. While it traded conservatively during choppy bull runs, it significantly outperformed a standard 50/50 Buy-and-Hold baseline during the 2022-2023 bear market across key risk-adjusted metrics, including vastly lower volatility, a higher Sharpe Ratio, and a significantly shallower Maximum Drawdown.
