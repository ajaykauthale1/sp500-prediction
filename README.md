# S&P 500 Direction Prediction

A machine-learning experiment that predicts whether the S&P 500 (`^GSPC`) will close higher the next day, using its full price history.

## Approach
1. Download the entire index history with `yfinance`
2. Build a binary target (tomorrow's close > today's close)
3. Train a `RandomForestClassifier` and evaluate it with precision score
4. Add rolling-horizon features (close-price ratios over several lookback windows)
5. Backtest with walk-forward training to avoid look-ahead bias

## Tech
Python, pandas, scikit-learn, yfinance, Jupyter.

## Run
```bash
pip install pandas scikit-learn yfinance jupyter
jupyter notebook s_and_p500.ipynb
```
