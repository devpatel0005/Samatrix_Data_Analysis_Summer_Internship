# Data Analytics Portfolio — Selected Notebooks

This repository contains two internship projects designed as concise, resume-ready case studies. Together they demonstrate practical data cleaning, exploratory analysis, statistical inference, simulation, and experiment decision-making.

## Project 1 — Google Play Store Exploratory Data Analysis
- **Objective**: Analyze Google Play Store app data to identify category-level trends, engagement patterns, and actionable product insights.
- **Dataset**: Public Google Play Store app metadata (10,841 rows) including app name, category, rating, reviews, size, installs, type, price, content rating, and last updated fields.
- **Data Preparation**:
	- Handled missing values (`Rating` imputation with median; selective row removal for sparse missing fields).
	- Cleaned and converted key columns (`Reviews`, `Size`, `Installs`, `Price`) into numeric formats.
	- Engineered time features (`Day`, `Month`, `Year`) from `Last Updated`.
	- Removed duplicate apps to ensure cleaner category comparisons.
- **Analysis Performed**:
	- Univariate analysis for numeric and categorical features.
	- Skewness, kurtosis, and IQR-based outlier assessment.
	- Category popularity analysis (share of apps and top categories).
	- Install concentration analysis by category and content rating.
	- Correlation heatmap across numeric variables.
	- Bivariate and multivariate views: rating by app type, installs by category and type, and log-transformed installs/reviews for skewed distributions.
- **Key Findings**:
	- A small set of categories dominates both app volume and installs.
	- `Reviews` and `Installs` are strongly related.
	- Free apps generally drive higher installation reach.
	- Content rating and app type provide meaningful context when interpreting performance.
- **Notebook**: [Project_1_Google_Playstore_EDA.ipynb](Project_1_Google_Playstore_EDA.ipynb)

## Project 2 — A/B Testing Analysis (Conversion Optimization)
- **Objective**: Evaluate whether a new checkout funnel (Variant B) improves conversion compared with the baseline (Variant A).
- **Experiment Setup**:
	- Simulated traffic for two variants with equal allocation.
	- Baseline assumptions: 10,000 visitors per variant, with conversion probabilities near 10% (A) and 12% (B).
	- Used binomial simulation to generate purchases (binary outcomes).
- **Statistical Workflow**:
	- Computed conversion rates for both variants.
	- Built 95% confidence intervals for each proportion using normal approximation.
	- Ran a one-sided two-proportion z-test (`H0: pB <= pA`, `H1: pB > pA`).
	- Interpreted z-statistic and p-value for decision-making.
- **Sequential Monitoring Simulation**:
	- Simulated batch-wise monitoring (100 users per batch, 60 batches).
	- Tracked cumulative lift and p-values over time.
	- Demonstrated how significance can be monitored during experiment rollout.
- **Key Results**:
	- Simulated conversion rates showed B outperforming A (about 11.34% vs 9.73%).
	- Confidence intervals were non-overlapping in the sampled run.
	- Hypothesis test returned a statistically significant result (p-value < 0.05).
	- Sequential simulation also detected significant positive lift for Variant B.
- **Additional Concepts Covered**:
	- Interpretation of binomial distribution, p-value, z-test, and confidence intervals.
	- Monte Carlo simulation concept for uncertainty, win probability, and robustness checks.
- **Notebook**: [Project_2_ABtesting.ipynb](Project_2_ABtesting.ipynb)

## Technical Stack
- **Environment**: Python 3.8+ with Jupyter Notebook
- **Libraries**: pandas, numpy, matplotlib, seaborn, scipy, statsmodels

## How To Run
1. Open notebooks in Jupyter Notebook or JupyterLab.
2. Install dependencies:

- A `requirements.txt` file is included at the repository root listing the core dependencies.

```bash
pip install -r requirements.txt
```


## Contact
- **Name**: Dev Patel
- **Email**: devdpatel0005@gmail.com
- **GitHub**: https://github.com/devpatel0005

