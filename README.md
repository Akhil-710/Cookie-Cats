# Cookie Cats A/B Testing Analysis

<p align="center">
<img src="images/executive_dashboard.png" width="950">
</p>
The executive dashboard summarizes the experiment outcomes, highlighting retention metrics, statistical significance, and the final product recommendation.
---

## Executive Summary

This project analyzes an A/B experiment conducted on the mobile game **Cookie Cats** to evaluate whether moving the first progression gate from **Level 30** to **Level 40** improves player retention.

Using exploratory data analysis, hypothesis testing, confidence intervals, bootstrap validation, statistical power analysis, and engagement-based segmentation, the analysis finds that maintaining the original gate at **Level 30** results in significantly higher long-term player retention without affecting short-term engagement.

The analysis concludes that maintaining the original progression gate at Level 30 produces significantly higher seven-day retention while showing no meaningful difference in one-day retention. Statistical testing, bootstrap validation, and power analysis consistently support this recommendation.

The project demonstrates an end-to-end product analytics workflow, from data validation to business recommendations.

---

# Project Overview

Cookie Cats is one of King's most popular mobile puzzle games.

To evaluate whether delaying player progression improves engagement, an A/B experiment was conducted comparing two versions of the game.

| Experiment Group | Progression Gate |
|-----------------|------------------|
| Gate 30 | Original Version |
| Gate 40 | Experimental Version |

The objective of this project is to determine whether changing the first progression gate improves player retention and to provide a statistically supported product recommendation.

---

# Business Question

**Should Cookie Cats delay the first progression gate from Level 30 to Level 40 to improve long-term player retention without negatively impacting player engagement?**

The answer is evaluated using statistical inference, bootstrap validation, statistical power analysis, and engagement-based segmentation.

---

# Dataset

| Metric | Value |
|---------|--------|
| Total Players | 90,189 |
| Gate 30 | 44,700 |
| Gate 40 | 45,489 |

### Features

| Variable | Description |
|-----------|-------------|
| userid | Unique player identifier |
| version | Experimental group |
| sum_gamerounds | Total number of game rounds played |
| retention_1 | Returned after one day |
| retention_7 | Returned after seven days |

---

# Executive Findings

| Metric | Result |
|---------|--------|
| Players | **90,189** |
| One-Day Retention | No statistically significant difference |
| Seven-Day Retention | **Gate 30 performs significantly better** |
| Bootstrap Validation | Confirmed |
| Statistical Power | **88.39%** |
| Final Recommendation | **Maintain Gate 30** |

---

---

## Overall Retention

<p align="center">
<img src="images/overall_retention.png" width="700">
</p>

---

## Retention Improvement

<p align="center">
<img src="images/retention_improvement.png" width="650">
</p>

---

## Player Segmentation

<p align="center">
<img src="images/segment_analysis.png" width="850">
</p>

---

## Engagement Distribution

<p align="center">
<img src="images/engagement_distribution.png" width="700">
</p>

---

---

# Analysis Workflow


Business Understanding
        │
        ▼
Data Validation
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Sample Ratio Mismatch (SRM)
        │
        ▼
Hypothesis Testing
        │
        ▼
Confidence Intervals
        │
        ▼
Effect Size (Cohen's h)
        │
        ▼
Bootstrap Validation
        │
        ▼
Statistical Power Analysis
        │
        ▼
Player Segmentation
        │
        ▼
Executive Dashboard
        │
        ▼
Business Recommendation
# Project Structure

text
cookie_cats_ab_testing_analysis/

├── data/
│   ├── raw/
│   └── cleaned/
│
├── notebooks/
│   ├── 01_Business_Understanding.ipynb
│   ├── 02_Experiment_Validation_and_EDA.ipynb
│   ├── 03_Hypothesis_Testing.ipynb
│   ├── 04_Bootstrap_Validation.ipynb
│   ├── 05_Power_Analysis.ipynb
│   ├── 06_Segmentation_Analysis.ipynb
│   ├── 07_Executive_Dashboard.ipynb
│   └── 08_Final_Business_Report.ipynb
│
├── images/
├── README.md
├── requirements.txt
└── LICENSE

# Methodology

The project follows a structured analytics workflow consisting of:

- Business Understanding
- Data Validation
- Exploratory Data Analysis
- Sample Ratio Mismatch (SRM) Validation
- Two-Proportion Z-Test
- Confidence Interval Estimation
- Effect Size (Cohen's h)
- Bootstrap Validation
- Statistical Power Analysis
- Engagement-Based Segmentation
- Executive Dashboard
- Business Reporting

---

# Key Findings

- The player activity distribution is highly right-skewed, with a small number of highly engaged players contributing disproportionately large numbers of game rounds.
- No missing values or duplicate observations were identified.
- One-day retention showed no statistically significant difference between the two experiment groups.
- Seven-day retention was significantly higher for players assigned to Gate 30.
- Bootstrap resampling confirmed the robustness of the hypothesis testing results.
- Statistical power exceeded the recommended 80% threshold, indicating sufficient sample size.
- Medium and High engagement players benefited most from maintaining the progression gate at Level 30.

---

# Business Recommendation

Based on the statistical evidence generated throughout the analysis, the recommended product decision is to **maintain the progression gate at Level 30**.

Although delaying the gate to Level 40 does not meaningfully affect short-term retention, it leads to a statistically significant reduction in seven-day retention. The strongest impact is observed among Medium and High engagement players, who are the most valuable users for long-term engagement.

---

# Technologies Used

| Category | Tools |
|----------|-------|
| Programming | Python |
| Data Analysis | Pandas, NumPy |
| Statistics | SciPy, Statsmodels |
| Visualization | Matplotlib |
| Environment | Jupyter Notebook |

---

# Running the Project

Clone the repository.

bash
git clone https://github.com/SambhavyaNayak/cookie-cats-ab-testing-analysis.git

Install the required libraries.

bash
pip install -r requirements.txt


Run the notebooks sequentially from **01** through **08**.

---

# Skills Demonstrated

- Product Analytics
- Experimental Design
- A/B Testing
- Exploratory Data Analysis
- Statistical Inference
- Hypothesis Testing
- Confidence Intervals
- Bootstrap Resampling
- Statistical Power Analysis
- User Segmentation
- Executive Dashboard Design
- Business Reporting
- Data Storytelling

---

# Future Improvements

Possible extensions to this analysis include:

- Incorporating monetization metrics such as ARPU and Lifetime Value (LTV)
- Performing cohort-based retention analysis
- Applying survival analysis to model player churn
- Building predictive churn models using machine learning
- Developing an interactive Power BI or Tableau dashboard


