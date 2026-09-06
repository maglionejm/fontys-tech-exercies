# Fontys Tech Exercises

A hands-on Python notebook series for learning data analytics and machine learning from zero. Three modules, nine notebooks, one guiding principle: **keep it simple**. Every notebook balances short theory blocks with immediate practice, explains every technical term the first time it appears, and ends with exercises plus worked solutions.

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

### M3 - ML Architectures and Deployment

Goes deeper: what is inside the models, how to run them in a real cloud, and how applications actually use them. Each notebook is self-contained.

| # | Notebook | What you learn | Open in Colab |
|---|----------|----------------|---------------|
| 1 | [Machine learning architectures](M3%20-%20ML%20Architectures%20and%20Deployment/01-machine-learning-architectures.ipynb) | Opening the black boxes: linear models, trees and ensembles, and neural networks built up from a single neuron — with decision-boundary visuals for every architecture, plus a plain-language tour of CNNs, RNNs and Transformers | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maglionejm/fontys-tech-exercies/blob/main/M3%20-%20ML%20Architectures%20and%20Deployment/01-machine-learning-architectures.ipynb) |
| 2 | [Deploying models in the cloud](M3%20-%20ML%20Architectures%20and%20Deployment/02-deploying-models-in-the-cloud.ipynb) | Turning a model into a real prediction API with FastAPI, testing it before shipping, packaging it with Docker, and deploying the same container to Google Cloud Run and AWS App Runner — with step-by-step walkthroughs, cost hygiene and cleanup | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maglionejm/fontys-tech-exercies/blob/main/M3%20-%20ML%20Architectures%20and%20Deployment/02-deploying-models-in-the-cloud.ipynb) |
| 3 | [Consuming models from applications](M3%20-%20ML%20Architectures%20and%20Deployment/03-consuming-models-from-applications.ipynb) | The last mile: calling a model API from Python with timeouts, error handling and retries; batch prediction; a working web page that calls the model; CORS; and how third-party AI APIs (and their keys) fit in — the notebook runs a real local server and consumes it over real HTTP | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maglionejm/fontys-tech-exercies/blob/main/M3%20-%20ML%20Architectures%20and%20Deployment/03-consuming-models-from-applications.ipynb) |

Recommended order: M1, then M2, then M3, each top to bottom. M1 notebook 1, all of M2 and most of M3 use the same Titanic dataset, so concepts carry over naturally.

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

- **Titanic passenger list** — loaded from a public GitHub URL (used in M1 notebook 1, all of M2 and M3 notebooks 2-3)
- **Palmer Penguins, tips, Anscombe's quartet** — loaded through `seaborn.load_dataset()`
- **Gapminder** — bundled with Plotly, no download needed
- **Handwritten digits and synthetic shapes (moons)** — bundled with scikit-learn, no download needed (M3 notebook 1)

## Good to know

- **No secrets, no accounts.** Nothing in this repo needs an API key, a `.env` file, or a login. Every notebook runs fully without any account. The only optional accounts are for the *publish to the internet* follow-along guides: a free Hugging Face account (M2 notebook 3) and free-tier Google Cloud / AWS accounts (M3 notebook 2) — those steps live in the guides, not in the code. Never paste tokens or passwords into notebooks.
- **Notebooks ship with outputs.** You can read every chart and result directly on GitHub without running anything. Interactive Plotly charts only render when you actually run the notebook (locally or in Colab).
- **`outputs/` folders** are created next to the notebooks while they run (cleaned CSVs, saved models, an exportable HTML dashboard, Hugging Face deployment files). They are gitignored on purpose — they are yours to generate.
