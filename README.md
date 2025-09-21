# Financial Forecasting of Gold Returns using Global Uncertainty (1999–2024)

## 🎯 Objective
Forecast monthly **gold returns** using global uncertainty indicators — **GEPU** and **WUI** — and compare traditional econometrics with **machine learning** models.

> This work is based on my MSc module *Predictive Analysis for Decision-Making* and its empirical report, which details methods, diagnostics, and results. See `reports/PADM_Empirical_Report_CourseWork2.pdf`. :contentReference[oaicite:0]{index=0}

## 🧠 Methods
- **Econometrics:** OLS baseline (with Newey–West SEs), lag structures, sub-sample analysis (pre-2008 vs post-2008).
- **Machine Learning:** Linear Regression (ML API), **SVR**, **Random Forest**, **Gradient Boosting** with time-aware 80/20 split (train ≈1999–2019, test ≈2020–2024). :contentReference[oaicite:1]{index=1}
- **Targets & Features:**
  - Target: monthly log return of gold
  - Features: GEPU, WUI (levels and lags), engineered from CSVs in `data/`.

## 📊 Key Findings (summary)
- Linear relationships are weak/inconsistent; **non-linear tree ensembles** predict better.  
- Post-2008 period shows **stronger sensitivity** of gold to policy uncertainty.  
- Indicative test performance (your report): **Gradient Boosting best** among ML models. :contentReference[oaicite:2]{index=2}

> See performance tables, residual diagnostics, feature importance, and stability checks inside the report and notebook. :contentReference[oaicite:3]{index=3}

## 🗂️ Repository Contents
- `notebooks/Forecasting_Gold_Returns.ipynb` — end-to-end workflow (EDA → OLS → ML → diagnostics).
- `data/gold_uncertainty_dataset_monthly.csv` — aligned monthly panel (gold, GEPU, WUI).
- `data/gold_uncertainty_dataset_lagged.csv` — prebuilt lag features (repro convenience).
- `reports/PADM_Empirical_Report_CourseWork2.pdf` — full write-up. :contentReference[oaicite:4]{index=4}
- `src/features.py` — (optional) helpers to build lags and train/test splits.
- `requirements.txt` — Python dependencies.

## Data Source: Bloomberg Education
