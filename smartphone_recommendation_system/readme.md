# 📱 Smartphone Recommendation System: MCDA & TOPSIS Spatial Engine

An interactive, end-to-end Multi-Criteria Decision Analysis (MCDA) engine designed to solve the smartphone selection problem using TOPSIS (Technique for Order Preference by Similarity to Ideal Solution).

This project combines an offline Python ETL & Data Engineering Pipeline with a zero-latency, reactive Client-Side Web SPA hosted directly via GitHub Pages.

---

## 🔗 Quick Links

*   **🦅 Kaggle Notebook & Analysis** — Explore the full data engineering & MCDA pipeline on Kaggle.
*   **🌐 Live Web Application SPA** — Interactive browser-based TOPSIS decision solver.

---

## 🌟 Key Features

*   **Math-Driven Recommendations**: Replaces rigid SQL filters (`WHERE price <= X`) with $n$-dimensional Euclidean distance scoring ($C_i \in [0, 1]$).
*   **Non-Compensatory Gaming Thresholds**: Automatically filters out underpowered processors before ranking to prevent budget-bias in power-user profiles.
*   **Dynamic Model Deduplication**: Groups hardware variants (RAM/Storage/Color) to preserve ranking diversity.
*   **Client-Side Web SPA**: Executes the TOPSIS solver in < 5ms directly inside the browser using modern vanilla JavaScript and Tailwind CSS.
*   **Visual Analytics**: Real-time Chart.js interactive visualizations, including:
    *   TOPSIS Spatial Positioning Boundaries ($S_i^+$ vs $S_i^-$).
    *   Pareto Efficient Frontiers (Price vs. Performance).
    *   Multi-Profile Morphological Radar Charts.

---

## 📂 Repository Structure

```text
kaggle_work/
└── smartphone_recommendation_system/
    ├── README.md                     # Complete project documentation
    ├── smartphone_recommendation.ipynb # Full Data Processing & Analysis Notebook
    ├── index.html                    # Single Page Application (UI + TOPSIS Engine)
    ├── smartphones_mcda.json         # Exported preprocessed dataset (100+ models)
    └── cleaned_smartphone_specs.csv  # Raw Kaggle smartphone specifications dataset
```

---

## 🔬 Mathematical Methodology: TOPSIS

TOPSIS ranks decision alternatives by calculating their relative closeness coefficient ($C_i$) to a virtual Positive Ideal Solution ($A^+$) and a Negative Ideal Solution ($A^-$) in normalized Euclidean space.

### Vector Normalization

$$r_{ij} = \frac{x_{ij}}{\sqrt{\sum_{k=1}^{m} x_{kj}^2}}$$

### Weighted Matrix Construction

$$v_{ij} = w_j \cdot r_{ij} \quad \text{where} \quad \sum w_j = 1.0$$

### Euclidean Spatial Distances

$$S_i^+ = \sqrt{\sum_{j=1}^{n} (v_{ij} - v_j^+)^2}, \quad S_i^- = \sqrt{\sum_{j=1}^{n} (v_{ij} - v_j^-)^2}$$

### Closeness Coefficient ($C_i$)

$$C_i = \frac{S_i^-}{S_i^+ + S_i^-}$$

---

## 🎯 Pre-Configured Archetypes

| Profile | Primary Focus | Key Weight Allocations | Hard Constraints |
| :--- | :--- | :--- | :--- |
| **Balanced** | All-Rounder | Perf: 25% \| Photo: 25% \| Battery: 20% \| Price: 10% | Max Price: €1,000 |
| **Gamer / Power User** | Raw Performance | Perf: 60% \| Screen: 15% \| Battery: 15% \| Price: 5% | Min Processor Benchmark $\ge 70.0$ |
| **Photographer** | Imaging & Optics | Photo: 45% \| Screen: 15% \| Perf: 15% \| Price: 15% | Max Price: €1,000 |
| **Budget First** | Price-to-Autonomy | Price: 55% \| Battery: 20% \| Perf: 10% | Max Price: €350 |

---

## 🚀 Live Web Demo & Kaggle Notebook

*   Check out the full notebook on Kaggle: 👉 **[Kaggle: Smartphone Recommendation System](https://www.kaggle.com/)** *(Update this link to your actual Kaggle Notebook URL)*
*   Access the hosted web application directly in your browser: 👉 **[Live MCDA Smartphone Decision Engine](https://bohne.github.io/kaggle_notebooks/)** *(Update this link to your actual deployment URL)*

---

## 🛠️ Local Development & Usage

### 1. Python Pipeline (Notebook)

Ensure you have pandas, numpy, matplotlib, and seaborn installed:

```bash
pip install pandas numpy matplotlib seaborn
```

Run the Jupyter notebook [`smartphone_recommendation.ipynb`](file:///c:/Users/bohne/OneDrive/Bureau/kaggle_notebooks/smartphone_recommendation.ipynb) or process `cleaned_smartphone_specs.csv` to clean the raw Kaggle dataset, run spatial diagnostics, and export `smartphones_mcda.json`.

### 2. Web SPA Local Launch

Simply launch a local HTTP server inside the `smartphone_recommendation_system` directory:

```bash
python -m http.server 8000
```

Open `http://localhost:8000` in your web browser.

---

## 📜 License

Distributed under the MIT License.
