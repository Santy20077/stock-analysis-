# stock-analysis
Here’s a professional and clean **README.md** for your project:


---

# 📈 Stock Analysis & Long-Term Investment Ranking

A quantitative stock analysis project that processes historical stock CSV data, performs statistical analysis, detects long-term trends, and ranks stocks based on a weighted investment scoring model.

This project focuses on identifying **high-quality long-term compounders** using CAGR, bull/bear cycles, and volatility regime analysis.

---

## 🚀 Project Overview

This script:

1. Loads multiple stock CSV files
2. Cleans and normalizes financial data
3. Computes yearly statistics
4. Detects growth trends and volatility regimes
5. Calculates CAGR (Compound Annual Growth Rate)
6. Scores and ranks stocks using a weighted quantitative model
7. Exports final ranking to CSV
8. Generates yearly price & volatility charts

---

## 📂 Project Structure

```
stock-analysis/
│
├── stock csv/                  # Folder containing raw historical CSV files
├── image/                      # Generated yearly charts
├── main.csv                    # Cleaned merged dataset
├── BEST STOCK RANKING.csv      # Final ranked stocks
└── stock_analysis.py           # Main script
```

---

## 📊 Key Features

### 1️⃣ Data Cleaning & Preprocessing

* Converts text volume values (K, M, B, T) into numeric format
* Cleans percentage values
* Handles missing values
* Converts date columns properly
* Merges multiple stock files into one unified dataset

---

### 2️⃣ Yearly Statistical Analysis

For each stock:

* Yearly Mean Price
* Yearly Volatility (Standard Deviation)
* Year-over-Year Growth %
* Lowest Performing Year
* Biggest Growth Year
* Biggest Drop Year
* Volatility Regime Change Detection
* Bull Run & Bear Run Length

---

### 3️⃣ CAGR Calculation

[
CAGR = \left(\frac{End}{Start}\right)^{\frac{1}{Years}} - 1
]

Used to measure long-term compounding performance.

---

### 4️⃣ Trend Detection Logic

The script identifies:

* Growth start year
* Sustained uptrend beginning
* Longest bull run
* Longest bear run
* Volatility regime shifts (3x volatility spike rule)

---

### 5️⃣ Quantitative Investment Scoring Model

Each stock receives a normalized score based on:

| Metric             | Weight |
| ------------------ | ------ |
| CAGR               | 50%    |
| Bull Run Strength  | 20%    |
| Bear Risk Penalty  | 20%    |
| Volatility Recency | 10%    |

Final Score:

```
Investment Score = 
0.5 * CAGR_score +
0.2 * Bull_score +
0.2 * Bear_score +
0.1 * Volatility_score
```

Stocks are then ranked from highest to lowest investment quality.

---

## 🏆 Example Output

Top ranked stocks:

```
===== Quality Long-Term Compounders =====

BJFN Historical Data
KTKM Historical Data
BRTI Historical Data
SUN Historical Data
AXBK Historical Data
```

Lowest ranked example:

```
COAL Historical Data
```

Final rankings are exported to:

```
BEST STOCK RANKING.csv
```

---

## 📈 Visualization

For each stock, the script generates:

* Yearly Mean Price line chart
* Yearly Volatility line chart

Saved to:

```
image/<stock_name>.png
```

---

## 🛠️ Technologies Used

* Python
* pandas
* numpy
* matplotlib
* seaborn
* statistics
* scikit-learn (prepared for modeling expansion)

---

## ▶️ How To Run

1. Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

2. Place stock CSV files inside:

```
stock csv/
```

3. Run:

```bash
python stock_analysis.py
```

---

## 📌 Data Requirements

Each CSV must contain:

* Date
* Price
* Open
* High
* Low
* Vol.
* Change %

---

## 🔎 Methodology Philosophy

This model is designed to identify:

* Strong long-term compounders
* Consistent growth stocks
* Low structural bear risk
* Recent stability in volatility

It favors **consistent long-term performers** over short-term speculative spikes.

---

## ⚠️ Disclaimer

This project is for educational and research purposes only.
It does not constitute financial advice.
Always conduct independent research before investing.

---

## 📬 Future Improvements

* Add Sharpe Ratio calculation
* Add Monte Carlo simulation
* Add risk-adjusted scoring
* Integrate portfolio optimization
* Deploy as web dashboard (Streamlit)

---

If you'd like, I can also create:

* 🔥 A more minimal GitHub-style README
* 📊 A portfolio-grade quant research README
* 🚀 A resume-ready project description
* 🌐 A Streamlit dashboard version
