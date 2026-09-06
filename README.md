# Fontys Tech Exercises

A hands-on Python notebook series for learning data analytics and machine learning from zero. Two modules, six notebooks, one guiding principle: **keep it simple**. Every notebook balances short theory blocks with immediate practice, explains every technical term the first time it appears, and ends with exercises plus worked solutions.

Everything runs **locally** or in **Google Colab** with a single click. No accounts, no API keys, no configuration files needed — all datasets load automatically from public sources.

## Course structure

### M1 - Descriptive analytics

| # | Notebook | What you learn | Open in Colab |
|---|----------|----------------|---------------|
| 1 | [Data cleaning](M1%20-%20Descriptive%20analytics/01-data-cleaning.ipynb) | Finding and fixing missing values, duplicates, wrong types, inconsistent text and outliers — with a heavy focus on loops and pandas/numpy | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maglionejm/fontys-tech-exercies/blob/main/M1%20-%20Descriptive%20analytics/01-data-cleaning.ipynb) |
| 2 | [Descriptive statistics](M1%20-%20Descriptive%20analytics/02-descriptive-statistics.ipynb) | Describing data with numbers: central tendency, spread, distribution shape, frequencies, group comparisons and correlation — nothing predictive | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maglionejm/fontys-tech-exercies/blob/main/M1%20-%20Descriptive%20analytics/02-descriptive-statistics.ipynb) |
| 3 | [Visualization and dashboards](M1%20-%20Descriptive%20analytics/03-visualization-and-dashboards.ipynb) | Matplotlib, seaborn and interactive Plotly charts; chart-choice rules and design principles; building static and interactive dashboards and exporting them as shareable HTML | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maglionejm/fontys-tech-exercies/blob/main/M1%20-%20Descriptive%20analytics/03-visualization-and-dashboards.ipynb) |

### M2 - Machine Learning

The three notebooks tell one continuous story — predicting Titanic survival — but each one is self-contained and can be run on its own.

| # | Notebook | What you learn | Open in Colab |
|---|----------|----------------|---------------|
| 1 | [Data prep and feature engineering](M2%20-%20Machine%20Learning/01-data-prep-and-feature-engineering.ipynb) | Train/test splits and data leakage, imputation, encoding, scaling, feature engineering, and scikit-learn pipelines | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maglionejm/fontys-tech-exercies/blob/main/M2%20-%20Machine%20Learning/01-data-prep-and-feature-engineering.ipynb) |
| 2 | [Model selection](M2%20-%20Machine%20Learning/02-model-selection.ipynb) | Comparing six models fairly with cross-validation, confusion matrices, precision/recall/F1, ROC-AUC, overfitting vs underfitting, and how to choose a model in real life | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maglionejm/fontys-tech-exercies/blob/main/M2%20-%20Machine%20Learning/02-model-selection.ipynb) |
| 3 | [Model optimization and deployment](M2%20-%20Machine%20Learning/03-model-optimization-and-deployment.ipynb) | Hyperparameter tuning with grid and random search, saving models with joblib, wrapping the model in a Gradio web app, and deploying it free on Hugging Face Spaces | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maglionejm/fontys-tech-exercies/blob/main/M2%20-%20Machine%20Learning/03-model-optimization-and-deployment.ipynb) |

Recommended order: M1 top to bottom, then M2 top to bottom. M1 notebook 1 and all of M2 use the same Titanic dataset, so concepts carry over naturally.

## How to run

### Option A — Google Colab (zero setup)

1. Click any "Open In Colab" badge above.
2. In Colab, choose **Runtime > Run all**.

That is it. The first cell of every notebook installs anything missing (on Colab almost everything is preinstalled), and datasets download automatically.

### Option B — Locally

Requirements: Python 3.10 or newer and an internet connection (datasets are downloaded from public URLs on first run).

```bash
git clone https://github.com/maglionejm/fontys-tech-exercies.git
cd fontys-tech-exercies

# Create and activate a virtual environment
python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

# Install the dependencies
pip install -r requirements.txt

# Start Jupyter
jupyter lab
```

Then open any notebook and run it top to bottom. Each notebook is independent — you can start with any of them.

## Datasets

All datasets are small, public, and load automatically — no downloads to manage:

- **Titanic passenger list** — loaded from a public GitHub URL (used in M1 notebook 1 and all of M2)
- **Palmer Penguins, tips, Anscombe's quartet** — loaded through `seaborn.load_dataset()`
- **Gapminder** — bundled with Plotly, no download needed

## Good to know

- **No secrets, no accounts.** Nothing in this repo needs an API key, a `.env` file, or a login. The only optional account is a free Hugging Face account for the final *publish your app to the internet* step of M2 notebook 3 — and that step happens entirely in the browser. Never paste tokens or passwords into notebooks.
- **Notebooks ship with outputs.** You can read every chart and result directly on GitHub without running anything. Interactive Plotly charts only render when you actually run the notebook (locally or in Colab).
- **`outputs/` folders** are created next to the notebooks while they run (cleaned CSVs, saved models, an exportable HTML dashboard, Hugging Face deployment files). They are gitignored on purpose — they are yours to generate.
