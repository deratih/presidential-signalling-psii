# presidential-signalling-psii
Replication package for PSII and Machine Learning manuscript
# Presidential Signalling Intensity Index (PSII)

Replication package for the manuscript:

**"Presidential Signalling Intensity Index (PSII) and Machine Learning: 
A Novel Framework for Forecasting US Market Volatility"**

## Overview

This repository contains all data, code, and results necessary to reproduce 
the findings in the manuscript submitted to the *International Journal of 
Forecasting*.

The study constructs a Presidential Signalling Intensity Index (PSII) from 
75,866 communications by President Donald J. Trump on Twitter (2009-2021) and 
Truth Social (2022-2026). Sentiment is extracted using Twitter-RoBERTa. The 
index is used to forecast realized S&P 500 volatility and the VIX using 
LASSO, Random Forest, XGBoost, and LightGBM.

## Key findings

- LASSO with PSII reduces VIX forecast RMSE by 10% (DM statistic 10.53, p < 0.0001)
- The improvement grows from 2.1% (2024) to 20.1% (2026), t = 7.27, p < 0.0001
- Real PSII outperforms all 100 placebo shuffles
- No spillover to non-US markets: the signal is domestically US-specific

## Data sources

| Dataset | Source | Access |
|---------|--------|--------|
| Trump tweets | Kaggle Trump Twitter Archive | Public |
| Truth Social | CNN archive (ix.cnn.io) | Public |
| Market data | Yahoo Finance, FRED, CBOE | Public |
| EPU index | policyuncertainty.com | Public |

## Reproducing results

1. Clone this repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Run notebooks sequentially from `01_data_collection.ipynb` to 
   `06_figures_and_tables.ipynb`.

Total runtime: approximately 45 minutes on Google Colab with a Tesla T4 GPU.

## Software requirements

- Python 3.10 or higher
- See `requirements.txt` for full dependency list

Key packages:
- pandas, numpy
- scikit-learn, xgboost, lightgbm
- transformers, torch
- shap
- yfinance, pandas-datareader, fredapi

## License

MIT License. See `LICENSE` for details.

## Contact

For questions regarding the data or code, contact:

Dewi Ratih
State University of Surabaya
Email: dewiratih@unesa.ac.id
ORCID: 0000-0002-0951-6236

## Citation

If you use this dataset or code in your research, please cite:

Ratih, D., Susanti, & Ab Samad, N. H. (2026). Presidential Signalling 
Intensity Index (PSII) and Machine Learning: A Novel Framework for 
Forecasting US Market Volatility. Manuscript submitted to the 
*International Journal of Forecasting*.
