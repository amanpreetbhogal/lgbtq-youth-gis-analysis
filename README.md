# lgbtq-youth-gis-analysis

# Geospatial Analysis of Policies and Mental Health in Sexual Minority Youth

**Author:** Amanpreet Bhogal  

This project examines the relationship between harmful and protective LGBTQIA+ policies by U.S. state and their impact on sexual minority youth mental health outcomes—specifically, suicidal ideation. The analysis links national survey data with state-level policy indices and geospatial information to explore how structural and geographic contexts shape disparities in youth mental health.

---

## Motivation

The prevalence of diagnosed mental or behavioral health conditions among youth has risen sharply in recent years, underscoring the importance of identifying risk factors for poor mental health. Prior studies emphasize how sociopolitical climates and structural stigma can affect the wellbeing of LGBTQIA+ youth. Building on this literature, this project investigates whether state-level LGBTQIA+ policies—protective versus harmful—are associated with suicidal ideation among sexual minority youth.  

By integrating indicators of policy protection or harm with behavioral health outcomes, this work aims to uncover geographic patterns of risk and inform targeted policy interventions and public health strategies.

---

## Research Questions

1. Are sexual minority youth at higher risk for suicidal ideation than heterosexual youth?  
2. How do state-level policy environments and geographic location influence suicidal ideation among sexual minority youth?

---

## Data Sources

- **Census Bureau TIGER/Line Shapefiles:** [https://www2.census.gov/geo/tiger/GENZ2022/shp/](https://www2.census.gov/geo/tiger/GENZ2022/shp/)  
- **Youth Risk Behavior Surveillance System (YRBSS):** [https://www.cdc.gov/yrbs/data/index.html](https://www.cdc.gov/yrbs/data/index.html)  
- **LGBTQ+ Policy Data (ICPSR Study 37877):** [https://www.icpsr.umich.edu/web/RCMD/studies/37877](https://www.icpsr.umich.edu/web/RCMD/studies/37877)  

The Census Bureau TIGER/Line shapefiles provided the geographic boundaries for state-level mapping. The YRBSS dataset supplied individual-level information on sexual identity, mental health status, and state identifiers. The ICPSR policy data quantified each state’s LGBTQ+ policy environment, allowing the linkage of policy scores with youth mental health indicators.

---

## Methodology

Data were cleaned and merged using Python (`pandas`, `geopandas`, and `statsmodels`). The YRBSS microdata were joined with state-level policy tallies and Census shapefiles to create a combined dataset supporting both statistical modeling and geospatial visualization.  
Analyses included:
- **Logistic regression** estimating odds ratios for suicidal ideation by sexual identity across states.  
- **Meta-analytic regression** testing whether variation in these odds ratios correlated with differences in state LGBTQIA+ policy tallies.

---

## Key Findings

- The logistic regression showed a statistically significant positive association between sexual minority identity and suicidal ideation across all analyzed states.  
  - Odds ratios ranged from approximately **3 to 6**, indicating that sexual minority youth were several times more likely than heterosexual peers to have seriously considered suicide.  
- A meta-analytic regression examining the relationship between policy tallies and odds ratios found **no statistically significant association** (β = -0.0006, p = 0.501, R² = 0.017).  
  - Although the trend suggested that more protective policies may correspond to slightly smaller disparities, the effect was minimal.  

These findings suggest that while sexual minority youth consistently face higher suicide risk, **state-level policies alone do not fully explain** the variation in mental health disparities. Broader social and institutional factors—such as family acceptance, stigma, school support systems, and access to affirming care—likely play stronger roles.

---

## Reflection

This project marked my **first experience with GIS** and introduced me to working with shapefiles, polygon data, and geospatial visualization. Through this process, I learned how to analyze spatial patterns in sexual minority youth mental health and visualize policy disparities across the U.S.  

It was also my **first time using Python instead of R** for statistical analysis, which required overcoming a steep learning curve related to syntax, libraries, and workflows. One of the most challenging yet rewarding aspects was independently determining which statistical approaches were appropriate for the research questions, helping me grow in both methodological decision-making and analytical reasoning.

---

## Tools & Libraries
- **Python 3.13**
- `pandas`, `numpy`, `geopandas`, `matplotlib`, `seaborn`, `statsmodels`, `scipy`
- Data visualization and geospatial mapping with `geopandas` and Census shapefiles.

---

## View the Full Notebook
➡️ [project_portfolio.ipynb](./project_portfolio.ipynb)

---

### License
This project uses public data sources and is distributed under the MIT License.
