# Foreign Exchange Risk Modelling with GARCH and Value-at-Risk

This project develops and evaluates a quantitative framework for modelling volatility and market risk across EUR/USD, EUR/GBP and EUR/CHF.

## Research Objective

The analysis examines whether different GARCH-family specifications provide reliable Value-at-Risk estimates across currency pairs with distinct volatility dynamics and during periods of market stress.

## Methodology

The project compares:

- GARCH(1,1)
- EGARCH(1,1)
- GJR-GARCH(1,1)

Each model is estimated with Gaussian, Student-t and skewed-t innovations.

Rolling 95% and 99% Value-at-Risk forecasts are evaluated using:

- Kupiec unconditional coverage test
- Christoffersen independence test
- Dynamic Quantile test

## Analysis Pipeline

1. Download and clean foreign-exchange market data
2. Calculate log returns and descriptive statistics
3. Estimate conditional volatility using GARCH-family models
4. Generate rolling VaR forecasts
5. Compare observed violations with expected loss frequencies
6. Validate model performance using statistical backtests
7. Examine model behaviour during major market disruptions

## Key Findings

The results demonstrate that VaR performance depends on the selected volatility specification, innovation distribution and currency pair. The comparison highlights the importance of evaluating both violation frequency and temporal independence instead of selecting risk models using a single accuracy measure.

The analysis also examines model behaviour around major market disruptions, including the January 2015 EUR/CHF shock and the 2022 EUR/GBP volatility spike.

## Technologies

Python, Pandas, NumPy, Matplotlib, yfinance, ARCH, statsmodels, time-series analysis, volatility modelling, Value-at-Risk and statistical backtesting.

## Repository Contents

- `fx_risk_garch_var_backtesting.ipynb` - complete data preparation, modelling, forecasting and backtesting workflow
- `figures/` - selected volatility and VaR visualisations
- `requirements.txt` - Python dependencies required to reproduce the analysis

## Data Source

Historical foreign-exchange data were obtained through Yahoo Finance. The notebook retrieves the data programmatically; raw market data are not redistributed in this repository.

## Reproducibility

Install the required packages:

```bash
pip install -r requirements.txt
```

Then open and run:

```bash
jupyter notebook fx_risk_garch_var_backtesting.ipynb
```

## Author

Anna Belous  
MSc Data Science, University of Vienna  
[LinkedIn](YOUR_LINKEDIN_URL) | [ORCID](https://orcid.org/0009-0002-7662-9297)
