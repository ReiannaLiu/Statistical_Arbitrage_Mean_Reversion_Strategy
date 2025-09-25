# Statistical_Arbitrage_Mean_Reversion_Strategy

## Project Title & Description
This project implements a **pairs trading strategy** by identifying pairs of securities with a stable long-term relationship. It uses:
- **Cointegration tests (Engle–Granger)** to detect equilibrium relationships.
- **Augmented Dickey–Fuller (ADF) tests** to confirm mean-reversion of the spread.

Trading signals are generated when the spread deviates significantly from its historical mean, with the expectation that it will revert.

---

## Dependencies & Requirements
Main Python packages required:
- `pandas`
- `numpy`
- `statsmodels`
- `scipy`
- `vectorbt` / `vectorbtpro`
- `matplotlib` (for visualization)
- `requests` (for scraping ticker data)

---

## Project Structure
The Jupyter Notebook follows this workflow:

1. **Data Loading**  
   - Fetches S&P 500 tickers and pulls historical price data from Yahoo Finance.

2. **Data Cleaning**  
   - Filters out incomplete series.

3. **Cointegration Test**  
   - Runs Engle–Granger tests on symbol pairs to identify candidates.

4. **ADF Mean-Reversion Test**  
   - Applies Augmented Dickey–Fuller test to check if the spread is stationary.

5. **Backtest Construction**  
   - Builds a long/short portfolio with signal generation and portfolio simulation.

6. **Results & Analysis**  
   - Reviews performance, checks mean-reversion behavior, and visualizes returns.

---

## How to Run
1. Clone or download this repository.
2. Install dependencies:
   ```bash
   pip install pandas numpy statsmodels scipy vectorbt matplotlib requests
   ```

3. Open the Jupyter Notebook:

   ```bash
   jupyter notebook pair_trading.ipynb
   ```
4. Run the cells in order.

---

## Results & Insights

* Certain pairs exhibited **cointegration and mean-reverting spreads**, validating the pairs trading approach.
* ADF tests confirmed mean-reversion for some candidate pairs.
* Backtests demonstrated potential profitability, though performance varied by parameter choice.

---

## Future Work

* Include **transaction costs and slippage** for more realistic backtests.
* Explore **dynamic hedge ratios** instead of fixed 1:1 trading.
* Extend to **multiple pairs** and portfolio-level optimization.
* Test alternative entry/exit rules (e.g., z-score thresholds, volatility filters).
* Apply **walk-forward validation** to assess robustness across market regimes.

