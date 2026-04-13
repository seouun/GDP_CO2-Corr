![Python](https://img.shields.io/badge/Python-3.x-blue)
![CO2](https://img.shields.io/badge/Topic-CO2%20Emissions-green)
![GDP](https://img.shields.io/badge/Topic-GDP-yellow)
![TimeSeries](https://img.shields.io/badge/Analysis-Time%20Series-purple)

# GDP–CO₂ Analysis: Economic Growth and Carbon Emissions

> Does economic growth inevitably mean more carbon emissions — or can countries grow while decoupling from carbon?

A two-phase exploratory analysis of the relationship between GDP and CO₂ emissions across 203 countries (1960–2022).  
This project examines **where** coupling and decoupling patterns emerge, and **how** those relationships have shifted over time — with direct implications for climate policy and sustainable development.

---

## Why This Question Matters

The tension between economic growth and carbon emissions sits at the heart of climate policy.  
If growth and emissions are structurally coupled, aggressive decarbonization risks economic contraction.  
If decoupling is achievable — as some high-income countries suggest — it becomes a blueprint worth understanding.

This project investigates that question empirically across countries and decades,  
using the same GDP–CO₂ framework that underpins tools like the **Environmental Kuznets Curve** and informs **carbon pricing policy** design.

---

## Analysis Structure

This project is organized as two sequential analyses, each building on the previous.

```
Phase 1: Where does decoupling happen?
   └── analysis.ipynb
        ├── Cross-sectional correlation analysis (203 countries)
        ├── GDP growth vs CO₂ growth scatter
        ├── Country case studies: Coupling vs Decoupling
        └── Category-wise breakdown (by population, income, emission level)

Phase 2: How has the relationship changed over time?
   └── analysis_advanced.ipynb
        ├── Global GDP and CO₂ trend (long-run view)
        ├── 5-year rolling correlation (dynamic relationship)
        ├── Period comparison: 2000–2010 vs 2011–2020
        └── Decoupling Index: CO₂ growth / GDP growth
```

---

## Repository Structure

| File | Description |
|---|---|
| `analysis.ipynb` | Phase 1: Correlation structure and cross-country patterns |
| `analysis_advanced.ipynb` | Phase 2: Time-series dynamics and decoupling quantification |
| `report.pdf` | Summary report of Phase 1 findings |

---

## Data

**Source:** [Kaggle — Global GDP and CO₂ Emissions Dataset 1960–2022](https://www.kaggle.com/datasets/mackness/global-gdp-and-co-emissions-dataset-19602022)

Download `gdp_co2_by_country_v2.csv` and place it in the same directory as the notebooks.

- **Coverage:** 203 countries, up to 63 years per country
- **Key variables:** GDP (total & per capita), CO₂ emissions (total & per capita), population category, GDP category, emission category

---

## Key Findings

### Phase 1 — Cross-Country Correlation Patterns

**Total GDP and total CO₂ are strongly coupled in most countries** — but the story changes when measured per capita.

| Country | Total Correlation | Per Capita Correlation | Pattern |
|---|---|---|---|
| India | +0.996 | +0.937 | Strong coupling |
| Thailand | +0.991 | +0.986 | Strong coupling |
| Germany | −0.781 | −0.836 | Decoupling |
| Sweden | −0.788 | −0.831 | Decoupling |

Per-capita correlations show far greater variability across countries — with a subset showing **negative correlations**, meaning economic growth and emissions are moving in opposite directions. This is the empirical signature of decoupling.

High-income countries (Germany, Sweden) already show negative correlations over the full period, while emerging economies (India, Thailand) remain in strong coupling territory.

**Category-level patterns** confirm that the coupling–decoupling divide tracks closely with GDP level and emission structure — not population size alone.

---

### Phase 2 — Time-Series Dynamics

**The relationship is not static.** Rolling correlation and period comparison reveal that the coupling–decoupling structure has been shifting.

**Period comparison (2000–2010 vs 2011–2020):**

| Country | 2000–2010 | 2011–2020 | Change |
|---|---|---|---|
| Germany | −0.607 | −0.516 | +0.09 (slight weakening of decoupling) |
| Sweden | −0.530 | −0.695 | −0.17 (decoupling deepened) |
| India | +0.991 | +0.988 | −0.003 (stable coupling) |
| Thailand | +0.992 | +0.876 | −0.12 (coupling weakening) |

Sweden's decoupling deepened in the 2011–2020 period, while Germany's showed slight reversal — suggesting that decoupling trajectories are country-specific rather than a uniform pattern among high-income economies.

**Decoupling Index (CO₂ growth / GDP growth):**

- Index < 0 → strong decoupling (CO₂ falling while GDP grows)
- 0 < Index < 1 → weak decoupling (CO₂ growing slower than GDP)
- Index > 1 → coupling (CO₂ growing faster than GDP)

Boxplot by GDP category shows that high-income countries have systematically lower Decoupling Index distributions — but with significant within-group variance, meaning income level is a necessary but not sufficient condition for decoupling.

---

## Implications for Climate Policy

These findings connect directly to ongoing debates in climate economics:

- **Carbon pricing design:** Countries still in coupling phase require different policy levers than those in decoupling phase
- **Technology transfer:** The gap between Germany/Sweden and India/Thailand suggests that decoupling may require structural economic transitions beyond GDP growth alone
- **Trade regulations:** Border carbon mechanisms like **CBAM** implicitly assume that production-based emissions can be attributed nationally — but decoupling complicates this picture when countries outsource emissions-intensive production

---

## Limitations & Future Work

- Correlation does not imply causality — no causal claims are made here
- Analysis uses production-based CO₂, not consumption-based; results may differ under a consumption accounting framework
- Energy mix, industrial structure, and trade composition are not incorporated due to data availability
- **Future extensions:** Panel regression with fixed effects, Environmental Kuznets Curve testing, causal inference (e.g., Granger causality), consumption-based emissions reallocation

---

## Environment

- **Language:** Python 3.x
- **Libraries:** pandas, numpy, matplotlib, seaborn
