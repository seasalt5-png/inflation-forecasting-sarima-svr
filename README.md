# 📈 Inflation Forecasting — SARIMA vs SVR
**Monthly Inflation Rate Forecasting for Bandar Lampung City (2006–2025)**

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-F9AB00?logo=googlecolab&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

This project compares the performance of **SARIMA** (Seasonal Autoregressive Integrated Moving Average) and **SVR** (Support Vector Regression) for forecasting monthly inflation rates in Bandar Lampung City, using data sourced from BPS (Badan Pusat Statistik) Lampung Province.

> Final project — Data Science Program, Institut Teknologi Sumatera (ITERA) · 2026

---

## 📁 Project Structure

```
inflation-forecasting-sarima-svr/
├── sarima_svr_inflation.ipynb              # Main notebook (full pipeline)
├── dataset/
│   ├── inflation_2006.csv                  # Raw yearly CSV files from BPS
│   ├── inflation_2007.csv
│   ├── ...
│   └── inflation_bandar_lampung_2006_2025.csv  # Merged master dataset (auto-generated)
├── outputs/
│   ├── inflation_trend_bandar_lampung.png  # Time series visualization
│   ├── acf_pacf_plot.png                   # ACF and PACF plots
│   ├── sarima_diagnostics.png              # SARIMA residual diagnostics
│   ├── sarima_forecast.png                 # SARIMA actual vs predicted
│   ├── svr_forecast.png                    # SVR actual vs predicted
│   └── sarima_vs_svr_comparison.png        # Side-by-side comparison plot
└── README.md
```

---

## 🔬 Methodology

| Stage | Details |
|---|---|
| **Data source** | Monthly inflation rate, Bandar Lampung, 2006–2025 (BPS Lampung) |
| **Preprocessing** | Missing value interpolation · IQR-based outlier detection |
| **Stationarity test** | Augmented Dickey-Fuller (ADF) test · First-order differencing if needed |
| **SARIMA** | Order selection via ACF/PACF · Ljung-Box residual diagnostic · 95% confidence interval |
| **SVR** | RBF kernel · Lag features: lag 1, 2, 3, 12 (seasonal) · Grid Search (C, γ, ε) |
| **Evaluation metrics** | RMSE · MAE · MAPE with interpretation |
| **Train/test split** | 80% training · 20% testing (chronological) |

---

## 🔧 Requirements

Install required libraries with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
```

> The notebook is designed to run on **Google Colab**. No local environment setup is needed.

---

## 🚀 How to Run

1. Upload your raw dataset files to Google Drive at the following path:
   ```
   My Drive/Dataset/inflation_rate_bandar_lampung/
   ```

2. Open `sarima_svr_inflation.ipynb` in **Google Colab**

3. Run all cells from top to bottom:
   ```
   Runtime → Run all
   ```

4. All outputs (plots and merged CSV) will be automatically saved back to your Drive folder.

---

## 📊 Results

> Update this table after running the notebook with your actual values.

| Metric | SARIMA | SVR |
|---|---|---|
| RMSE | — | — |
| MAE | — | — |
| MAPE (%) | — | — |
| MAPE Interpretation | — | — |
| **Best Model** | — | — |

**MAPE Criteria (Lewis, 1982):**
- `< 10%` → Highly Accurate
- `10–20%` → Good Forecast
- `20–50%` → Reasonable Forecast
- `> 50%` → Inaccurate

---

## 📚 References

1. Rizki, M. I. & Taqiyyuddin, T. A. (2021) — *Penerapan Model SARIMA untuk Memprediksi Tingkat Inflasi di Indonesia*. Jurnal Sains Matematika dan Statistika, 7(2), 62–72.
2. Hendayanti, N. P. N. & Nurhidayati, M. (2020) — *Perbandingan Metode SARIMA dengan SVR dalam Memprediksi Jumlah Kunjungan Wisatawan Mancanegara ke Bali*. Jurnal Varian, 3(2), 149–162.
3. Isnaeni R., Sudarmin, S. & Rais, Z. (2022) — *Analisis SVR dengan Kernel RBF untuk Memprediksi Laju Inflasi di Indonesia*. VARIANSI, 4(1), 30–38.
4. Ruliana, R. et al. (2024) — *Implementation of the SVR Method in Inflation Prediction in Makassar City*. ARRUS Journal of Mathematics and Applied Science, 4(1), 28–35.
5. Ramadhan, G. L. et al. (2021) — *Peramalan Inflasi Indonesia dengan SARIMA*. Sistemasi, 10(3), 627–636.
6. Yahya, A. (2022) — *Peramalan IHK Indonesia Menggunakan Metode SARIMA*. Jurnal Gaussian, 11(2), 313–322.

---

*Made with ♥ by Sarah Wasti · Institut Teknologi Sumatera · 2026*
