# Investments Project – FIN-405

This project was developed as part of the **FIN-405: Investments** course at EPFL.  
It focuses on constructing and evaluating international equity and currency strategies, analyzing diversification benefits, and designing fund portfolios with targeted risk levels.  

---

## Project Overview
The main goal is to understand how global diversification and systematic strategies (momentum, reversal, carry, and dollar exposure) impact portfolio performance for a U.S.-based investor. We use monthly data from 2002–2024 covering international equity indices, exchange rates, and U.S. Treasury bills.

**Key questions addressed:**
- How does international diversification improve risk-adjusted returns?  
- Can momentum, reversal, and currency-based strategies add value beyond diversification?  
- How do these strategies combine into an optimal fund portfolio with controlled volatility?  

---

##  Strategies Implemented

### 1. International Diversification (DIV)
- Convert local returns into USD.  
- Build **equally weighted**, **risk-parity**, and **mean-variance optimal** portfolios.  
- Assess benefits of diversification and currency hedging.  

### 2. Equity Index Momentum (MOM)
- Long-short portfolio: buy past winners, short past losers.  
- Statistically significant alpha, largely independent of DIV.  

### 3. Equity Index Long-Term Reversal (REV)
- Constructed from 5-year lagged cumulative returns.  
- Negative and statistically significant performance in our sample.  

### 4. Currency Carry (CARRY)
- Long high-interest-rate currencies, short low-interest-rate currencies.  
- Strong positive returns and high Sharpe ratio.  
- Uncorrelated with DIV → strong diversification benefits.  

### 5. Dollar Strategy (DOLLAR)
- Long USD against a basket of major currencies.  
- Underperformed DIV and delivered negative alpha.  

### 6. Optimal Fund Portfolio (STRAT & FUND)
- Combine DIV, T-Bills, and strategy overlays to target **15% volatility**.  
- Risk-parity combination of MOM, REV, CARRY, DOLLAR (STRAT).  
- Final **Fund Portfolio** achieved higher Sharpe ratio than DIV + T-Bills alone.  

---

## Performance & Risk Analysis
- Regression against **Fama–French Five Factors** shows near-zero betas.  
- Significant positive alpha (~6.4% annually).  
- Interpretation: returns compensate for exposure to **non-standard global risk factors** (momentum, reversal, carry), consistent with the **Arbitrage Pricing Theory (APT)**.  

---

## Data Sources
- **WRDS**: Monthly World Indices, CRSP U.S. equity returns, U.S. Treasury Bills.  
- **FRED**: Exchange rates and 3-month interbank rates.  
- **Data Cleaning**: linear interpolation for missing values, alignment across common dates.  

---

## Repository Contents
- `notebooks/` → Jupyter Notebooks with data import, cleaning, and strategy implementation.  
- `figures/` → Plots of portfolio performance and regression outputs.  
- `report/` → Final PDF report.  

---

## Authors
- Souhail Ed-dlimi  
- Khalil Ouazzani Chahdi  
- Imane Benkamoun  
- Yann Hirjy  

---

## License
This project is for **academic purposes only**.  
Not intended for financial advice or commercial use.  
