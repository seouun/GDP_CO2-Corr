![Python](https://img.shields.io/badge/Python-3.x-blue)
![CO2](https://img.shields.io/badge/Topic-CO2%20Emissions-green)
![GDP](https://img.shields.io/badge/Topic-GDP-yellow)
![TimeSeries](https://img.shields.io/badge/Analysis-Time%20Series-purple)

# GDP–CO₂ Analysis: Economic Growth and Carbon Emissions

##A data analysis project exploring the relationship between GDP and CO₂ emissions across countries.
This study examines patterns of coupling and decoupling between economic growth and carbon emissions through visualization-driven exploratory analysis and extended time-series analysis.
---

## Repository Structure

| File | Description |
|------|------|
| `analysis.ipynb` | Initial analysis: exploratory correlation visualization |
| `analysis_advanced.ipynb` | Advanced analysis: extended time-series analysis |
| `report.pdf` | Report summarizing initial analysis results |
---

## Analysis Overview

### Initial Analysis (analysis.ipynb)

| Section | Description |
|------|------|
| Data Loading & Preprocessing | Handling missing values and preparing analysis-ready variables |
| Correlation Distribution | Distribution of GDP–CO₂ correlation coefficients (total vs per capita) |
| Growth Scatter Plot | GDP growth vs CO₂ growth (colored by population size) |
| Country Case Studies | Coupling (India, Thailand) vs Decoupling (Germany, Sweden) time-series comparison |
| Top & Bottom Countries | Bar charts of top and bottom 5 countries by correlation |
| Category-wise Distribution | Correlation comparison by population size, emission level, and GDP level |

### Advanced Analysis (analysis_advanced.ipynb)

| Section | Description |
|------|------|
| Global Trends | Long-term trends of global GDP and CO₂ emissions |
| Rolling Correlation | 5-year rolling correlation to track dynamic relationships |
| Period Comparison | Comparison between 2000–2010 and 2011–2020 |
| Decoupling Index | Quantifying decoupling using CO₂ growth / GDP growth ratio |

---

## Data Preparation

Download the dataset from Kaggle and place it in the **same directory** as the notebooks.

🔗 [Kaggle Dataset](https://www.kaggle.com/datasets/mackness/global-gdp-and-co-emissions-dataset-19602022)

File name: gdp_co2_by_country_v2.csv
---

## Key Findings

- A strong positive correlation between total GDP and CO₂ emissions is observed in many countries
- Greater variability is found in per capita measures, with some countries showing negative correlations
- High-income countries (Germany, Sweden) exhibit increasing decoupling trends over time
- The Decoupling Index reveals heterogeneity across countries and time periods
- Differences between total and per capita results highlight structural complexity
  → The growth–emissions relationship varies depending on population size, economic level, and emission structure
---

## Limitations & Future Work

- Correlation analysis does not imply causality
- The impact of trade regulations such as **CBAM** requires further investigation
- Future work may extend to econometric approaches (e.g., panel regression, causal inference)

---

## Environment

- **Language**: Python 3.x
- **Libraries**: pandas, numpy, matplotlib, seaborn
