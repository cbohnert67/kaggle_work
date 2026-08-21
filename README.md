# 🦅 Kaggle Work & Data Science Portfolio

Welcome to `kaggle_work` — a curated portfolio of end-to-end Data Science, Machine Learning, and Multi-Criteria Decision Analysis (MCDA) projects developed on Kaggle.

This repository serves as a bridge between exploratory data engineering pipelines (executed in Jupyter/Kaggle notebooks) and production-ready visual web applications.

---

## 🌟 Featured Projects

| Project | Domain / Tech Stack | Kaggle Notebook | Live Interactive Demo |
| :--- | :--- | :--- | :--- |
| **📱 Smartphone Recommendation System** | MCDA, TOPSIS Solver, Data Pipeline, Vanilla JS, Chart.js, Tailwind CSS | [🦅 View on Kaggle](https://www.kaggle.com/code/computux/smartphone-recommendation-system) | [🌐 Live Web Application SPA](https://cbohnert67.github.io/kaggle_work/smartphone_recommendation_system/) |

---

## 📂 Featured Showcase

### 📱 1. Smartphone Recommendation System (MCDA & TOPSIS Engine)

An interactive decision science engine designed to solve the smartphone selection problem using TOPSIS (Technique for Order Preference by Similarity to Ideal Solution).

*   **Folder Location**: [`./smartphone_recommendation_system/`](file:///c:/Users/bohne/OneDrive/Bureau/kaggle_notebooks/smartphone_recommendation_system/)
*   **Key Highlights**:
    *   Replaces rigid binary SQL filters (`WHERE price <= X`) with $n$-dimensional Euclidean distance scoring ($C_i \in [0, 1]$).
    *   Prevents budget-bias in power-user profiles using non-compensatory gaming thresholds and non-linear processor performance scaling ($\text{Score}^{1.8}$).
    *   Dynamic hardware variant deduplication to preserve model diversity in top recommendations.
    *   Zero-latency client-side Web SPA executing the TOPSIS solver in < 5ms directly inside the browser.
    *   Visual spatial decision analytics ($S_i^+$ vs $S_i^-$ distance map), Pareto efficiency frontiers, and multi-profile radar charts.

---

## 📂 Repository Structure

```text
kaggle_work/
├── README.md                            # Main portfolio documentation
└── smartphone_recommendation_system/    # Smartphone MCDA Decision Project
    ├── README.md                        # Detailed project documentation
    ├── index.html                       # Client-Side Web SPA Decision Engine
    ├── smartphones_mcda.json            # Processed dataset artifact for web SPA
    ├── cleaned_smartphone_specs.csv     # Raw Kaggle smartphone specifications dataset
    └── smartphone_recommendation.ipynb  # Full Kaggle ETL & TOPSIS Notebook
```

---

## 🚀 Getting Started

### Clone the Repository

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/kaggle_work.git
cd kaggle_work
```

### Run the Web SPA Locally

To test any interactive web application locally, navigate into the project directory and launch a local HTTP server:

```bash
cd smartphone_recommendation_system
python -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

---

## 📜 License

This repository is distributed under the MIT License. Feel free to explore, fork, and adapt the projects!
