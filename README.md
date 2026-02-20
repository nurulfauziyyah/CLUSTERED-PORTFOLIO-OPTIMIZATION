# 📊 Clustered Portfolio Optimization using MOEA/D

Multi-objective portfolio optimization on the SRI-KEHATI Index (2022–2024) using **MOEA/D**, **CVaR**, and **Sortino Ratio** with prior stock clustering.

---

## 🚀 Project Overview

This project implements a multi-objective evolutionary optimization framework to construct stock portfolios that balance:

- 📈 Expected Return (maximize)
- ⚠️ Conditional Value at Risk (CVaR, 95%) (minimize)
- 📉 Sortino Ratio (maximize)

Before optimization, stocks are grouped using **K-Means clustering** to improve portfolio structure.

The optimizer generates a **Pareto Front** representing trade-offs between return and downside risk.

---

## 🧠 Methodology

### 1️⃣ Data
- Index: SRI-KEHATI
- Period: 2022–2024
- Frequency: Daily returns

### 2️⃣ Preprocessing
- Return calculation
- Outlier handling & standardization (clustering features only)
- Stock grouping using K-Means

### 3️⃣ Optimization
Algorithm: **Multiobjective Evolutionary Algorithm based on Decomposition (MOEA/D)**

Objectives:
- Maximize: Expected Return
- Minimize: CVaR (95%)
- Maximize: Sortino Ratio


Output:
- Pareto-optimal portfolios
- Risk-return trade-off solutions
- Portfolio performance grouping

---

## 📈 Results Summary

| Portfolio | Expected Return | CVaR | Sortino |
|-----------|----------------|------|----------|
| Low       | -0.1116       | -0.0286 | -1.2895 |
| Medium    | 0.1403        | -0.0276 | 0.5965 |
| High      | 0.2337        | -0.0239 | 1.505 |

The **high-performance portfolio** achieves the best downside-risk-adjusted return.

---

## 🛠 Tech Stack

- Python
- NumPy
- Pandas
- Scikit-learn
- Evolutionary Optimization (MOEA/D implementation)

---
🔎 Key Contributions
- Integration of clustering + multi-objective optimization
- Explicit modeling of tail risk via CVaR
- Pareto-based portfolio selection
- Application in sustainable index context

📌 Future Improvements
- Compare with NSGA-II
- Add transaction cost modeling
- Extend to dynamic rebalancing
