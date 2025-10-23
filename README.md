Tech & Well-Being: A Statistical Analysis of Screen Time, Sleep, and Mental Health
Project Overview

This project investigates the relationship between daily screen time and mental health outcomes — specifically stress, anxiety, and depression — while testing whether sleep quality moderates these effects.

We use realistic synthetic survey data from 5,000 participants containing behavioral, psychological, and lifestyle variables.
The analysis integrates classical statistical testing, distribution modeling, and model diagnostics, following a structured and reproducible pipeline.

Repository Structure

   statistical_theory_project
├── data/                           # Raw or prepared data (CSV)
├── notebooks/
│   ├── 01_eda.ipynb                # Exploratory Data Analysis
│   └── 02_models_main.ipynb        # Modeling, inference, and diagnostics
├── outputs/
│   ├── figures/                    # Exported plots (PNG, CSV)
│
├── paper/
│   └── statistical_theory_project.pdf
├── requirements.txt
└── README.md

Research Question

Does daily screen time predict mental health outcomes (stress, anxiety, depression)?
Does sleep quality moderate this effect, and what is the distributional nature of screen time behavior?

Methods & Statistical Tools

The analysis applies multiple statistical techniques covered in the course:

Regression with interaction term

screen_time × sleep_quality

Tested using GLRT and Wald test

Multiple testing correction using Benjamini–Hochberg FDR

Nonparametric tests: Mann–Whitney U (Low vs. High sleep quality)

Distributional modeling: Gamma–Poisson mixture for screen time

Diagnostics:

Heteroskedasticity (Breusch–Pagan)

Multicollinearity (VIF)

Descriptive statistics and correlation analysis

Key Results

Daily screen time is positively associated with stress, anxiety, and depression levels.

Sleep quality shows a strong protective effect but does not significantly moderate the effect of screen time.

The Gamma distribution provides a good fit for screen time (mean ≈ 5.04 h/day, mild right skew).

Strong evidence of heteroskedasticity and multicollinearity in regression diagnostics.

All results are reproducible from the notebooks and outputs.


Requirements

python >= 3.9
numpy
pandas
scipy
statsmodels
matplotlib
seaborn

How to Reproduce the Analysis

Clone the repository

git clone https://github.com/<isaacbenadiba>/tech-wellbeing-analysis.git
cd tech-wellbeing-analysis

Install dependencies

pip install -r requirements.txt


Run notebooks

Start Jupyter Lab / Notebook

Execute:

01_eda.ipynb for exploratory analysis

02_models_main.ipynb for modeling and tests

Check outputs

Figures and test results are saved in outputs/

Final paper: paper/statistical_theory_project.pdf

Author

Isaac Benadiba
B.Sc. Mathematics & Statistics | Bar-Ilan University
📧 isaacbenadiba11@gmail.com

📍 Tel Aviv / Madrid
