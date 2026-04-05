# Development of an AML (Anti-Money Laundering) System for "Dropper" Detection

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://imgshields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

## Background
You are a Data Science team in a large bank. The Financial Monitoring Department (Compliance) is facing a problem: illegal transactions are passing through the bank using "dropper" (Money Mule) accounts. These are people who provide their accounts for the transit of stolen money.
Standard rules (a rules-based approach) produce too many false positives, blocking honest customers who simply use their accounts actively.

## Your Task
1. Analyze the provided dataset of transactional activity.
2. Build a binary classification model that identifies "droppers" (Is_Mule = 1).

## Data Characteristics
You have access to data regarding account age, transaction volumes, transfer frequency, and end-of-day balances.

## Business Requirement
The model must minimize the blocking of highly active honest customers (Crypto traders, freelancers) while still catching the droppers. **Note:** The classes are highly imbalanced (there are significantly fewer fraudsters than honest customers).

## Success Criteria & Interpretability
* **Metric:** Choose the right quality metric (Accuracy will not work!).
* **Interpretability:** You must be able to explain why the model flagged a customer as suspicious.

---

## Project Organization

```text
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         aml_system and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── aml_system         <- Source code for use in this project.
    │
    ├── __init__.py             <- Makes aml_system a Python module
    │
    ├── config.py               <- Store useful variables and configuration
    │
    ├── dataset.py              <- Scripts to download or generate data
    │
    ├── features.py             <- Code to create features for modeling
    │
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py          <- Code to run model inference with trained models          
    │   └── train.py            <- Code to train models
    │
    └── plots.py                <- Code to create visualizations