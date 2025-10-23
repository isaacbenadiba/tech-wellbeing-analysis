# Tech & Well-Being: A Statistical Analysis of Screen Time, Sleep, and Mental Health

This project investigates the relationship between daily screen time and mental health outcomes — specifically stress, anxiety, and depression — while testing whether sleep quality moderates these effects. We use realistic synthetic survey data from 5,000 participants containing behavioral, psychological, and lifestyle variables. The analysis integrates classical statistical testing, distribution modeling, and model diagnostics, following a structured and reproducible pipeline.

## Repository Structure
statistical_theory_project  
├── data/                           # Raw or prepared data (CSV)  
├── notebooks/  
│   ├── 01_eda.ipynb                # Exploratory Data Analysis  
│   └── 02_models_main.ipynb        # Modeling, inference, and diagnostics  
├── outputs/  
│   ├── figures/                    # Exported plots (PNG, CSV)  
├── paper/  
│   └── statistical_theory_project.pdf  
├── requirements.txt  
└── README.md

## Research Question
Does daily screen time predict mental health outcomes (stress, anxiety, and depression), and is this association moderated by sleep quality?

## Secondary Aim
To characterize the statistical distribution of daily screen time in order to inform model selection and diagnostics.

## Methods & Statistical Tools
- Regression with interaction term: `screen_time × sleep_quality`  
- Tests: Generalized Likelihood Ratio Test (GLRT), Wald test  
- Multiple testing correction: Benjamini–Hochberg FDR  
- Nonparametric test: Mann–Whitney U (Low vs. High sleep quality)  
- Distributional modeling: Gamma–Poisson mixture for screen time  
- Diagnostics:  
  - Heteroskedasticity (Breusch–Pagan)  
  - Multicollinearity (VIF)  
  - Descriptive statistics and correlation analysis

## Key Results
- Daily screen time is positively associated with stress, anxiety, and depression.  
- Sleep quality shows a protective effect but does not significantly moderate the effect of screen time.  
- The Gamma distribution provides a good fit for screen time (mean ≈ 5.04 h/day, mild right skew).  
- Evidence of heteroskedasticity and multicollinearity in regression diagnostics.  
- All results are reproducible from the notebooks and outputs.

## Requirements
python >= 3.9  
numpy  
pandas  
scipy  
statsmodels  
matplotlib  
seaborn

## How to Reproduce the Analysis
1. Clone the repository:  
`git clone https://github.com/isaacbenadiba/tech-wellbeing-analysis.git`  
`cd tech-wellbeing-analysis`  

2. Install dependencies:  
`pip install -r requirements.txt`  

3. Run notebooks:  
Start Jupyter Lab / Notebook and execute:  
- `01_eda.ipynb` for exploratory analysis  
- `02_models_main.ipynb` for modeling and tests

4. Check outputs:  
Figures and test results are saved in `outputs/`  
Final paper: `paper/statistical_theory_project.pdf`

## Author
Isaac Benadiba  
B.Sc. Mathematics & Statistics | Bar-Ilan University  
isaacbenadiba11@gmail.com  
Tel Aviv / Madrid

