
# 🧠 US LNG Trade Flow Optimization & Arbitrage Model (2019–2024, Python + LP)

## 📌 Project Summary  
This project builds a linear programming-based optimization model to **maximize export profitability** for **US LNG trade flows** across key global destinations including **UK, Japan, India, Spain, France, and South Korea**. It combines **real trade data (2019–2024)** with estimated shipping costs and synthetic route constraints to simulate **freight arbitrage and optimal allocation decisions**.

---

## 🎯 Objective  
> Maximize total export profit from the US Gulf by optimizing LNG shipment volumes across key routes, using a **Linear Programming (LP)** approach.

---

## 📊 Data Sources & Assumptions  

| Data Element                     | Source/Type                              | Notes                                                                 |
|----------------------------------|------------------------------------------|-----------------------------------------------------------------------|
| US LNG Export Volumes            | EIA / DOE                                | Monthly volume by destination (in MMcf)                               |
| US LNG Export Prices             | EIA / DOE                                | Monthly destination-wise price ($/Mcf)                                |
| Shipping Costs (per KT)         | Estimated (Public Freight Index + Routing) | Approximate average cost per country from US Gulf (manual entry)     |
| Route Capacity (Max KT)         | Synthetic                                 | Assumed based on port-level throughput estimates                      |
| Conversion Factors              | Approximate (1 KT ≈ 50.5 Mcf)             | Used for cost, volume, and revenue normalization                      |

---

## ⚙️ Tools & Libraries Used
- **Python (Pandas, NumPy)**
- **PuLP (Linear Programming)**
- **Seaborn + Matplotlib** (Data Visualization)
- **Jupyter Notebook** (Interactive Modeling)

---

## 🧮 Model Highlights
- **Objective Function**: Maximize profit = (Export price – Shipping cost) × Volume  
- **Constraints**:
  - Max capacity per route
  - Total US LNG export limit (220 KT assumed)
- **Scenario Simulation**:
  - UK price drop  
  - France price surge  
  - Capacity constraint shifts  
  - Observed freight arbitrage behavior

---

## 📈 Key Insights
1. **France emerges as a dominant high-profit route**, even outperforming Japan in some scenarios.
2. **UK's import volume is relatively insensitive** to minor price drops—freight cost efficiency sustains its allocation.
3. **Shipping cost is a primary arbitrage driver** — small cost differences lead to large volume shifts.
4. **South Korea and Japan** become suboptimal routes when European prices are competitive.
5. **The model reacts dynamically to small price shocks**, showing realistic shifts in trade flows.
6. **Linear Programming enables fast rebalancing** — helping energy firms simulate policy, pricing, or infrastructure changes.

---

## 📌 How to Use
1. Load the notebook in **Jupyter** or **nbviewer**  
2. Ensure you have the `PuLP`, `pandas`, `matplotlib`, and `seaborn` libraries  
3. Replace or extend with your own trade price or freight assumptions  
4. Modify `routes` or run new `scenarioX` blocks to simulate other shocks

---

## 📬 Contact / Collaboration  
If you're a recruiter, energy quant, or hiring manager — feel free to connect:  
**📧 Email:** mohitkr.h@gmail.com  
**🔗 GitHub:** [@mohit-kumar-3Q](https://github.com/mohit-kumar-3Q)
